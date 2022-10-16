# Credit_Bureau_BS_model

## 1. What is BSS(Behavior Scoring System) model?
### - 계약이 체결된 고객의 정보(속성, 신용거래, 기타 금융정보 등)를 종합하여 기존 고객의 신용도 변화를 점검하여 고객의 부실 가능성을 예측, 조기경보하는 시스템
### - 고객이 된 후 월 1회(Batch)로 점수 산출
### - 기존고객 관리 전략, 추가 대출 마케팅 전략에 사용함

## 2. BSS model의 단계
### 2.1 요건 정의
#### 2.1.1 대상자 선정 
- 기연체 대상자 제외 여부 선정
- ???? 일수의 최대값이 특정 일수 (ex. 60일, 90일) 이하인 대상자 제외 여부 선정
- 개인 대상자 vs. 소호 대상자 선정
  : 개인 대상자와 소호 대상자의 CB스코어 차이 등 서로 다른 성질에 의해 각 대상자 특성에 맞는 모델을 구축하는 것을 선호
#### 2.1.2 불량 정의
- 12개월 내 채무불이행 일수가 60일 이상 or 개인 회생 신청 or ????
#### 2.1.3 시점 정의: 개발 시점, 검증 시점1, 검증 시점2 정의
- 분기별 불량률 및 CB스코어 경향성 파악
- 개발 시점: 불량률 및 CB스코어가 시간이 경과할수록 증가하는 형태 또는 감소하는 형태를 보인다면 개발 시점을 연속적인 시점을 선택하는 것보다 간헐적인 시점을 선정하여 모든 경향성 및 계절성을 반영할 수 있게 함
- 검증 시점1: 개발 시점과 동일하게 간헐적인 시점으로 선정하여 모든 경향성 및 계절성에서 모형을 검증할 수 있게 함
- 검증 시점2: 최근 시점으로 설정하여, 개발한 BSS 모델의 최근 시점에서의 성능을 검증할 수 있게 함
### 2.2 모델 선정(Logistic? ML?..)
#### 2.2.1 Logistic Regression: 
#### 2.2.2 ML
#### 2.2.3 기타
- 앙상블: ML(Random Forest, Decision Tree, DNN)을 앙상블하여 모형의 예측 성능을 더욱 향상시키는 기법이지만 시간이 오래걸린다는 단점이 있음
### 2.3 모형 개발
#### 2.3.1 요약항목 선정
#### 가명처리-numeric.ipynb
- Fineclassing
- Coarse Classing
- Stepwise Selection(logistic regression 사용)
- 평점표 생성
- 등급화
#### 2.3.2 전략 수립(한도 전략, 승인 전략)
- 결합등급 생성
- Cut-off 전략 수립
