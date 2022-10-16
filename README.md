# Credit_Bureau_BS_model

## 1. What is BSS(Behavior Scoring System) model?
### - 계약이 체결된 고객의 정보(속성, 신용거래, 기타 금융정보 등)를 종합하여 기존 고객의 신용도 변화를 점검하여 고객의 부실 가능성을 예측, 조기경보하는 시스템
### - 고객이 된 후 월 1회(Batch)로 점수 산출
### - 기존고객 관리 전략, 추가 대출 마케팅 전략에 사용함

## 2. BSS model의 단계
### 2.1 요건정의
### 2.2 모델 선정(Logistic? ML?..)
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
