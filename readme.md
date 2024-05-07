# 딴복 ( 딴짓하면, 복습이다! )
학습 능률 향상 & 학습 태도 개선을 위한 스터디 앱

YOLOv5 알고리즘을 활용한 학습 모델을 통해 사용자의 학습 태도를 분석함과 동시에, 
에빙하우스의 망각곡선 이론을 활용하여 효율적인 학습을 할 수 있도록 도와주는 스터디 애플리케이션

<br />

## **📝 프로젝트 개요**

<img width="100%" height="700" alt="메인 페이지" src="https://github.com/YouHyunji/Application-to-Improve-Learning-Attitudes/assets/54940615/cfa46037-ffc3-4c88-b762-fac90085a461" />


<br>
<br>

> **프로젝트:** 학습 능률 향상 & 학습 태도 개선을 위한 스터디 앱
>
> **기획:** 유현지
>
> **개발:** 김지섭(팀장), 유현지, 노관범
> 
> **분류:** 팀 프로젝트
>
> **제작 기간:** 2022.10.01 ~ 2023.10.31
>
> **주요 기능:** 망각 진행률 그래프, YOLOv5 모델을 활용한 학습 태도 분석, 복습하기 리스트
>


<br />

## 🛠 기술 및 도구
![Java](https://img.shields.io/badge/JAVA-007396?style=flat-square&logo=java&logoColor=white) 
![Python](https://img.shields.io/badge/Python-3776AB?&style=flat-square&logo=Python&logoColor=white)
![Android Studio](https://img.shields.io/badge/Android%20Studio-3DDC84?style=flat-square&logo=Android&logoColor=white) 
![Colab](https://img.shields.io/badge/Google%20Colab-F9AB00.svg?&style=flat-square&logo=googlecolab&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-%23039BE5.svg?style=flat-square&logo=firebase)
![GitHub](https://img.shields.io/badge/Github-%23121011.svg?style=flat-square&logo=github&logoColor=white)

<br>

## 🔗 링크

**Original Repository Link :** [https://github.com/gamjaseob/Review_Project](https://github.com/gamjaseob/Review_Project)

<br />

## 💻 동작 구조도
![시스템 구조도](https://github.com/gamjaseob/Review_Project/assets/54940615/f82a930d-779f-425f-ab45-3e0d4ca05838)

<br>

## 🎯 주요 기능

### 1. 사용자가 학습한 파일에 대한 " 망각 진행률 " 그래프 제공
- 헤르만 에빙하우스의 망각 곡선 이론을 바탕
- 사용자는 그래프를 열람으로써 동기 부여 효과
- 망각 진행률이 60%일 때, 복습 알림 전송

<img width="450" height="600" alt="망각곡선" src="https://github.com/YouHyunji/Application-to-Improve-Learning-Attitudes/assets/54940615/78b3cbb0-f0ec-418a-9db4-79308c49de26.gif" />

<br>
  
### 2. AI 모델 ( YOLOv5 ) 을 적용시킨 학습 태도 분석 ( 집중모드 )

<img width="50%" alt="학습 태도 분석 과정" src="https://github.com/YouHyunji/Review_Project/assets/54940615/4e08069d-4eea-4101-b2f7-65612c34ba2f" />

- 사용자가 자리 이탈 하는 경우와 졸고 있는 경우를 감지
- 집중모드로 학습 후 학습 태도 분석 결과 열람 가능
- 학습 태도 개선 효과
<br>
  
### 3. "복습하기 " 리스트
- 사용자가 학습한 파일 중에서, 시스템이 복습이 필요하다고 판단한 파일을 '복습하기' 리스트에 자동으로 업로드
- '복습하기' 리스트에서는 '집중모드'가 자동 실행
- 시스템이 복습이 잘 되었다고 판단했을 경우에는 복습하기 리스트에서 자동으로 삭제
- 복습 횟수 증가 & 학습 태도를 개선 효과

<br>

## ⏰ 커밋 히스토리

[나의 커밋 히스토리](https://github.com/gamjaseob/Review_Project/commits?author=YouHyunji)
<br/>
<br/>
<br/>

## 📑 개인 작업 요약

### 1. 앱의 초기 환경 구축

- 동작 구조도 설계
- 사용자 인증 관련 기능 구현: 로그인, 회원가입, 비밀번호 찾기
- 데이터베이스 테이블 설계 및 FireBase 연동
- 여러 개의 메뉴 버튼 구현
- 학습 및 복습 리스트 기능 구현: 과목 카테고리, 파일 추가 및 삭제, 일괄 삭제 구현
- PDF Viewer 구현
  
<br>

### 2. 망각 진행률 계산을 위한 데이터 로딩

- 사용자의 학습 시작 시간, 종료 시간을 데이터베이스에 저장
- 망각 진행률 계산을 위해 학습 종료 시간 데이터를 로드하는 로직 구현

<br>

### 3. 학습 태도 분석 모델 개발

- Custom DataSet 생성 : Annotation 작업 수행, Augmentation 기법 활용 
- YOLOv5 모델 학습 : 얼굴과 졸린 눈을 감지하는 모델 개발

<br>

### 4. 집중모드 구현
- 사용자의 집중 모드 선택 여부에 따라 복습하기 리스트와 동일한 동작을 수행하도록 하는 로직 구현 

<br>

### 5. 복습하기 리스트 기능 구현
- 복습이 필요한 파일은 자동으로 업로드되며, 복습이 완료된 파일은 자동으로 삭제되는 기능 구현
- 복습하기 메뉴 클릭 시, '집중모드' 자동 활성화


