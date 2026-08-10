---
title: "신용카드 고객 세그먼트 분류 AI 알고리즘 개발"
period: "2025/03/10 → 2025/04/30"
order: 2
cover: "/assets/images/projects/02-credit-card/cover.png"
badge: "인공지능 경진대회 플랫폼 DACON 2등 수상 (총 236개 팀 참여)"
field: ["금융", "카드사"]
skills: ["Python", "고객세분화", "모델링", "분류"]
---

<figure>
  <img src="{{ '/assets/images/projects/02-credit-card/img-01.jpg' | relative_url }}" alt="DACON 신용카드 고객 세그먼트 분류 AI 경진대회 수상 인증서">
  <figcaption>DACON 신용카드 고객 세그먼트 분류 AI 경진대회 수상 인증서</figcaption>
</figure>

## 경진대회 목표

- 카드사 신용카드 고객 등급을 분류하는 AI 알고리즘 개발
- 각 고객들의 등급을 예측하는 모델 설계
- 마케팅 전략(고객 맞춤형 서비스 등) 및 고객 관리 기여

## Step1. 데이터 품질 관리

고객별 금융활동 데이터 (2018.07 ~ 2018.12)

**Train Data** — 240만 건 + 872개 변수

- 회원 정보: 78개 변수
- 신용 정보: 42개 변수
- 승인매출 정보: 406개 변수
- 청구입금 정보: 46개 변수
- 잔액 정보: 82개 변수
- 채널 정보: 105개 변수
- 마케팅 정보: 64개 변수
- 성과 정보: 49개 변수
- Segment (고객 등급): 1개 변수

**Test Data** — 60만 건 + 871개 변수 (동일 카테고리, Segment 제외)

**EDA**

각 등급별 인원 수 확인 → 문제 확인 → 방향 설정

- train data의 클래스 간 불균형이 매우 심했음 (E 등급이 약 80% 차지 & A/B 등급은 매우 적음) → A/B 등급 고객을 잘 구분하는 것으로 방향 설정
- Box Plot → 분포 확인
- 상관관계 분석: 상관계수 계산 및 heatmap 시각화 → 등급과 다른 변수 간의 상관관계 파악

<figure>
  <img src="{{ '/assets/images/projects/02-credit-card/img-02.png' | relative_url }}" alt="Segment별 고객 수 분포 — E 등급이 약 80% 차지하는 클래스 불균형">
  <figcaption>Segment별 고객 수 분포 (클래스 불균형 확인)</figcaption>
</figure>

**데이터 전처리**

결측치 처리 / 자료형 변환 / 파생변수 생성 / 변수 삭제

## Step2. 등급별 소비 패턴 분석

시각화를 통해 등급별 특징 파악

변수 분포 시각화 (box plot) → 특정 등급의 특징을 반영한 파생변수 생성

(예시) 고객 등급별 '1순위 카드 이용금액' 분포

<figure>
  <img src="{{ '/assets/images/projects/02-credit-card/img-03.png' | relative_url }}" alt="Segment별 1순위 카드이용금액 분포 박스플롯">
  <figcaption>Segment별 '1순위 카드이용금액' 분포</figcaption>
</figure>

## Step3. 고객 세분화 AI 알고리즘 개발

**문제 해결**

문제1. 많은 변수 → 학습 속도 저하 및 과적합

- 피처 중요도(feature importance) 산출 → 상위 변수 추출 (100개, 200개, 300개) → 조합별 모델 성능 비교
- 데이터 타입 최적화: 64비트 → 32비트

문제2. 클래스 불균형 (A/B 클래스 데이터 부족)

- SMOTE 오버샘플링 → 다양한 비율의 조합 실험
- 균형잡힌 클래스 가중치 적용
- mlogloss, macro F1-score 기준 비교

**모델링**

Google Colab T4 GPU를 이용하여 모델링 진행

- GPU 지원이 가능하고 대용량 데이터를 효율적으로 처리할 수 있는 모델 선정 → 3가지 모델: XGBoost, CatBoost, LightGBM
- Optuna를 통한 Hyperparameter tuning: 각각 9개, 6개, 11개의 parameter로 진행 → 모델 성능 극대화
- Soft voting → 단일 모델 대비 안정적이고 높은 성능 확보
  - XGBoost 40% + LightGBM 30% + CatBoost 30%
  - XGBoost 기준 중요도 상위 300개 변수 및 GPU 사용
- 각 모델에서 predict_proba()로 클래스별 예측 확률 추출
- 모델 별 확률 가중 평균 → 다양한 가중치 비율 조합 실험
- np.argmax()를 통해 가장 높은 확률의 클래스 선택

**고객 세분화**

- 총 5등급으로 고객군 세분화
- F1-score 약 2배 향상시킴
