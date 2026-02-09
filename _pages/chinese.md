---
permalink: /
title: ""
excerpt: "中文"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">


{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}


# 🧍‍♂️ 关于我
<span class='anchor' id='about-me'></span>
我目前是一名<a href="https://www.tjut.edu.cn" class="link-accent">天津理工大学</a>计算机科学与工程学院<a href="https://i-mac-lab.net" class="link-accent">智能媒体分析与计算实验室</a>的二年级博士生, 师从<a href="https://ia.cas.cn/rcdw/jcqn/202404/t20240422_7129942.html" class="link-accent">徐常胜</a>研究员(国家杰青, IEEE/IAPR/CCF/CSIG Fellow)和<a href="https://cs.tjut.edu.cn/info/1226/1795.htm" class="link-accent">张飞飞</a>教授。
在此之前, 我分别于2021年和2024年在<a href="https://www.just.edu.cn/" class="link-accent">江苏科技大学</a>获得了学士和硕士(导师: <a href="https://mypage.just.edu.cn/jsjkxgc/hsc/list.htm" class="link-accent">黄树成</a>教授)学位。



<div class="quote-accent">
我目前的研究方向为 <span class="accent-text">多模态学习, 计算机视觉</span>, 具体包括: 
  <ul>
    <li><span class="primary-gradient-text">组合式图像检索</span></li>
    <li><span class="primary-gradient-text">多模态学习</span></li>
    <li><span class="primary-gradient-text">测试时自适应, 持续学习</span></li>
    <li><span class="primary-gradient-text">人脸表情识别, 微表情识别</span></li>
  </ul>
</div>



<!-- <span class='anchor' id='-news'></span>
# 🔥 News
- *2026.02*: &nbsp;🎉🎉 One paper is accepted by the <span class="accent-text">IEEE TMM</span> journal. _(SCI, Q1, IF=9.7, CCF-A)_
- *2025.12*: &nbsp;🎉🎉 I am supported by China Association for Science and Technology <span class="accent-text">Talent Cultivation Project</span>.
- *2025.12*: &nbsp;🎉🎉 One paper is accepted by the <span class="accent-text">Artificial Intelligence Review</span> journal. _(SCI, Q1, IF=13.9)_
- *2025.11*: &nbsp;🎉🎉 One paper is accepted by the <span class="accent-text">AAAI 2026</span> conference. _(CCF-A)_
- *2025.10*: &nbsp;🎉🎉 One paper is accepted by the <span class="accent-text">IEEE TIP</span> journal. _(SCI, Q1, IF=13.7, CCF-A)_
- *2024.12*: &nbsp;🎉🎉 Two papers are accepted by the <span class="accent-text">Neurocomputing</span> journal. _(SCI, Q1, IF=6.5)_
- *2024.07*: &nbsp;🎉🎉 One paper is accepted by the <span class="accent-text">IEEE TCSVT</span> journal. _(SCI, Q1, IF=11.1, CCF-B)_
- *2023.12*: &nbsp;🎉🎉 I am awarded <span class="accent-text">National Scholarship</span>.
 -->



<span class='anchor' id='-publications'></span>
# 📃 学术论文

<div id="publications-wrapper">
  <div id="filter-container"></div>
  
  <div class='paper-box floating-card' data-tags="第一作者, Test-Time Reinforcement Learning, Composed Image Retrieval, CCF-A">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">AAAI 2026</div>
      <img src='/images/ttrldr.png' alt="TTRLDR Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>Duplex Rewards Optimization for Test-Time Composed Image Retrieval</h3>
      <div class="authors"><span class="primary-gradient-text">Haoliang Zhou</span>⭐️, Feifei Zhang, Changsheng Xu</div>
      <div class="venue">The Fortieth AAAI Conference on Artificial Intelligence (AAAI 2026)</div>
      <div class="links">
        <a href="https://github.com/HaoliangZhou/TT-RLDR" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <a href="https://github.com/HaoliangZhou/TT-RLDR" class="btn-accent"><i class="fab fa-github"></i> Code</a>
      </div>
    </div>
  </div>

  <div class='paper-box floating-card' data-tags="Zero-shot Learning, Composed Image Retrieval, 中科院一区, CCF-A">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">IEEE TMM 2026</div>
      <img src='/images/mmcir.png' alt="MMCIR Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>Enhancing Representation Inversion and Alignment for Zero-Shot Composed Image Retrieval</h3>
      <div class="authors">Feifei Zhang, Jia Chen, <span class="primary-gradient-text">Haoliang Zhou</span>, Changsheng Xu</div>
      <div class="venue">IEEE Transactions on Multimedia (TMM 2026), SCI, 中科院一区, IF=9.7, CCF-A</div>
      <div class="links">
        <a href="https://" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <!-- <a href="https://" class="btn-accent"><i class="fab fa-github"></i> Code</a> -->
      </div>
    </div>
  </div>

  <div class='paper-box floating-card' data-tags="Facial Expression Recognition, Transfer Learning, 中科院一区">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">AI Review 2026</div>
      <img src='/images/eaclip.png' alt="EACLIP Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>Emotion-aware Adaptation of CLIP model for Facial Expression Recognition</h3>
      <div class="authors">Jing Huan, Mingxing Li, <span class="primary-gradient-text">Haoliang Zhou</span></div>
      <div class="venue">Artificial Intelligence Review (2025), SCI, 中科院一区, IF=13.9</div>
      <div class="links">
        <a href="https://link.springer.com/article/10.1007/s10462-025-11468-4" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <!-- <a href="https://" class="btn-accent"><i class="fab fa-github"></i> Code</a> -->
      </div>
    </div>
  </div>
  
  <div class='paper-box floating-card' data-tags="第一作者, Continual Learning, Composed Image Retrieval, 中科院一区, CCF-A">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">IEEE TIP 2025</div>
      <img src='/images/u2car.png' alt="U2CAR Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>Dual Uncertainty-aware Correspondence Adapting and Retaining for Continual Composed Image Retrieval</h3>
      <div class="authors"><span class="primary-gradient-text">Haoliang Zhou</span>⭐️, Feifei Zhang, Changsheng Xu</div>
      <div class="venue">IEEE Transactions on Image Processing (TIP 2025), SCI, 中科院一区, IF=13.7, CCF-A</div>
      <div class="links">
        <a href="https://doi.org/10.1109/TIP.2025.3628454" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <a href="https://github.com/HaoliangZhou/U2CAR" class="btn-accent"><i class="fab fa-github"></i> Code</a>
      </div>
    </div>
  </div>

  <div class='paper-box floating-card' data-tags="Micro Expression Recognition, 中科院二区">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">NEUCOM 2025</div>
      <img src='/images/psn.png' alt="PSN Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>PSN: Parallel Spatiotemporal Network to Recognize Micro-Expression</h3>
      <div class="authors">Jingting Li, Sujing Wang, Yong Wang, <span class="primary-gradient-text">Haoliang Zhou</span>, Xiaolan Fu</div>
      <div class="venue">Neurocomputing (2025), SCI, 中科院二区, IF=6.5</div>
      <div class="links">
        <a href="https://doi.org/10.1016/j.neucom.2025.129891" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <!-- <a href="https://" class="btn-accent"><i class="fab fa-github"></i> Code</a> -->
      </div>
    </div>
  </div>
  
  <div class='paper-box floating-card' data-tags="第一作者, Facial Expression Recognition, Transfer Learning, 中科院一区">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">IEEE TCSVT 2024</div>
      <img src='/images/ceprompt.png' alt="CEPrompt Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>CEPrompt: Cross-Modal Emotion-Aware Prompting for Facial Expression Recognition</h3>
      <div class="authors"><span class="primary-gradient-text">Haoliang Zhou</span>⭐️, Shucheng Huang, Feifei Zhang, Changsheng Xu</div>
      <div class="venue">IEEE Transactions on Circuits and Systems for Video Technology (TCSVT 2024), SCI, 中科院一区, IF=11.1, CCF-B</div>
      <div class="links">
        <a href="https://doi.org/10.1109/TCSVT.2024.3424777" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <a href="https://github.com/HaoliangZhou/CEPrompt" class="btn-accent"><i class="fab fa-github"></i> Code</a>
      </div>
    </div>
  </div>
  
  <div class='paper-box floating-card' data-tags="第一作者, Facial Expression Recognition, Evidential Deep Learning, 中科院二区">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">NEUCOM 2024</div>
      <img src='/images/uafer.png' alt="UAFER Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>UA-FER: Uncertainty-aware Representation Learning for Facial Expression Recognition</h3>
      <div class="authors"><span class="primary-gradient-text">Haoliang Zhou</span>⭐️, Shucheng Huang, Yuqiao Xu</div>
      <div class="venue">Neurocomputing (2024), SCI, 中科院二区, IF=6.5</div>
      <div class="links">
        <a href="https://doi.org/10.1016/j.neucom.2024.129261" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <a href="https://github.com/HaoliangZhou/UAFER" class="btn-accent"><i class="fab fa-github"></i> Code</a>
      </div>
    </div>
  </div>

  <div class='paper-box floating-card' data-tags="Micro Expression Recognition, Self-supervised Learning, 中科院二区">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">NEUCOM 2024</div>
      <img src='/images/dvscl.png' alt="DVSCL Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>Micro-Expression Recognition using Dual-View Self-Supervised Contrastive Learning with Intensity Perception</h3>
      <div class="authors">Jingting Li, <span class="primary-gradient-text">Haoliang Zhou</span>, Yu Qian, Zizhao Dong, Sujing Wang</div>
      <div class="venue">Neurocomputing (2024), SCI, 中科院二区, IF=6.5</div>
      <div class="links">
        <a href="https://doi.org/10.1016/j.neucom.2024.129142" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <a href="https://github.com/MELABIPCAS/DVSCL" class="btn-accent"><i class="fab fa-github"></i> Code</a>
      </div>
    </div>
  </div>


  <div class='paper-box floating-card' data-tags="Continual Learning, Few-shot Learning">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">MMSJ 2024</div>
      <img src='images/caclip.png' alt="INCEPTR Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>CA-CLIP: Category-aware Adaptation of CLIP Model for Few-Shot Class-Incremental Learning</h3>
      <div class="authors">Yuqiao Xu, <span class="primary-gradient-text">Haoliang Zhou</span>⭐️, Shucheng Huang</div>
      <div class="venue">Multimedia Systems (2024), SCI, 中科院三区, IF=3.5</div>
      <div class="links">
        <a href="https://link.springer.com/article/10.1007/s00530-024-01322-y" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <!-- <a href="https://" class="btn-accent"><i class="fab fa-github"></i> Code</a> -->
      </div>
    </div>
  </div>
  
  <div class='paper-box floating-card' data-tags="第一作者, Micro Expression Recognition">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">MMSJ 2023</div>
      <img src='images/inceptr.png' alt="INCEPTR Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>IncepTR: Micro-Expression Recognition Integrating Inception-CBAM and Vision Transformer</h3>
      <div class="authors"><span class="primary-gradient-text">Haoliang Zhou</span>⭐️, Shucheng Huang, Yuqiao Xu</div>
      <div class="venue">Multimedia Systems (2023), SCI, 中科院三区, IF=3.5</div>
      <div class="links">
        <a href="https://doi.org/10.1007/s00530-023-01164-0" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <a href="https://github.com/HaoliangZhou/IncepTR" class="btn-accent"><i class="fab fa-github"></i> Code</a>
      </div>
    </div>
  </div>
  
  <div class='paper-box floating-card' data-tags="第一作者, Micro Expression Recognition">
    <div class='paper-box-image'>
      <div class="badge pulse-accent">Entropy 2023</div>
      <img src='images/dualatme.png' alt="DUALATME Overview" width="100%">
    </div>
    <div class='paper-box-text'>
      <h3>Dual-ATME: Dual-branch Attention Network for Micro-Expression Recognition</h3>
      <div class="authors"><span class="primary-gradient-text">Haoliang Zhou</span>⭐️, Shucheng Huang, Jingting Li, Sujing Wang</div>
      <div class="venue">Entropy (2023), SCI, 中科院三区, IF=2.1</div>
      <div class="links">
        <a href="https://doi.org/10.3390/e25030460" class="btn-accent"><i class="fas fa-file-alt"></i> Paper</a>
        <a href="https://github.com/HaoliangZhou/Dual-ATME" class="btn-accent"><i class="fab fa-github"></i> Code</a>
      </div>
    </div>
  </div>
</div>


<span class='anchor' id='-educations'></span>
# 🏫 教育经历
- *2024.09 - 至今*, 博士研究生 天津理工大学
  - **院系专业**: 计算机科学与工程学院, 计算机科学与技术
  - **指导老师**: <a href="https://ia.cas.cn/rcdw/jcqn/202404/t20240422_7129942.html" class="link-accent">徐常胜</a>研究员 (国家杰青, IEEE/IAPR/CCF/CSIG Fellow), <a href="https://cs.tjut.edu.cn/info/1226/1795.htm" class="link-accent">张飞飞</a>教授 (青拔, 天津市杰青)
  - **荣誉称号**: 入选中国科协青年科技人才培育工程博士生专项计划, 一等学业奖学金
- *2021.09 - 2024.06*, 硕士 江苏科技大学
  - **院系专业**: 计算机学院, 软件工程
  - **指导老师**: <a href="https://mypage.just.edu.cn/jsjkxgc/hsc/list.htm" class="link-accent">黄树成</a>教授
  - **专业排名**: 1/12; **课程绩点**: 4.1/5.0
  - **荣誉称号**: 研究生国家奖学金 (Top 3%)、一等奖学业学金 (连续3年)、优秀硕士学位论文、优秀毕业生 (Top 3%)、优秀研究生标兵 (Top 1.5%)等10余项荣誉称号
  - **比赛获奖**: 第四届江苏省研究生数学建模科研创新实践大赛省三等奖、第七届中国高校计算机大赛-网络技术挑战赛华东赛区三等奖、江苏科技大学研究生数学建模大赛一等奖
- *2018.09 - 2019.01*, 访问学生 加州州立大学圣贝纳迪诺分校
  - **院系专业**: 商业与公共管理学院, 管理信息系统
  - **课程绩点**: 3.9/4.0 (均获A级)
- *2017.09 - 2021.06*, 学士 江苏科技大学
  - **院系专业**: 经济管理学院, 信息管理与信息系统
  - **专业排名**: 5/72
  - **荣誉称号**: 优秀毕业生 (Top 3%)、一等奖学业学金、三好学生、优秀学生干部等10余项荣誉称号
  - **比赛获奖**: 江苏省大学生创新创业训练计划省级结题 (No. 201910289051Y)、“创青春-启航杯”创业设计大赛三等奖


<span class='anchor' id='-awards'></span>
# 🏆 荣誉称号
- *2025.12 - 2027.12*: <span class="primary-gradient-text">中国科协青年科技人才培育工程博士生专项计划</span>
- *2024.12*  天津理工大学研究生一等学业奖学金
- *2024.06*  江苏科技大学优秀硕士学位论文, 研究生优秀毕业生 (Top 3%), 一等学业奖学金
- *2023.12*  <span class="primary-gradient-text">硕士研究生国家奖学金</span> (Top 3%)
- *2023.10*  江苏科技大学优秀研究生标兵 (Top 1.5%), 一等学业奖学金
- *2022.10*  第四届江苏省研究生数学建模科研创新实践大赛省三等奖
- *2022.10*  第七届中国高校计算机大赛-网络技术挑战赛华东赛区三等奖
- *2021.06*  江苏科技大学优秀毕业生 (Top 3%), 一等学业奖学金



<span class='anchor' id='-interships'></span>
# 💼 研究经历
- *2024.09-至今*, 中国科学院自动化研究所 多模态人工智能系统全国重点实验室 <a href="https://nlpr-web.ia.ac.cn/mmc/index.html" class="link-accent">多媒体计算组 (MMC)</a>, 客座学生（实习）
  - **研究方向**: 跨模态图文检索, 多模态大语言模型, 测试时自适应, 持续学习等
  - **合作导师**: <a href="https://ia.cas.cn/rcdw/jcqn/202404/t20240422_7129942.html" class="link-accent">徐常胜</a>研究员 (国家杰青, IEEE/IAPR/CCF/CSIG Fellow), <a href="https://cs.tjut.edu.cn/info/1226/1795.htm" class="link-accent">张飞飞</a>教授 (青拔, 天津市杰青)
- *2023.03-2024.06*, 天津理工大学 <a href="https://i-mac-lab.net/" class="link-accent">智能媒体分析与计算实验室 (IMAC Lab)</a>, 客座学生（实习）
  - **研究方向**: 人脸表情识别, 视觉语言模型, 多媒体计算
  - **合作导师**: <a href="https://ia.cas.cn/rcdw/jcqn/202404/t20240422_7129942.html" class="link-accent">徐常胜</a>研究员 (国家杰青, IEEE/IAPR/CCF/CSIG Fellow), <a href="https://cs.tjut.edu.cn/info/1226/1795.htm" class="link-accent">张飞飞</a>教授 (青拔, 天津市杰青)
- *2021.07-2023.03*, 中国科学院心理研究所 <a href="http://melab.psych.ac.cn/index.html" class="link-accent">微表情应用研究中心 (MELAB)</a>, 客座学生（实习）
  - **研究方向**: 微表情识别, 对比学习, 自监督学习
  - **合作导师**: <a href="https://psych.cas.cn/sourcedb/cn/expert/201704/t20170411_6369874.html" class="link-accent">王甦菁</a>副研究员, <a href="https://psych.cas.cn/sourcedb/cn/expert/202209/t20220905_6508737.html" class="link-accent">李婧婷</a>副研究员



<span class='anchor' id='-services'></span>
# 👓 学术活动
- **期刊审稿人**: IEEE TPAMI/TCSVT/TMM, MMSJ, SPIC, AJSE, SIVP
- **会议审稿人**: IEEE CVPR/ICCV/ICME, AAAI, ACM MM, ChinaMM
- **邀请汇报**: <a href="https://www.koushare.com/live/details/49962" class="link-accent">中国图象图形学学会(CSIG)第20期学生会员分享论坛</a>



<span class='anchor' id='-interests'></span>
# 📰 项目经历
- *2024.01-2027.12*, 国家自然科学基金面上项目, 参与
  - **项目名称**: 面向跨媒体查询的增量检索研究（在研）
  - **项目简介**: 主要研究跨媒体内容生成完备化、跨媒体语义融合透明化以及跨媒体关联推理持续化三个关键问题, 从数据层、分析层和推理层三个层面, 系统研究面向跨媒体查询的增量检索方法。 围绕跨媒体检索相关领域, 多篇成果发表在SCI/CCF高水平学术期刊上, 推动领域研究进展。
- *2023.01-2026.12*, 国家自然科学基金面上项目, 技术骨干
  - **项目名称**: 基于鲁棒表观建模的行人检测方法研究（在研）
  - **项目简介**: 主要研究复杂场景下的行人检测算法, 例如: 单域中遮挡严重导致大量误检和漏检问题；跨域检测中存在模型泛化性能差的问题；增量检测中存在灾难性遗忘的问题。相关成果发表在SCI/CCF高水平学术期刊上, 推动领域研究进展。
- *2022.03-2023.03*, 江苏省研究生科研创新计划项目, 项目负责人
  - **项目名称**: 基于视觉自注意网络与跨模态特征融合的微表情识别 (已结项)
  - **项目简介**: 以跨种族、跨数据库的多场景微表情视频帧为研究对象, 研究自注意力机制和深度信息对提高微表情识别的显著性, 改进视觉Transformer模型, 设计出适用于多种微表情数据库的微表情识别通用模型。围绕人脸表情、微表情识别等情感计算相关领域, 已发表SCI/CCF学术论文5篇, 公开发明专利2项。
- *2018.01-2021.12*, 国家自然科学基金面上项目, 技术骨干
  - **项目名称**: 基于鲁棒表观建模的目标跟踪方法研究（已结项）
  - **项目简介**: 主要研究复杂场景下的目标跟踪算法, 提出了一种基于条件随机场的鲁棒性深度相关滤波目标跟踪算法；此外还对视频中的关键部分(精彩片段)和视频时序定位等问题进行相关研究。相关成果发表在SCI/CCF高水平学术期刊上, 推动领域研究进展。
- *2019.01-2020.1*, 江苏省大学生创新创业训练计划省级重点项目, 第二完成人
  - **项目名称**: 基于mvc的大学生就业软件设计与开发（已结项）
  - **项目简介**: 针对大学生日益严峻的就业问题, 开发一款专门面向毕业生的就业小程序, 以缓解其就业压力。主要负责数据库设计开发和前端开发工作; 撰写软件各类开发文档, 共计10万余字。


<span class='anchor' id='-visitor'></span>
# 📣 学生工作
- 班级班长（2021-2024）
- 研究生会组织部部长（2021-2022）
- 学生会科技部部长（2018-2019）
- 班级团支书（2017-2021）

<span class='anchor' id='-visitor'></span>
# 🔧 专业能力
- 编程语言：Python, Pytorch
- 专业工具：Latex, Matlab, Linux


<span class='anchor' id='-visitor'></span>
# 🗺️ 访客地图
<script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=55a2e5&w=100&t=tt&d=q0lMQbv42GO9Uz2DKyDiIher0PBDh8IwLw2ozMawjng&co=ffffff&cmo=0c8759&cmn=e5153d&ct=979bad'></script>


<script>
document.addEventListener('DOMContentLoaded', function() {
  const wrapper = document.getElementById('publications-wrapper');
  if (!wrapper) return;

  const filterContainer = document.getElementById('filter-container');
  const paperBoxes = wrapper.querySelectorAll('.paper-box');
  
  let tagCounts = {}; 
  let activeTags = new Set();

  // 1. 定义白名单
  const visibleTagsWhitelist = [
    "CCF-A", 
    "中科院一区", 
    "第一作者", 
    "Composed Image Retrieval", 
    "Continual Learning", 
    "Facial Expression Recognition", 
    "Micro Expression Recognition"
  ];

  // 初始化：生成标签并统计数量
  paperBoxes.forEach(box => {
    const tagsAttribute = box.getAttribute('data-tags');
    if (tagsAttribute) {
      // 统一使用 tagsList 变量名
      const tagsList = tagsAttribute.split(',').map(t => t.trim()).filter(t => t);
      
      // --- 渲染卡片内部标签 (仅限白名单) ---
      const textContainer = box.querySelector('.paper-box-text');
      const linksContainer = box.querySelector('.links');
      
      if (textContainer && !textContainer.querySelector('.badge-container')) {
        const badgeContainer = document.createElement('div');
        badgeContainer.className = 'badge-container';
        
        tagsList
          .filter(tag => visibleTagsWhitelist.includes(tag)) 
          .forEach(tag => {
            const badge = document.createElement('span');
            badge.className = 'inner-tag-badge';
            badge.textContent = tag;
            badgeContainer.appendChild(badge);
          });
        
        if (linksContainer) {
          textContainer.insertBefore(badgeContainer, linksContainer);
        } else {
          textContainer.appendChild(badgeContainer);
        }
      }

      // --- 统计逻辑：只统计白名单内的标签用于生成顶部按钮 ---
      tagsList.forEach(tag => {
        if (visibleTagsWhitelist.includes(tag)) {
          tagCounts[tag] = (tagCounts[tag] || 0) + 1;
        }
      });
    }
  });

  // 2. 生成顶部过滤按钮
  const sortedTags = Object.keys(tagCounts).sort();
  if (filterContainer) {
    filterContainer.innerHTML = ''; 
    sortedTags.forEach(tag => {
      const btn = document.createElement('button');
      btn.className = 'filter-btn';
      btn.textContent = `${tag} (${tagCounts[tag]})`;
      
      btn.onclick = () => {
        if (activeTags.has(tag)) {
          activeTags.delete(tag);
          btn.classList.remove('active');
        } else {
          activeTags.add(tag);
          btn.classList.add('active');
        }
        filterPapers(); 
      };
      
      filterContainer.appendChild(btn);
    });
  }

  // 3. 核心逻辑：过滤论文 + 高亮标签
  function filterPapers() {
    paperBoxes.forEach(box => {
      const boxTagsString = box.getAttribute('data-tags');
      const boxTags = boxTagsString ? boxTagsString.split(',').map(t => t.trim()) : [];
      
      let isVisible = true;
      if (activeTags.size > 0) {
        if (boxTags.length === 0) {
          isVisible = false;
        } else {
          // AND 逻辑：必须包含所有选中的标签
          isVisible = Array.from(activeTags).every(activeTag => boxTags.includes(activeTag));
        }
      }

      box.classList.toggle('hidden', !isVisible);

      // 处理内部标签的高亮
      const innerBadges = box.querySelectorAll('.inner-tag-badge');
      innerBadges.forEach(badge => {
        badge.classList.toggle('active', activeTags.has(badge.textContent));
      });
    });
  }
});
</script>
