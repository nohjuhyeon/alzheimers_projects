
# 알츠하이머 예측 및 치료 방안 모색 프로젝트

# 1. 주제 선정
 <img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/343dd121-805b-4575-8768-8088c0996f6c" width = '75%'>

1) 알츠하이머 환자수는 10년간 꾸준히 증가하는 추세를 보이고 있음.  
2) 환자는 대부분 60대 이상으로 구성되어 있음.

➡ 60-90로 구성되어 있는 환자들의 건강 정보를 포함하고 있는 데이터 셋을 활용하여 알츠하이머 예측 및 치료 방안으로 모색
<br>

# 2. 데이터
## 수집한 데이터 
- [alzheimers disease dataset](https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset/data) : 인구 통계적 세부 정보, 라이프스타일 요인, 병력, 임상 측정, 인지 및 기능 평가, 증상 및 알츠하이머병 진단이 포함되어 있는 데이터 세트
- [알츠하이머 2014-2023 환자 통계](https://opendata.hira.or.kr/op/opc/olap3thDsInfoTab3.do#none) : 2014년부터 2023년까지 알츠하이머 환자 통계
<br>

# 데이터 컬럼들에 대한 설명

### 1. 인적 정보
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|PatientID|식별 번호|471-6900|Age|나이|60-90|
|Gender|성별|0:남자, 1 : 여자|Ethnicity|인종|0:백인, 1 : 아프리카계 미국인, 2 : 아시아, 3 : 기타|
|Education Level|교육 수준|0 : 없음, 1 : 고등학교, 2 : 학사, 3 : 더 높음|

### 2. lifestype
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Smoking|흡연 유/무|0 : 아니오, 1 : 예|Alcohol Consumption|주당 알코올 소비량|0-20|
|Physical Activity|주간 신체 활동량|0-10|Diet Quality|식단 품질|0-10|
|Sleep Quality|수면의 질|4-10|

### 3. 병력
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Family History Alzheimers|알츠하이머 가족력|0 : 없음, 1 : 예|Cardiovascular Disease|심혈관 질환 유무|0 : 없음, 1 : 예|
|Diabetes|당뇨병 유무|0 : 없음, 1 : 예|Depression|우울증 유무|0 : 없음, 1 : 예|
|HeadInjury|두부 손상 유무|0 : 없음, 1 : 예|Hypertension|고혈압 유무|0 : 없음, 1 : 예|

### 4. 임상 측정
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Systolic BP|수축기 혈압|90-180|Diastolic BP|이완기 혈압|60-120|
|Cholesterol Total|콜레스테롤 총량|150-300|Cholesterol LDL|LDL콜레스테롤 수치|50-200|
|Cholesterol HDL|HDL콜레스테롤 수치|20-100|Cholesterol Triglycerides|중성지방|50-400|
|BMI|신체질량지수|15-40|

### 5. 인지 및 기능 평가
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|MMSE|간이 정신 상태 검사 점수|0-30, 낮을수록 인지 장애가 있음|Functional Assessment|기능평가|0-10, 낮을수록 기능 장애가 심함|
|Memory Complaints|기억 장애 유무|0 : 없음, 1 : 예|Behavioral Problems|행동 문제 유무|0 : 없음, 1 : 예|
|ADL|일상생활활동 점수|0-10, 낮을수록 장애가 심함|

### 6. 증상
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Confusion|혼란의 유무|0 : 없음, 1 : 예|Disorientation|방향 감각 상실 유무|0 : 없음, 1 : 예|
|Personality Changes|성격 변화 유무|0 : 없음, 1 : 예|Difficulty Completing Tasks|작업 완료 어려움 유무|0 : 없음, 1 : 예|
|Forget fulness|건망증 유무|0 : 없음, 1 : 예|

### 7. 진단
|column 명|설명|value|column 명|설명|value|
|--|--|--|--|--|--|
|Diagnosis|알츠하이머 유무|0 : 없음, 1 : 예|DoctorInCharge|담당 의사에 대한 정보|'XXXConfid'|
<br>

# 3. 주요 기술
|소프트웨어|구분|활용 범위|
|--|--|--|
|python|Programming|프로그램 코드 작성|
|Jupyter|Programming|오픈소스 웹 애플리케이션|
|Tableu|Programming|데이터 시각화|
|Collaboration tool|Docker|개발 환경 공유|
<br>


# 4. 파일 위치
|분류|활동|날짜|진행 상황|파일 위치|
|--|--|--|--|--|
|Part 1|알츠하이머에 영향을 미치는 요인 분석|2024.07.04 ~ 2024.07.06|완료|[hypothesis testing](https://github.com/nohjuhyeon/alzheimers_projects/blob/main/docs/data_analysis/hypothesis_testing.ipynb)|
|Part 2|알츠하이머 예측 모델 제작|2024.07.07 ~ |진행 중|[classification_model]()|

# 5. 진행 과정
## Part 1 : 알츠하이머에 영향을 미치는 요인 분석

### 첫번째 가설
- 인적 사항, 병력, 일상 생활, 임상 측정, 인지 및 기능 평가, 증상이 알츠하이머 유/무와 상관관계가 있다.

### 가설 검정 과정 
- 범주형 변수 : 카이제곱 검정
- 수치형 변수 : 둘 다 정규 분포일 경우 t-검정, 비정규 분포를 포함할 경우 Mann Whitney U 검정

### 가설 검정 결과  
<img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/85fdf745-647b-453a-aa24-49593f21d9b3" width="500" height="400"> <img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/f7eb5a33-d4ed-4d7d-a208-fe63ca199f91" width="500" height="400" >

- MemoryComplaints가 없을 때에 비해 MemoryComplaints가 있을 때 알츠하이머가 있을 가능성이 약 36.1% 상승함(27.9% -> 64%)
- MemoryComplaints가 없을 때에 비해 MemoryComplaints가 있을 때 알츠하이머가 있을 가능성이 약 36.1% 상승함(27.9% -> 64%)
- BehavioralProblems가 없을 때에 비해 BehavioralProblems가 있을 때 알츠하이머가 있을 가능성이 약 29,4% 상승함(30.8% -> 60.2%)

<img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/dcca1e7b-9575-4a07-ae52-6c320f044a97" width=75% >

- 알츠하이머가 있는 그룹이 없는 그룹에 비해 MMSE 점수가 5.58점 낮음.
- 알츠하이머가 있는 그룹이 없는 그룹에 비해 FunctionalAssessment 점수가 2.95점 낮음.
- 알츠하이머가 있는 그룹이 없는 그룹에 비해 ADL 점수가 2.90점 낮음.
- 알츠하이머가 있는 그룹이 없는 그룹에 비해 SleepQuality 점수가 0.33점 낮음.

### 결론 
- 인지 및 기능 평가 그룹(MemoryComplaints, BehavioralProblems, MMSE, FunctionalAssessment, ADL)이 알츠하이머 유/무와 상관관계가 있음.
- 인지 및 기능 평가 그룹 외에도 SleepQuality도 알츠하이머 유/무와 상관관계가 있지만, 큰 차이는 없음.

### 두번째 가설
- 인적 사항, 증상, 병력, 일상 생활, 임상 측정이 인지 및 기능 평가의 변수들과 상관관계가 있다.

### 가설 검정 과정 
- 인지 및 기능 평가 그룹에 범주형 변수와 수치형 변수가 섞여 있기 때문에 각각 검정 방법을 다르게 진행함. 
- 인지 및 기능 평가 변수가 범주형 변수일 경우(MemoryComplaints, BehaviorProblems)
    - 범주형 변수 : 카이제곱 검정
    - 수치형 변수 : 둘 다 정규 분포일 경우 t-검정, 비정규 분포를 포함할 경우 Mann Whitney U 검정
- 인지 및 기능 평가 변수가 수치형 변수일 경우(FunctionalAssessment, ADL, MMSE)
    - 범주형 변수 : 범주형 변수가 그룹이 2개일 경우 T-test/Mann Whitney U 검정, 세 개 이상일 경우 일원분산분석/크루스칼-왈리스 검정
    - 수치형 변수 : 둘 다 정규 분포일 경우 Pearson 상관관계 분석, 비정규 분포를 포함할 경우 Spearman 상관관계 분석

### 가설 검정 결과  
<img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/6d2be8fe-ff76-4198-ba0e-689ec3cc8286" width="500" height="400"> <img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/e84964e0-d33d-446f-bfcd-360a74194b26" width="500" height="400">
- DifficultyCompletingTasks가 MemoryComplaints와 관련이 있다.
    - DifficultyCompletingTasks가 없을 때에 비해 DifficultyCompletingTasks가 있을 때 MemoryComplaints가 있을 가능성이 약 4.9% 상승함(20.03% -> 24.93%)
    - MemoryComplaints가 없을 때에 비해 MemoryComplaints가 있을 때 DifficultyCompletingTasks가 있을 가능성이 약 4.0% 상승함(15.04% -> 19.02%)

<img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/3d1fa67b-7770-4368-9349-e91593975e30" width="500" height="400"> <img src="https://github.com/nohjuhyeon/alzheimers_projects/assets/151099184/ef854563-5034-4040-a247-f582b9f15782" width="500" height="400">

- HeadInjury가 BehavioralProblems와 관련이 있다.
    - HeadInjury가 없을 때에 비해 HeadInjury가 있을 때 BehavioralProblems가 있을 가능성이 약 5.94% 상승함(15.15% -> 21.09%)
    - BehavioralProblems가 없을 때에 비해 BehavioralProblems가 있을 때 HeadInjury가 있을 가능성이 약 3.8% 상승함(8.66% -> 12.46%)

### 결론 
- 기능 평가 결과 기억력에 문제가 있을 경우 업무 완료를 어려워하는 증상이 나타날 수 있다.
- 두부 손상을 당한 병력이 있으면 기능 평가에서 행동에 문제가 있을 수 있다.

## Part 2 : 알츠하이머 예측 모델 제작

