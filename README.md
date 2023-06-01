# opensw23-KLKB

## Team Introduction
김영록 202011269 Role: Leader <br />
이주혁 202011347 Role: Sample Data Research <br />
김현민 202211289 Role: Presenter <br />
배찬우 201914303 Role: Find Repository <br />

## Topic Introduction
https://github.com/williamcfrancis/CNN-Image-Colorization-Pytorch Repository에서 가져와 사용함.  
이 Repository의 인공지능은 색이 들어가 있는 여러 이미지들을 그레이 스케일화 시켜, 원본 이미지와 그레이 스케일로 변환된 이미지를 서로 비교해가며 이미지의 색을 자동으로 입힐 수 있게 되도록 학습하는 인공지능이다.  
해당 Repository는 인공지능의 학습을 위한 소스 코드와 이미지 파일들을 제공하며, 이 이미지들을 통하여 먼저 학습을 끝내면, 다른 소스 코드를 사용하여 색칠을 진행한다.  
Repository에서 제공하는 인공지능이 학습할 때 따뜻한 색상 또는 차가운 색상 위주로 학습하도록 특정 값을 넣어 조절하는 기능을 사용할 수 있다. 사용자가 어떤 값을 넣으냐에 따라 이 후 나오게 될 결과값에 변형을 줄 수 있다.  
학습이 끝나면 사용자는 결과를 확인하기 위해 학습에 사용되었던 이미지나 학습에 사용되지 않았던 새로운 그레이 스케일 이미지를 인공지능이 색칠하게 할 수 있다.  

## Results

## Analysis/Visualization

## Installation
오픈 소스 repo 설치 및 실행 방법  
되도록이면 가상환경을 만들어 거기에 clone하는 것을 추천한다.  
가상환경이 있는 위치에 다음 git명령어를 사용하여 clone해준다.  
git clone https://github.com/chanubc/opensw23-KLKB  

![image01](https://github.com/chanubc/opensw23-KLKB/assets/106955456/43be217b-19f9-4025-ab66-776f5452950a)  

CNN-Image-Colorization-Pytorch 폴더에 들어간다.  
inference 폴더에 들어가 사용하고 싶은 이미지의 이름과 확장자를 test_img.jpg로 설정하여 넣는다.  
cmd창을 켜서 가상환경을 실행시킨 뒤에 inference_script.py 가 있는 위치로 이동한 뒤에 다음 명령어를 실행한다.
inference_script.py --model_path [모델이 있는 위치] --image_path [변환할 이미지가 있는 위치]


![inference](https://github.com/chanubc/opensw23-KLKB/assets/127182406/179b974e-c4c9-4055-976a-3a4643f463ef)  



## Presentation
