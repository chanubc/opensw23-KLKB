# opensw23-KLKB

## Team Introduction  
### 13조
김영록 202011269 Role: 조장, 설치방법 작성, 분석작업 <br />
이주혁 202011347 Role: 레포지토리 선정, 모델학습, 데이터 셋 제공 <br />
김현민 202211289 Role: 토의사항 작성, 데이터 셋 제공 <br />
배찬우 201914303 Role: 분석작업 보조, 발표영상녹화 <br />

## Topic Introduction
https://github.com/williamcfrancis/CNN-Image-Colorization-Pytorch Repository에서 가져와 사용함.  
이 Repository의 인공지능은 그레이 스케일 이미지가 입력값으로 들어왔을 때, 학습된 모델을 통하여 그레이 스케일 이미지를 자동으로 색칠하여 256x256 크기의 이미지로 출력하는 딥러닝 모델이다.      

## Installation
실행 조건: pc에 NVIDIA기종의 그래픽카드가 설치되어있어야 한다.  
### <오픈 소스 repo 설치 및 실행 방법>  
되도록이면 가상환경을 만들어 거기에 clone하는 것을 추천한다.  
#### <가상환경 구축방법>
![가상환경생성](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/20e937b6-f2d4-4a6d-9df1-5458c354219f)  
cmd창을 연뒤에 가상환경을 생성하고 싶은 파일 위치로 이동해서 다음과 같은 명령어를 입력해준다.  
virtualenv opensw   
(opensw는 가상환경이름이다. 필요하다만 다른 이름을 지정해서 사용해도 무관하다.)  
그런 뒤에 opensw\Scripts\activate 명령어를 입력해주어서 가상환경을 실행해준다.  

### <개발환경 구축>  
위 레포지토리를 실행하려면 cuda, torch, torchvision등 여러 모듈들의 설치가 필요하다.  
#### <설치>  
shift + ctrl + esc 버튼을 눌러 작업 관리자를 실행한 후 성능 탭에 접속  
![image](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/ff93a7e6-182e-4670-b55e-91c0e2853d70)  
GPU메뉴에 접근하여 내 pc가 어떤 그래픽 카드를 쓰고 있는지 확인  
(필자는 NVIDIA GeForce GTX 1060을 쓰고 있음을 알 수 있다.)  
#### <NVIDIA Driver 사이트 접속>  
![image](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/c5530677-0496-4e66-8e5a-94799e1c0afd)  
![image](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/6fa65bcf-eff9-4342-83ee-63a14331db3f)  
아까 작업관리자에서 확인했던 그래픽 카드 정보를 바탕으로 해당 product Series와 Product를 선택한 뒤에 Search를 누르고 Driver를 다운/설치를 한다.  
  
#### <적절한 CUDA버전 확인>  
cmd창을 열어서  
cd C:\Program Files\NVIDIA Corporation\NVSMI 명령어를 실행한 뒤에  
nvidia-smi.exe 명령어 실행  
![image](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/ed80560e-9095-4712-88d7-ba2652a16df9)  
그러면 다음과 같은 표를 얻을 수 있고 우측 상단에 CUDA Version을 확인할 수 있다.  
(필자의 경우엔 10.2라고 나온다.)  
위 버전을 잘 기억해 두자  
  
#### <CUDA toolkit설치>  
  
https://developer.nvidia.com/cuda-toolkit-archive  
다음 사이트에 접속하여 표에서 얻은 CUDA Version과 같은 것을 다운 받는다,  
![image](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/1eead272-d0b6-483f-a85a-a9ff89aa8d9c)  

이제 다시 cmd창을 활용하여 아까 생성했던 가상환경을 돌아가준다.  
  
#### <라이브러리 설치>  
https://pytorch.org/get-started/previous-versions/  
위 사이트를 참고 하여 본인 CUDA버전과 맞는 pytorch, torchvision, torchaudio 라이브러리를 설치한다.  
![파이토치 설치](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/a7f5dcc0-2a4a-41a6-be74-dd162809b322)  
  
![토치cuda호환](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/1d4f1fc9-c022-49fb-a15a-d7695123cfe1)  
위와 같이 명령어를 입력하여 설치한 토치와 cuda가 호환이 되는지 확인한다.  
사진과 같이 True가 뜨면 정상적으로 실행된다는 뜻이다.  
False가 뜨면 쿠다 버전과 호환이 되는 다른 토치버전을 설치하거나 cuda toolkit을 재설치하는걸 권장한다.  
  
다음은 Matplotlib이랑 scikit-image 그리고 CV2라이브러리를 다운/설치 한다.  
Matplotlib설치 명령어  
![mat설치](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/4a102dbc-4252-474b-a4e0-0dcb336fd1b4)  
pip install matplotlib  
  
scikit-image설치 명령어  
![사이킷](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/84407eef-9d55-4399-aa02-889cbb943374)  
pip install scikit-image  
  
CV2설치 명령어  
![cv2](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/097fbe2c-9c5e-455f-8ba4-077b9f9729bb)  
pip install opencv-python  
  
### <clone및 실행방법>  
가상환경이 있는 위치에 다음 git명령어를 사용하여 clone해준다.  
git clone https://github.com/chanubc/opensw23-KLKB  
![클론한 폴더](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/28c19659-040f-43fd-b4a0-98711f9e3207)  
클론한 폴더로 이동한다.   
inference 폴더에 들어가 사용하고 싶은 이미지를 넣는다.  
cmd창을 켜서 가상환경을 실행시킨 뒤에 inference_script.py 가 있는 위치로 이동한 뒤에 다음 명령어를 실행한다.
inference_script.py --model_path models/saved_model.pth --image_path inference/[이미지경로]
![inference_0608](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/f33b80c0-7973-47ce-85ad-0535b319cdae)  

![inference](https://github.com/chanubc/opensw23-KLKB/assets/127182406/179b974e-c4c9-4055-976a-3a4643f463ef)  

inference폴더로 이동하면 변환된 이미지 inference_output.jpg를 볼 수 있다.

![결과0608](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/37fab65a-6866-4bc3-b972-a7437baf6ab9)  
  
### <플로우 차트>  
아래의 차트는 위의 설치 방법을 간략하게 플로우차트로 나타낸 것입니다.  
![flowchat_ex](https://github.com/chanubc/chanubc.github.io/assets/106955456/047a706f-a95e-480e-9b80-fad7e9703be9)  
  
## Results  
저희는 총 60장의 직접 촬영한 사진을 사용해보았습니다.  
아래는 촬영한 사진들 중 대표적으로 3장을 골라 각 사진의 원본, 흑백화된 원본, 흑백화된 사진에 모델을 사용한 결과들입니다.<br>
원본 이미지 경로 : AnalysisImageSet/original/nature(자연)/20181030_163942.jpg<br>
흑백 이미지 경로 : AnalysisImageSet/bw_image_BlackImage/nature(자연)/bw_20181030_163942.jpg<br>
colorization 이미지 경로 : AnalysisImageSet/inference_ColorizationImage/nature(자연)/inference_output_20181030_163942.jpg<br>
![5](https://github.com/chanubc/opensw23-KLKB/assets/127182406/2798cc82-abb7-4a2c-8680-db3bc3841002)  
원본 이미지 경로 : AnalysisImageSet/original/nature(자연)/MyPhoto_1200850165_0677.jpg<br>
흑백 이미지 경로 : AnalysisImageSet/bw_image_BlackImage/nature(자연)/bw_MyPhoto_1200850165_0677.jpg<br>
colorization 이미지 경로 : AnalysisImageSet/inference_ColorizationImage/nature(자연)/inference_output_MyPhoto_1200850165_0677.jpg<br>
![8](https://github.com/chanubc/opensw23-KLKB/assets/127182406/5238b727-0e6a-4b21-8c5b-abf182626b01)  
원본 이미지 경로 : AnalysisImageSet/original/arc(건물)/IMG_1621.jpg<br>
흑백 이미지 경로 : AnalysisImageSet/bw_image_BlackImage/arc(건물)/bw_IMG_1621.jpg<br>
colorization 이미지 경로 : AnalysisImageSet/inference_ColorizationImage/arc(건물)/IMG_1621_output.jpg<br>
![3](https://github.com/chanubc/opensw23-KLKB/assets/127182406/3acf713f-b6c6-4d8c-a787-79c21336428e)   

  
## Analysis/Visualization
결과 분석 설명 전, 원본 Repository에는 모델이 주어지지 않아 직접 모델을 학습시켜 이 Repository에 추가시켰고,  
아래의 결과 분석은 해당 모델이 어떤 이미지들을 잘 colorization시키는지에 대하여 분석한 내용입니다.

### <분석방법>
1. 크기가 256*256인 원본 이미지를 준비한다.  
2. 원본 이미지를 흑백화 시킨다.
3. 흑백화 시킨 이미지를 colorization시킨다.  
4. colorization시킨 이미지와 원본 이미지의 각 픽셀간 RGB거리를 구한다.  
5. 그렇게 구한 RGB거리들을 모두 더해준다.  
6. 결과값을 이미지 카테고리별로 묶어서 서로 평균을 내어 이미지 카테고리별로 어떤 차이가 있는지 확인한다. (RGB거리가 짧을 수록 원본이미지와의 색상 차이가 없다는 것을 의미합니다.)  
  
분석방법이 이해가 잘 안되는 분도 있을 수 있어서 쉽게 예를 들어 보겠습니다.  
만약 크기가 2*2인 원본이미지와 그 이미지를 Colorization시킨 이미지가 있을 때 이 이미지들의 RGB거리 값은 다음과 같이 구합니다.  
  
![RGB거리예시](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/89beab22-3b2c-48c7-87e9-77d530836dd9)  

분석하는데 사용한 이미지들은 다음과 같습니다:  
1. 건물사진 55장 (인터넷에서 구한 건물사진 25장 + 저희가 찍은 사진 30장)  
2. 인물사진 55장 (인터넷에서 구한 인물사진 55장)  
3. 자연물사진 55장 (인터넷에서 구한 자연물 사진 25장 + 저희가 찍은 사진 30장)  

(분석을 더욱 자세히 하기 위하여 직접 찍은 사진들과 인터넷에서 사진을 구하여 같이 사용하였습니다.  
분석에 사용된 이미지는 모두 AnalysisImageSet 폴더에 저장되어 있습니다.)

이미지 카테고리별로 RGB거리의 평균값을 구해보았습니다.    
  
![카테고리별 평균 거리](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/920ef42a-83b1-4700-a0eb-ebf06bda72d9)  
  
차이를 눈에 잘 보이게 하기 위해 그래프로 나타내보았습니다.  
![카테고리별 평균 거리(그래프)](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/4ea4e25b-eaf4-4bff-b1c8-db7e698808bb)  
  
분석 결과 위 모델은 건물이미지를 다른 이미지보다 colorization을 잘 시키는데 반해, 인물이미지는 다른 이미지들보다 colorization을 잘 못시키고 있음을 알 수 있습니다.  
  
이번에는 분석한 카테고리별 이미지들을 다 합쳐서 RGB거리가 긴 이미지 10개, RGB거리가 짧은 이미지 10개를 뽑아보겠습니다.  
  
먼저 RGB거리가 짧은 이미지10개 즉 colorization이 다른 이미지에 비해 잘된 이미지들을 선정해보았습니다.
  
![1](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/1ed59dbc-f2f7-43f0-94a7-64d9265e8401)  
![2](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/bc2a977c-0dae-48fc-a095-8b555b5ad184)  
![3](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/6f8fa4c2-78bc-4333-ac03-291bf519cad2)  
![4](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/46f42178-8eba-49c6-878e-51e13cd286c9)  
![5](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/23f86a12-96d5-48f3-9c4b-e1a371f1cee8)  
![6](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/530592c6-10aa-4f05-b665-e829af046032)  
![7](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/9efc87ba-d729-404d-87f2-bd496ea639be)  
![8](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/f793d2c3-4c7c-41ce-9369-61b7b9548aa4)  
![9](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/d080d55b-506c-4620-bb86-a2d3e5acf8a1)  
![10](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/27c55d78-c1c5-47d2-9757-593a6b7b127f)  
  
이번에는 RGB거리가 긴 이미지 10개 즉 colorization이 다른 이미지에 비해 잘 안된 이미지들을 선정해보았습니다.  
  
![1](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/b5ae433c-9a2f-49b9-aacc-393318abad37)  
![2](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/dbe5329b-bf73-4e60-ad10-ba8c759f012d)  
![3](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/d2ab1a56-c432-4517-9e5a-d5ac83928758)  
![4](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/00047b7b-ea67-44d0-bd53-f1216f04a486)  
![5](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/aa780486-2bdc-4fb3-aec9-2df06cddcff4)  
![6](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/036577d0-049e-4b1a-9c7d-b75932489cdb)  
![7](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/30c522ae-3b4e-4f3b-bab4-89a64cd6a7b5)  
![8](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/1a36f4cc-2ada-4df3-a6c4-ad6c4fe69abb)  
![9](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/27397454-b3f2-4c5a-a1bc-2f9514fff1f1)  
![10](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/b70a9624-0551-427b-a0b9-f3d5080b66fd)  
  
  
colorization이 잘된 이미지와 잘 안된 이미지 각각 10개씩을 살펴본 결과 잘된 이미지는 전체적으로 검은색, 회색이 많이 들어간 느낌이고
colorization이 잘되지 않은 이미지들을 살펴본 결과 주로 갈색, 노란색이 많이 들어간 느낌이 들었습니다.  
  
그래서 저희는 추가적으로 위에서 선정한 이미지들의 평균 RGB값을 구해보았습니다.  
  
먼저 잘 된 이미지들의 평균 RGB값입니다.  
![잘된이미지표](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/7599c08f-bbf1-4a28-be11-574dcda5b4aa)
잘된 이미지들의 경우 R,G,B의 값 각각의 차이가 적은 것을 알 수 있고  
대다수의 이미지들에 검은색, 회색 계열의 색깔이 주로 들어가있음을 알 수 있습니다.  
  
이번에는 잘 안된 이미지들의 평균 RGB값을 보겠습니다.  
![잘안된이미지표](https://github.com/kimyeoungrok/openswAssignment_README/assets/127182406/93bac2d6-92f5-4268-b934-41008b3360b4)
잘 안된 이미지들의 경우 R,G,B의 값 각각의 차이가 큰 것을 알 수 있고    
대다수의 이미지에 노란색, 갈색 계열의 색깔이 주로 들어가있음을 알 수 있습니다.  
  
### <최종분석 결론>  
분석 결과 저희가 사용한 모델은 건물 카테고리의 이미지와 이미지 주요 색깔이 검은색, 회색 계열을 띄는 이미지를 colorization을 시키는데 있어서  
다른 이미지에 비해 높은 정확도를 나타냄을 알 수 있는 반면에,  
인물 카테고리의 이미지와 이미지 주요 색깔이 노란색, 갈색 계열을 띄는 이미지를 colorization시키는데 있어서  
다른 이미지에 비해 낮은 정확도를 나타냄을 알 수 있습니다.  
  
## Discussion
### <느낀 점>
1. 결과 이미지를 생성할 때 여러 이미지를 한번에 colorization을 하는 것이 불가능한데 여러 이미지를 한번에 colorization해주고 결과를 내주도록 변경되면 좋을 것 같음.  
2. 이미지를 넣고 돌릴 수 있는 확장자 형식이 고정되어 있어 불편함을 겪음. JPG형식만 읽을 수 있어 직접 찍은 HEIC형식의 사진을 사용하여 새로운 아웃풋을 만들 때 이미지 확장자 변환 프로그램을 사용하여 결과를 만들어냄.  
3. 결과 이미지를 생성할 때 이미지 파일이 256*256으로 고정되지 않고 inference단계에서 넣은 이미지 원본과 같은 크기의 픽셀로 출력 할 수 있으면 좋을것 같음.    
  
### <추가 사항>
원본 repository에서 학습한 모델을 제공하지 않아 직접 학습시킨 모델을 사용함. (모델 사용을 위해 train.py 코드 에러 수정)  
  
## Presentation
https://www.youtube.com/watch?v=UyAU0A370UY  
