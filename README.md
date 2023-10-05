# CCTV 영상 데이터를 이용한 무기, 화재, 이상 행동 탐지 시스템

- 제로베이스 데이터 스쿨 13기 2조 4인 팀 프로젝트
- 23.08.11 ~ 23.09.07

## 프로세스
![image](https://github.com/zoe-0314/DL_CCTV_project/assets/119393455/c91bc666-2512-4d60-920e-a762a6419b11)

## 담당 역할
### CASE 1-1 : 이상탐지 모델(RTFM)

- Model   
  - feature extraction : ResNet-50 활용된 I3D 모델   
  - train, test : ucf-crime 데이터셋을 활용한 anomaly detection sota 모델 중 RTFM을 사용   
<br>

- Dataset   
  - ucf-crime, Aihub 이상행동 CCTV   
  - 데이터 용량 및 소요시간을 고려하여 4개의 클래스로 진행   
  - 폭행, 싸움, 강도, 일반 (assault, fighting, robbery, normal)   
<br>

### 내용
- ucf-crime 데이터셋이 해외 영상으로 이루어져 있는 점을 고려하여 ucf-crime 데이터로만 훈련 시킨 경우와 한국형 cctv 영상 데이터인 이상행동 cctv데이터와 ucf-crime를 함께 훈련 시킨 경우 두 가지를 나눠 진행
- 따로 국내의 cctv 영상을 가지고 있지 않아, 모델링을 진행할 때 사용하지 않았던 cctv 영상으로 테스트를 진행.
- ucf-crime과 이상행동 cctv 영상을 이용한 경우에 ucf-crime 동영상만 이용한 경우의 accuracy보다는 약간 낮지만 테스트 영상 결과를 보았을 때에 조금 더 세밀한 예측 결과를 얻을 수 있었음.
- 동영상으로 확인했을 때 낮은 예측을 보여 아쉬운 점 존재
<br>

### 결과 동영상
링크 : https://drive.google.com/file/d/1zJwyGsuUBXEVzFZ_lO1Ki8L9UqvYSB-s/view?usp=sharing

<br>


### 관련 파일
- 관련 코드의 일부 파일만 업로드
<br>

### 참고 링크

- https://pypi.org/project/i3dFeatureExtraction/
- https://paperswithcode.com/paper/weakly-supervised-video-anomaly-detection
- https://github.com/tianyu0207/RTFM
- https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=realm&dataSetSn=171
- https://www.kaggle.com/datasets/odins0n/ucf-crime-dataset
