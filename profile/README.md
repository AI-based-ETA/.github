## 프로젝트 소개 👋

기존의 길찾기 시스템은 ``예측(prediction)``이 아닌 ``추론(estimation)``입니다. 단순히 과거의 비슷한 시간대의 유사한 이력 자료를 가져올 뿐이다. 이는 실제 걸리는 ETA(Estimated Time of Arrival)와 차이가 있습니다.

따라서 저희는 한국도로공사에서 제공하는 차량감지장치(VDS)로 학습한 Deep Learning 모델과 A*알고리즘을 사용하여, ``미래 상황을 예측``하고 개선된 ``ETA``를 계산하려 한다

## 프로젝트 아키텍처

![아키텍처](https://github.com/AI-based-ETA/.github/assets/65798779/d7fb4559-270e-42e2-9b43-e034fdf5145b)

## 프로젝트 구현

### [GCP Server](https://github.com/AI-based-ETA/GCP-Server)
1. Front-End의 ``출발지, 도착지, 출발시각``을 요청을 받는다.
2. 인공지능은 출발시각 1시간 전 데이터을 기반으로 미래의 1시간을 추론한다.
3. A* 알고리즘의 연산을 통해 최단 시간 ETA와 경로를 반환한다. 이때, 경과 시간이 앞서 인공지능이 추론한 시간을 초과할 경우 다시 2번으로 돌아간다.

### [Front-End](https://github.com/AI-based-ETA/Capstone_Kakaomap)
1. React를 사용한 UI
2. Flask와 GCP를 사용한 인공지능 연계 및 데이터 송수신
3. Kakao API를 사용한 Map 구현 및 경로 표시

### [Data preparation](https://github.com/AI-based-ETA/Preprocessing)
1. LightGBM을 사용한 결측 데이터 보완(예측 방법)
2. 교통량 비율에 따른 데이터 비율 가중 평균 변환
3. 인공지능이 사용할 수 있도록 데이터 형식 변환

### [AI model](https://github.com/AI-based-ETA/pretrained_AI_Model/tree/main)
1. Graph-WaveNet 모델에 대한 설명
2. Epoch 마다 평균 학습 시간과 추론 시간
3. 학습 성능과 추론 성능

## 시연

<img width="720" alt="1" src="https://github.com/AI-based-ETA/.github/assets/65798779/c7e51af5-dfc3-4f5e-abf0-5602a7f5ec6e">

(1) 경로 요청 및 인공지능 추론

<img width="720" alt="2" src="https://github.com/AI-based-ETA/.github/assets/65798779/8b8ee40c-cfd8-4799-9413-949df2f95b37">

(2) 경로 시각화 및 ETA 도출

## 팀원 소개

| 이름 | 역할 | GitHub 프로필 | 이메일 |
|------|------|----------------|--------|
| 김상원 | 프로젝트 매니저, 인공지능 학습 및 배포 | [GitHub](https://github.com/daydream-er) | borntocde@naver.com |
| 윤태형 | 프론트엔드 개발자, React 및 Flask | [GitHub](https://github.com/YunTaeng) | howard9166@naver.com |
| 최우석 | 백엔드 개발자, 서버 운용 및 관리 | [GitHub](https://github.com/ddakgi00) | ddakgi00@naver.com |
| 강주현 | 프론트엔드 개발자, React 및 경로 탐색 | [GitHub](https://github.com/juhyunk0820) | juhyunk0820@naver.com |
