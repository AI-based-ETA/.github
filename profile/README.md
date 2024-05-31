## Hi there 👋

안녕하세요.

세종대학교 컴퓨터공학과 캡스톤 프로젝트 ... 소개

## 프로젝트 아키텍처

![아키텍처](https://github.com/AI-based-ETA/.github/assets/65798779/d7fb4559-270e-42e2-9b43-e034fdf5145b)

## 프로젝트 구현

### [GCP Server](https://github.com/AI-based-ETA/GCP-Server)
1. Front-End의 ``출발지, 도착지, 출발시각``을 요청을 받는다.
2. 인공지능은 출발시각 1시간 전 데이터을 기반으로 미래의 1시간을 추론한다.
3. A* 알고리즘의 연산을 통해 최단 시간 ETA와 경로를 반환한다. 이때, 경과 시간이 앞서 인공지능이 추론한 시간을 초과할 경우 다시 2번으로 돌아간다.

### Front-End

### Data preparation

### [AI model](https://github.com/AI-based-ETA/pretrained_AI_Model/tree/main)
1. Graph-WaveNet 모델에 대한 설명
2. Epoch 마다 평균 학습 시간과 추론 시간
3. 학습 성능과 추론 성능

## 팀원 소개

| 이름 | 역할 | GitHub 프로필 | 이메일 |
|------|------|----------------|--------|
| 김상원 | 프로젝트 매니저, 인공지능 학습 및 배포 | [GitHub](https://github.com/daydream-er) | borntocde@naver.com |
| 윤태형 | 프론트엔드 개발자, React 및 Flask | [GitHub](https://github.com/YunTaeng) | howard9166@naver.com |
| 최우석 | 백엔드 개발자, 서버 운용 및 관리 | [GitHub](https://github.com/ddakgi00) | younghee@example.com |
| 강주현 | 프론트엔드 개발자, React 및 경로 탐색 | [GitHub](https://github.com/younghee) | juhyunk0820@naver.com |
