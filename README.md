# opensw23-KLKB

## Team Introduction
김영록 202011269 Role: Leader <br />
이주혁 202011347 Role: Sample Data Research <br />
김현민 202211289 Role: Presenter <br />
배찬우 201914303 Role: Find Repository <br />

## Topic Introduction
https://github.com/williamcfrancis/CNN-Image-Colorization-Pytorch Repository에서 가져와 사용함.  
이 Repository의 인공지능은 그레이 스케일 이미지가 입력값으로 들어왔을 때, 학습된 모델을 통하여 그레이 스케일 이미지를 자동으로 색칠하여 256x256 크기의 이미지로 출력하는 딥러닝 모델이다.      

## Analysis/Visualization

## Installation
오픈 소스 repo 설치 및 실행 방법  
되도록이면 가상환경을 만들어 거기에 clone하는 것을 추천한다.  
가상환경이 있는 위치에 다음 git명령어를 사용하여 clone해준다.  
git clone https://github.com/chanubc/opensw23-KLKB  

![image01](https://github.com/chanubc/opensw23-KLKB/assets/106955456/43be217b-19f9-4025-ab66-776f5452950a)  

CNN-Image-Colorization-Pytorch 폴더에 들어간다.  
inference 폴더에 들어가 사용하고 싶은 이미지를 넣는다.  
cmd창을 켜서 가상환경을 실행시킨 뒤에 inference_script.py 가 있는 위치로 이동한 뒤에 다음 명령어를 실행한다.
inference_script.py --model_path models/saved_model.pth --image_path inference/[이미지 이름]
![cmd로 inference실행방법](https://github.com/chanubc/opensw23-KLKB/assets/127182406/7354c0ca-4625-4b63-b0c6-41447066366f)  


![inference](https://github.com/chanubc/opensw23-KLKB/assets/127182406/179b974e-c4c9-4055-976a-3a4643f463ef)  

inference폴더로 이동하면 변환된 이미지 inference_output.jpg를 볼 수 있다.

![output이미지](https://github.com/chanubc/opensw23-KLKB/assets/127182406/05a98fc3-e1de-4ab6-8dec-45b618f1b831)  

## Results  
<인풋이미지>  
![test](https://github.com/chanubc/opensw23-KLKB/assets/127182406/a65ab306-fe69-4850-8016-40bd9333a64e)  

<아웃풋 이미지>  
![inference_output](https://github.com/chanubc/opensw23-KLKB/assets/127182406/e9e76841-e94f-4ea4-9eb5-5be3ef196570)    
  

## Presentation

