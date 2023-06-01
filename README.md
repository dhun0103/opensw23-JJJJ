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

선정한 프로젝트는 학습된 pytorch 모델을 이용하여 input으로 들어온 이미지나 비디오의에서 얼굴을 detect하여 blur처리 한 결과를 output으로 만드는 코드입니다.


# Results


# Analysis/Visualization


# Installation
---

**주의!** 
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

요구사항
---
git(Updated)

pip(Updated)

python 3.9.X ( 원 프로젝트는 3.9.0을 요구하였음)

\*기타 요구 패키지는 requirements.txt에 담겨 있음. pip를 이용하지 않는다면 참고하여 설치해주시면 됩니다.


## 설치방법

1. (Option) Create Virtual Environment of Python and Activate the Environment.

( Recommended, If you don’t want to disturb python packages)

python3 -m venv yolov7objblurring

call yolov7objblurring/Scripts/activate

2. Clone the repository.

git clone https://github.com/dhun0103/opensw23-JJJJ

cd opensw23-JJJJ

3. Install requirements with mentioned command below.

pip install -r requirements.txt

4. (Option) If you want to use GPU, you have to install additional requirements.

pip install -r requirements_gpu.txt (To use GPU, Not Tested)

5. 실행할 모델을 준비합니다. 아래 표는 출처 프로젝트에서 가져왔으며 사용 자체는 아무 모델을 사용하여도 상관 없습니다.

## 실행과정

기본 실행 명령어는 다음과 같습니다.

-----

python detect.py --weights selected_model.pt --blurratio 50 --device cpu --source your_image.jpg

-----

입력 인자(옵션) 설명
1. --weights : contains your downloaded model from the above table
2. --bluurratio : to determine the strength of blurring, default value is 20
3. --device : either cpu or 0 in case of gpu.
4. --source : containes your images (png, jpg etc) or video (mp4 etc)

Terminal 또는 bash가 해당 경로에 있도록 설정해줍니다

…/opensw23-JJJJ

아래 코드는 실행 예시 코드 입니다. model 로 yolov7-lite-t.pt를 사용하였으며 input image로 SmileFaces.jpeg를 사용하였습니다.

-----

python detect.py --weights yolov7-lite-t.pt --blurratio 50 --device cpu --source Smile
Faces.jpeg

-----

위 샘플 입력을 활용하였을때 다음과 같은 이미지 결과가 나옵니다. 결과는 프로젝트 내 run 폴더 내부에 저장됩니다.


# Presentation
