
# 알츠하이머 예측 및 치료 방안 모색 프로젝트

## 주제 선정
 <img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/dd2d3692-f360-4147-9aa4-f658e43fd287">
1) 심장병과 관련된 진료를 보는 사람들이 매년 계속 증가하고 있음 
2) 심장질환에 대한 사망률 역시 점점 증가하고 있음
-  심장병에 영향을 미치는 요인이 무엇인지 분석하고, 심장병을 예측하는 모델을 만들어 심장병을 예방할 수 있는 방안 모색
<br>

## 데이터
### 수집한 데이터 
- [heart disease 2020](https://www.kaggle.com/datasets/aqleemkhan/heart-disease-2020/data) : 2020년 심장병과 관련이 있는 다양한 요소들에 대한 설문조사
- [알츠하이머 2014-2023 환자 통계](https://opendata.hira.or.kr/op/opc/olap3thDsInfoTab3.do#none) : 2014년부터 2023년까지 알츠하이머 환자 통계
<br>

## 데이터 컬럼들에 대한 설명

### 1. 인적 정보
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|PatientID|식별 번호|471-6900|Age|나이|60-90|
|Gender|성별|0:남자, 1 : 여자|Ethnicity|인종|0:백인, 1 : 아프리카계 미국인, 2 : 아시아, 3 : 기타|
|EducationLevel|교육 수준|0 : 없음, 1 : 고등학교, 2 : 학사, 3 : 더 높음|

### 2. lifestype
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Smoking|흡연 유/무|0 : 아니오, 1 : 예|AlcoholConsumption|주당 알코올 소비량|0-20|
|PhysicalActivity|주간 신체 활동량|0-10|DietQuality|식단 품질|0-10|
|SleepQuality|수면의 질|4-10|

### 3. 병력
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|FamilyHistoryAlzheimers|알츠하이머 가족력|0 : 없음, 1 : 예|CardiovascularDisease|심혈관 질환 유무|0 : 없음, 1 : 예|
|Diabetes|당뇨병 유무|0 : 없음, 1 : 예|Depression|우울증 유무|0 : 없음, 1 : 예|
|HeadInjury|두부 손상 유무|0 : 없음, 1 : 예|Hypertension|고혈압 유무|0 : 없음, 1 : 예|

### 4. 임상 측정
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|SystolicBP|수축기 혈압|90-180|DiastolicBP|이완기 혈압|60-120|
|CholesterolTotal|콜레스테롤 총량|150-300|CholesterolLDL|LDL콜레스테롤 수치|50-200|
|CholesterolHDL|HDL콜레스테롤 수치|20-100|CholesterolTriglycerides|중성지방|50-400|
|BMI|신체질량지수|15-40|

### 5. 인지 및 기능 평가
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|MMSE|간이 정신 상태 검사 점수|0-30, 낮을수록 인지 장애가 있음|FunctionalAssessment|기능평가|0-10, 낮을수록 기능 장애가 심함|
|MemoryComplaints|기억 장애 유무|0 : 없음, 1 : 예|BehavioralProblems|행동 문제 유무|0 : 없음, 1 : 예|
|ADL|일상생활활동 점수|0-10, 낮을수록 장애가 심함|

### 6. 증상
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Confusion|혼란의 유무|0 : 없음, 1 : 예|Disorientation|방향 감각 상실 유무|0 : 없음, 1 : 예|
|PersonalityChanges|성격 변화 유무|0 : 없음, 1 : 예|DifficultyCompletingTasks|작업 완료 어려움 유무|0 : 없음, 1 : 예|
|Forgetfulness|건망증 유무|0 : 없음, 1 : 예|

### 7. 진단
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Diagnosis|알츠하이머 유무|0 : 없음, 1 : 예|DoctorInCharge|담당 의사에 대한 정보|'XXXConfid'|
<br>

## 주요 기술
|소프트웨어|구분|활용 범위|
|--|--|--|
|python|Programming|프로그램 코드 작성|
|Jupyter|Programming|오픈소스 웹 애플리케이션|
|Collaboration tool|Docker|개발 환경 공유|
<br>


## 진행 과정
|분류|활동|날짜|진행 상황|파일 위치|
|--|--|--|--|--|
|Part 1|심장병에 미치는 영향 분석|2024.02.26 ~ 2024.03.03|완료|[heart impact factor](https://github.com/nohjuhyeon/heart_disease_projects/blob/main/docs/data_analysis/heart_impact_factor.ipynb)|
|Part 2|심장병 예측 모델 제작|2024.03.04 ~ 2024.03.10|완료|[classification : NONE](https://github.com/nohjuhyeon/heart_disease_projects/blob/main/docs/data_analysis/classification_NONE.ipynb)<br>[classification : UNDER](https://github.com/nohjuhyeon/heart_disease_projects/blob/main/docs/data_analysis/classification_UNDER.ipynb)<br>[classification : SMOTE](https://github.com/nohjuhyeon/heart_disease_projects/blob/main/docs/data_analysis/classification_SMOTE.ipynb)<br>[classification : SMOTEENN](https://github.com/nohjuhyeon/heart_disease_projects/blob/main/docs/data_analysis/classification_SMOTEENN.ipynb)||

