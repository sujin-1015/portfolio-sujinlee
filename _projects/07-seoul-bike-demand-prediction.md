---
title: "서울시 공공자전거 수요 예측 및 영향 요인 분석"
period: "2023/11/13 → 2023/12/07"
order: 8
cover: "/assets/images/projects/07-seoul-bike/cover.png"
field: ["교통", "공공서비스"]
skills: ["Python", "예측", "회귀", "모델링"]
---

## Step1. 데이터 수집

총 5개 범주의 데이터를 식별키를 기준으로 통합: 공공자전거(이용건수 등), 집객시설 및 상권, 아파트(평균 시가 등), 교통(버스정거장 수 등), 인구

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-01.png' | relative_url }}" alt="행정동별로 통합된 공공자전거·상권·집객시설·인구 데이터 스프레드시트">
  <figcaption>행정동 기준 통합 데이터 샘플</figcaption>
</figure>

## Step2. EDA 및 데이터 전처리

자치구별 현황 분석, 변수 분포 확인 → 표준화/정규화 필요성 파악

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-02.png' | relative_url }}" alt="자치구별 이용건수 및 대여소개수 막대그래프">
  <figcaption>자치구별 이용건수 · 대여소개수 현황</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-03.png' | relative_url }}" alt="자치구별 이용건수 분포 산점도">
  <figcaption>자치구별 이용건수 분포</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-04.png' | relative_url }}" alt="이용건수, 상권 수, 집객시설 수 등 주요 변수의 히스토그램 분포">
  <figcaption>주요 변수 분포 (표준화/정규화 필요성 확인)</figcaption>
</figure>

변수 간의 상관관계 → '공공자전거 이용건수'와 상관관계 높은 변수 파악

데이터 전처리: 변수명 변경, 결측치 처리, 중복 처리, 이상치 처리, log 변환, 표준화 등

## Step3. 이용 패턴 분석

Linear Regression, Standard/MinMax/Robust Scaler, Log Transformation, Cook's Distance 등

R-Squared 값 기준 모델 선택

회귀진단: 다중공선성, 정규성, 등분산성 확인

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-05.png' | relative_url }}" alt="Normal Q-Q plot, Equal Variance Check, 변수별 VIF 표">
  <figcaption>회귀진단 — 정규성 · 등분산성 · 다중공선성(VIF)</figcaption>
</figure>

결과 해석 및 활용 방안 제시

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-06.png' | relative_url }}" alt="최종 회귀식, 변수 설명, 남자 40대 생활인구 연도별 추이 그래프">
  <figcaption>최종 회귀식 및 활용 방안</figcaption>
</figure>

## Step4. 타 지역 설치 방향 제시

Logistic Regression, Forward Selection, Hosmer-Lemeshow test 등

서울시 이외의 지역 공공자전거 유치 방향성 제시

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-07.png' | relative_url }}" alt="지방 공공자전거 유치 방향성 제시 다이어그램">
  <figcaption>지방 공공자전거 유치 방향성 제시</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/images/projects/07-seoul-bike/img-08.png' | relative_url }}" alt="공공자전거 이용 활성화의 분석 의의 — 선형회귀분석과 로지스틱 회귀분석 요약">
  <figcaption>분석 의의 요약</figcaption>
</figure>
