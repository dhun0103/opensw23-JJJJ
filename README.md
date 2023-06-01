# Introduction

1. 정동훈

ID : 202111420

Role : Github Expert


2. 주지민

ID : 201911284

Role : Team Leader


3. 장동혁

ID : 201911276

Role : Presenter


4. 정제원

ID : 201713298

Role : Coder


# Topic introduction

선정 프로젝트:
https://github.com/FareedKhan-dev/yolov7-face-blur

선정한 프로젝트는 학습된 pytorch 모델을 이용하여 input으로 들어온 이미지나 비디오에서 사람의 얼굴을 detect하여 blur처리한 결과를 output으로 만드는 코드입니다.


# Results

## Sample Input&Output

All samples located in `.../opensw23-JJJJ/samples`

input model

    yolov7-lite-t.pt

input source 

    SmileFaces.jpg

Input Command

    python detect.py --weights yolov7-lite-t.pt --blurratio 50 --device cpu --source SmileFaces.jpg
    

### input

![SmileFaces_input](https://github.com/dhun0103/opensw23-JJJJ/assets/50978743/316a6a93-ccda-41f0-b094-aa77f23d9244)

### output

![SmileFaces_output](https://github.com/dhun0103/opensw23-JJJJ/assets/50978743/41b4a7f7-5a14-434a-a2ff-60ba2cf04352)


# Analysis/Visualization


# Installation
---

**Warning!** 

설치 경로에 한글이 포함되어 있다면 정상작동 하지 않으므로 영문으로만 된 경로를 설정하여 설치해주시기 바랍니다.

---
Original Introduction
---
### How to install
1. Create Virutal Environment of Python, Recommended python version `3.9.0`, incase you dont have `3.9.0`, see `pyenv` guide.
2. Activate the Environment using `python -m venv your_env_name/Scripts/activate`
3. install required libraries using `pip install -r requirements`
4. (Optional) If you want to use GPU, you have to install additional requirements i.e, `pip install -r requirements_gpu.txt` 

---

## Requirements

git(Updated)

pip(Updated)

python 3.9.X ( 원 프로젝트는 3.9.0을 요구하였음)

If you do not use pip, read 'requirements.txt' and install require packages.

## Setting Project

-----

### \*Option 
Create Virtual Environment of Python and Activate the Environment.

(Recommended, If you don’t want to disturb python packages)

    python3 -m venv yolov7objblurring

 and activate virtual environment
 
    call yolov7objblurring/Scripts/activate
    
-----

Clone this project

    git clone https://github.com/dhun0103/opensw23-JJJJ
    
and move to project Directory

    cd opensw23-JJJJ
      
Install requirements with mentioned command below

    pip install -r requirements.txt

##### Option

If you want to use GPU, you have to install additional requirements.

    pip install -r requirements_gpu.txt (To use GPU, Not Tested)


Prepare Model file from the table below. Click link in 'google' or 'baidu' column.

| Models           |  Test Size | Easy  | Medium | Hard  | FLOPs (B) @640 | Google | Baidu |
| -----------------| ---------- | ----- | ------ | ----- | -------------- | ------ | ----- |
| yolov7-lite-t    | 640        | 88.7  | 85.2   | 71.5  |  0.8           | [google](https://drive.google.com/file/d/1HNXd9EdS-BJ4dk7t1xJDFfr1JIHjd5yb/view?usp=sharing) | [gsmn](https://pan.baidu.com/s/1oxlJVveUgHUQs4UiR26aCw) |
| yolov7-lite-s    | 640        | 92.7  | 89.9   | 78.5  |  3.0           | [google](https://drive.google.com/file/d/1MIC5vD4zqRLF_uEZHzjW_f-G3TsfaOAf/view?usp=sharing) | [3sp4](https://pan.baidu.com/s/1f_DD1gZ1AUGLFKHoPNq10Q) |
| yolov7-tiny      | 640        | 94.7  | 92.6   | 82.1  |  13.2          | [google](https://drive.google.com/file/d/1Mona-I4PclJr5mjX1qb8dgDeMpYyBcwM/view?usp=sharing) | [aujs](https://pan.baidu.com/s/1IzHLQc2RbPyuDgEqgY8hUg) |
| yolov7s          | 640        | 94.8  | 93.1   | 85.2  |  16.8          | [google](https://drive.google.com/file/d/1_ZjnNF_JKHVlq41EgEqMoGE2TtQ3SYmZ/view?usp=sharing) | [w72z](https://pan.baidu.com/s/1fZfZTH7qSdN-0zTk5iCcnA) |
| yolov7           | 640        | 96.9  | 95.5   | 88.0  |  103.4         | [google](https://drive.google.com/file/d/1oIaGXFd4goyBvB1mYDK24GLof53H9ZYo/view?usp=sharing) | [jrj6](https://pan.baidu.com/s/1PiEnSaogvjkNvRLHctBz9A) |
| yolov7+TTA       | 640        | 97.2  | 95.8   | 87.7  |  103.4         | [google](https://drive.google.com/file/d/1oIaGXFd4goyBvB1mYDK24GLof53H9ZYo/view?usp=sharing) | [jrj6](https://pan.baidu.com/s/1PiEnSaogvjkNvRLHctBz9A) |
| yolov7-w6        | 960        | 96.4  | 95.0   | 88.3  |  89.0          | [google](https://drive.google.com/file/d/1U_kH7Xa_9-2RK2hnyvsyMLKdYB0h4MJS/view?usp=sharing) | - |
| yolov7-w6+TTA    | 1280       | 96.9  | 95.8   | 90.4  |  89.0          | [google](https://drive.google.com/file/d/1U_kH7Xa_9-2RK2hnyvsyMLKdYB0h4MJS/view?usp=sharing) | - |


## Running Project

Basic Command Format

    python detect.py --weights model.pt --blurratio 50 --hidedetarea --device cpu --source image.jpg

Explain Argument(Original & Korean Translate)
    
    --weights : contains your downloaded model from the above table
    위 테이블에서 다운로드한 모델을 입력합니다
   
    --bluurratio : to determine the strength of blurring, default value is 20
    얼마나 blur할 것인지 수치로 결정합니다. 기본값은 20입니다 (0~100)
    
    --hidedetarea
    만약 blur처리된 얼굴 부분의 테두리 표기를 원치 않는다면 이 옵션을 추가하여 입력합니다. 입력하지 않아도 되는 인자 입니다.
    
    --device : either cpu or 0 in case of gpu.
    cpu 또는 0을 입력하여 cpu나 gpu 사용을 결정합니다.
    
    --source : containes your images (png, jpg etc) or video (mp4 etc)
    이미지나 비디오를 입력합니다.
 
 
If you run the code, output may located in

    .../opensw23-JJJ/runs/detect/...


# Presentation
