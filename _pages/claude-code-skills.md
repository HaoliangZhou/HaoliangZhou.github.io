---
title: "Claude Code Skills 和 Subagents 的个人实践"
permalink: /blog/claude-code-skills-subagents/
excerpt: "两套落地系统：大规模自动化文献下载 Agent 与自迭代 AI Scientist，展示 Skills 与 Subagents 如何把 LLM 升级为生产级科研基础设施。"
author_profile: true
---

<div class="floating-card" style="padding: 2rem; margin-bottom: 2rem;">
  <p class="tag-accent" style="display: inline-block; margin-bottom: 0.8rem;">LLM Orchestration · Research Workflow</p>
  <h1 style="margin-top: 0;">Claude Code Skills 和 Subagents 的个人实践</h1>
  <p style="color: #495057; font-size: 1rem;">网上关于 Claude Code 的文章不少，但多数还停留在「怎么接 MCP」「怎么接第三方大模型」这种入门层面，对 Skills 和 Subagents 的讨论往往浅尝辄止。这里分享我在真实科研场景中搭建的两套系统：大规模、跨付费墙的自动化文献下载 Agent，以及在特定数据集上自动迭代优化预测算法的「自迭代 AI Scientist」。</p>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; margin-top: 1rem;">
    <div class="highlight-block floating-card" style="padding: 1rem;">
      <h3 style="margin-top: 0;">你会看到</h3>
      <ul>
        <li>Skills 与 Subagents 在实践中的真实角色</li>
        <li>如何把 LLM 从「聊天工具」升级为生产级科研基础设施</li>
        <li>长时间运行、复杂优化任务里遇到的坑与规避方案</li>
      </ul>
    </div>
    <div class="highlight-block floating-card" style="padding: 1rem;">
      <h3 style="margin-top: 0;">两套落地系统</h3>
      <ul>
        <li>跨付费墙的自动化文献下载 Agent</li>
        <li>可连续迭代的 AI Scientist</li>
      </ul>
    </div>
  </div>
</div>

## 一、AI 驱动的自动化文献下载 Agent

在生命科学和化学研究中，文献大多不属于 Open Access：打开学校 VPN、逐篇搜索、点击下载、命名、归档，效率惨不忍睹。传统爬虫难以覆盖复杂业务逻辑，跨站授权也棘手，于是我尝试让 Claude Code 接管整条流程。

<div class="floating-card" style="padding: 0.75rem 0.75rem 0.9rem; margin: 1.2rem 0;">
  <img src="/images/claude-pipeline.png" alt="自动化文献下载 Pipeline 示意图" style="width: 100%; border-radius: 12px; box-shadow: 0 6px 18px rgba(1, 47, 99, 0.08);">
  <p style="text-align: center; margin: 0.65rem 0 0; color: #495057;">自动化文献下载 Pipeline 示意图（由 Nano Banana Pro 生成）</p>
</div>

### 第一阶段：从 Agent 到 Skill 的演变

- **初代 Agent 的诞生**：围绕多肽自组装主题做文献综述，要求标准化命名（如 `<YYYY>_<JournalAbbr>_<Sanitized-Title>_MS.pdf`）、添加前检查本地 total.htm 去重。首次运行约 10 分钟、32 次工具调用，收回 50 篇新文献。
- **问题暴露**：通过 MCP 检索到的文献很多，但 Open Access 下载不稳定，数量受限。
- **规模化挑战 → 引入 API 与 Skills**：利用机构订阅的 Springer、Elsevier、Wiley 的 TDM API 获取付费文献；OA 文献用 OpenAlex REST API。将「按 DOI 下载 PDF」封装成 Skill（`.claude/skills/paper-download` 内的 `download_by_doi.py`、`download_multiple_dois.py` 和 `SKILL.md`），Agent 只做调度。此后只需一句「帮我下载 100 篇 xxx 领域的文献」即可触发。

### 第二阶段：大规模测试与鲁棒性优化

- **15293 条多肽自组装文献压力测试**：成功下载 9071 篇，成功率 59.3%。TDM API 渠道表现突出：Elsevier 99.8%，Wiley 95.9%，并有 Unpaywall 回退。
- **解决上下文坍缩与「偷懒」**：在下载 10000 篇任务时，Agent 约 200 篇后提前收尾。应对策略：
  - 限制 MCP 搜索 `max_results`，避免上下文爆炸。
  - 分批执行：生成 `doi_batch_1.txt`、`doi_batch_2.txt`，逐批调用下载 Skill。
  - 后台执行长命令：在 `CLAUDE.md` 记忆「Always execute download command in the background」避免超时。
- **进一步优化**：使用 `continuous-claude`（基于 Git 管理任务进度）让 Claude 持续运行直至完成目标。

<div class="floating-card" style="padding: 1.2rem 1.4rem; margin: 1.5rem 0;">
  <h4 style="margin-top: 0;">小结：AI 驱动科研工作流的价值</h4>
  <p style="margin-bottom: 0.4rem;">通过 MCP 和 Skills，把复杂逻辑（多源检索、API 鉴权、去重、标准化命名）剥离出 LLM 推理层，封装进稳定脚本，LLM 仅负责编排。原本需数周的文献收集压缩到极短时间，为后续信息提取奠定数据基础。</p>
  <p style="margin: 0;">项目已开源：<a class="link-accent" href="https://github.com/jxtse/auto-paper-harvester">auto-paper-harvester</a></p>
</div>

## 二、自迭代 AI Scientist

文献下载解决了「数据入口」，下一个问题是：能否让 AI 自己调模型、跑实验、迭代配置？

### 早期版本：单体 Agent 的瓶颈

- Python 脚本驱动 LLM 做特征选择与算法设计，Claude Code / Codex 负责实现。
- 运行后输出验证集 c-index（衡量排序一致性的指标，近似「验证集表现分数」），反馈给 LLM 继续调整。
- 问题：实现经常「写一半停手」，需多轮提示；迭代一两轮后 c-index 开始下降，LLM 缺少结构化上下文时极易失焦。

### 用 Skills + Subagents 重新架构：让 Claude 连续跑几个小时

我把系统拆成「1 个 Skill + 4 个 Subagent」，Claude 只做 orchestrate：

- **Subagent 1：Algorithm-Implementer**：按特征集合、建模思路、超参配置实现模型，输出 `results.json`、`model_checkpoint.pt`、`training_log.txt`、`implementation_summary.md`。
- **Subagent 2：Feature-Selection-Agent**：基于数据集特征、当轮总结、历史尝试进行特征选择与生成，输出 `selected_features.json`。
- **Subagent 3：Idea-Iteration-Agent**：根据新特征、历史实现总结迭代建模思路，输出优先级排序的 `ideas.json`。
- **Subagent 4：Optimization-Algorithm-Agent**：将想法具体化为训练配置，输出 `config.yaml`（batch size、epoch、early stopping、正则强度等）。

> 所有 Subagent 定义在 `.claude/subagents`，可通过 `/agents` 查看。Subagent 2 提供查看数据集列名与样本的 Skill；Subagent 3 提供调用 LLM API 迭代想法的 Skill，包含精心设计的迭代 prompt。

**收益**：

- 职责清晰，避免单体 Agent stuck。
- Claude 只协调，不必记住所有历史；结构化文件成为上下文来源。
- 系统可连续运行数小时，LLM 每轮仅消费高价值、压缩过的信息。

## 三、两项目抽象出的 Claude Code 最佳实践

<div class="floating-card" style="padding: 1.2rem 1.4rem; margin: 1.5rem 0;">
  <ol style="margin: 0; padding-left: 1.1rem;">
    <li><strong>把负载从推理层转移到执行层：</strong>凡是循环、计数、精准匹配逻辑，一律下沉为 Python Skills。LLM 只做「理解意图 → 组装参数 → 调用 Skills → 检查返回」。</li>
    <li><strong>用 Subagents 做上下文防火墙：</strong>不同角色隔离上下文，互相只传递 Summary/JSON，高价值压缩信息延缓上下文污染。</li>
    <li><strong>状态外置而非内置：</strong>对话历史最不可靠。下载进度放在 `total.htm`、`doi_batch.txt`，AI Scientist 的进化路径放在 `ideas.json`、`config.yaml`，执行流转依赖 `continuous-claude` 的 Git 提交。</li>
  </ol>
</div>

## 四、结语

从 Chatbot 到 Claude Code，正在经历从 Prompt Engineering 走向 Context Engineering 的范式转变。自动化文献下载证明了「AI 检索 + TDM API 下载」的有效组合；自迭代 AI Scientist 证明了结构化状态与多 Agent 协同让 LLM 具备长时程推理与探索能力。核心不在炫技式 prompt，而在于为模型构建一个确定性、可观测、可容错的生存环境。

未来，LLM 编排 + 专业代码执行 + 多智能体协作，或许将成为科研自动化的新常态。
