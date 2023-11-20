# Cross-Modal Emotion-Aware Prompting for Facial Expression Recognition
```Paper ID: 11311```

## Installation
```
pip install -r requirements.txt
```

## Preparation
1. Download pretrained VLP(ViT-B/16) model from [OpenAI CLIP](https://github.com/openai/CLIP).
2. Download images of  RAF-DB and AffectNet dataset.

2.1. The downloaded RAF-DB are reorganized as follow:
```
data/
├─ RAF-DB/
│  ├─ basic/
│  │  ├─ EmoLabel/
│  │  │  ├─ images.txt
│  │  │  ├─ image_class_labels.txt
│  │  │  ├─ train_test_split.txt
│  │  ├─ Image/
│  │  │  ├─ aligned/
│  │  │  ├─ aligned_224/  # reagliend by MTCNN
```
2.2. The downloaded AffectNet are reorganized as follow:

```
data/
├─ AffectNet/
│  ├─ affectnet_info/
│  │  ├─ images.txt
│  │  ├─ image_class_labels.txt
│  │  ├─ train_test_split.txt
│  ├─ Manually_Annotated_Images/
│  │  ├─ 1/
│  │  │  ├─ images
│  │  │  ├─ ...
│  │  ├─ 2/
```
2.3. The structure of three data-load and -split txt files are reorganized as follow:
```
(1) images.txt:
idx | imagename
1 train_00001.jpg
2 train_00002.jpg
.
15339 test_3068.jpg

(2) image_class_labels.txt:
idx | label
1 5
2 5
.
15339 7

(3) train_test_split.txt:
idx | train(1) or test(0)
1 1
2 1
.
15339 0
```

## Training
### First stage
```
python3 train_fer_first_stage.py \  
--dataset ${DATASET} \  
--data-path ${DATAPATH}
```
### Second stage
```
python3 train_fer_second_stage.py \  
--dataset ${DATASET} \  
--data-path ${DATAPATH} \  
--ckpt-path ${CKPTPATH}
```

## Evaluation
```
python3 train_fer_second_stage.py \ 
--eval \
--dataset ${DATASET} \  
--data-path ${DATAPATH} \  
--ckpt-path ${CKPTPATH} \  
--eval-ckpt ${EVACKPTPATH}
```