# opensw23-KLKB

## Team Introduction
김영록 202011269 Role: Leader <br />
이주혁 202011347 Role: Sample Data Research <br />
김현민 202211289 Role: Presenter <br />
배찬우 201914303 Role: Find Repository <br />

## Topic Introduction

## Results

## Analysis/Visualization

## Installation
오픈 소스 repo 설치 및 실행 방법

### 1. 설치  
위 사이트 접속  
- https://github.com/williamcfrancis/CNN-Image-Colorization-Pytorch.git  

되도록 이면 가상환경을 만들어 거기에 clone하는 것을 추천한다.  

가상환경이 있는 위치에 다음 git명령어를 사용하여 clone해준다.  
git clone https://github.com/williamcfrancis/CNN-Image-Colorization-Pytorch.git  
![image01](https://github.com/chanubc/opensw23-KLKB/assets/106955456/43be217b-19f9-4025-ab66-776f5452950a)  

https://drive.google.com/file/d/15jprd8VTdtIQeEtQj6wbRx6seM8j0Rx5/view?usp=sharing  
다음 링크에 접속하여 데이터 셋을 다운받는다.  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/a90e9b09-e9af-4518-bc3d-09b52db87221)  
  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/fd4d0730-bf01-4723-a07e-4aa0d3aa17bc)

압축을 푼 위치 train_landscape_images라는 폴더가 생겼음을 알 수 있다.  
  
  
이제 설치는 끝났고 실행시키기 위해 개발환경을 설정해줄 차례이다.  

### 2. 개발환경 설정  
  
CUDA 다운  
  
shift + ctrl + esc 버튼을 눌러 작업 관리자를 실행한 후 성능 탭에 접속  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/611283d5-7387-418b-9498-436b7aea9704)  
  
GPU메뉴에 접근하여 내 pc가 어떤 그래픽 카드를 쓰고 있는지 확인  
(필자는 NVIDIA GeForce GTX 1060을 쓰고 있음을 알 수 있다.)  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/8b6a7076-934f-45b7-8282-e0cc7b41798f)  
  
  
<NVIDIA Driver사이트 접속>  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/44bb883b-6d56-4c81-b658-5bfa3adb3466)  
  
  
아까 작업관리자에서 확인했던 그래픽 카드 정보를 바탕으로 해당 product Series와 Product를 선택한 뒤에 Search를 누르고 Driver를 다운/설치를 한다.  
  
<적절한 CUDA버전 확인>  
cmd창을 열어서  
cd C:\Program Files\NVIDIA Corporation\NVSMI 명령어를 실행한 뒤에  
nvidia-smi.exe 명령어 실행  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/39cde8b8-39e6-4fbf-b334-5789b1339327)  
  
  
그러면 다음과 같은 표를 얻을 수 있고 우측 상단에 CUDA Version을 확인할 수 있다.  
(필자의 경우엔 10.2라고 나온다.)  
위 버전을 잘 기억해 두자  

<CUDA toolkit설치>  
  
https://developer.nvidia.com/cuda-toolkit-archive  
다음 사이트에 접속하여 표에서 얻은 CUDA Version과 같은 것을 다운 받는다,  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/41272cad-71c6-4281-94ae-a8854e68dc6d)  
  
이제 다시 cmd창을 활용하여 클론 했던 가상환경 위치로 다시 돌아간다.    
  
<라이브러리 설치>  
https://pytorch.org/get-started/previous-versions/  

위 사이트를 참고 하여 본인 CUDA버전과 맞는 pytorch, torchvision, torchaudio 라이브러리를 설치한다.  
![image](https://github.com/chanubc/opensw23-KLKB/assets/106955456/4394548b-2d1a-4700-9896-73023549d09d)  
위와 같은 방식으로 사이트에 있는 명령어를 복사하여 사용하면 된다.  

## Presentation
