---
title: "VOC 기반 고객 행동 분석 및 상품 기획"
period: "2026/03/05 → 2026/03/20"
order: 4
cover: "/assets/images/projects/03-voc-bedding/cover.png"
field: ["기업", "고객", "상품", "서비스"]
skills: ["웹크롤링", "Python", "분류", "자연어처리", "토픽모델링", "텍스트마이닝", "비정형"]
---

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-01.png' | relative_url }}" alt="침구 관리의 번거로움을 해결하는 침구 리프레셔 — BX/CX/DX 프로젝트 로드맵">
  <figcaption>프로젝트 개요 (BX·CX·DX 로드맵)</figcaption>
</figure>

## 프로젝트 추진 배경

- 성숙 시장의 한계를 넘는 LG전자만의 성공 방정식 → '신규 카테고리라이징'을 통한 시장 지배력 강화
- 현대인의 가장 절실한 니즈는 '수면' - 이제는 기술 기반의 솔루션을 통해 거대 신규 시장으로 구체화 중
- LG전자의 '수면 가전' 카테고리의 전략적 공백

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-02.png' | relative_url }}" alt="수면 개선 노력 2x2 매트릭스 — 내적/외적 요인, 능동적/수동적 관리">
  <figcaption>수면 개선 노력 세그멘테이션</figcaption>
</figure>

## Step1. 고객 경험 목표

수면의 질 개선 노력에 따른 세그멘테이션 정의

'침구관리' 연관어 분석 결과 - 침구류 위생에 관한 니즈와 기존 방식의 한계 파악

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-03.png' | relative_url }}" alt="'침구관리' 연관어 네트워크 분석">
  <figcaption>'침구관리' 연관어 분석</figcaption>
</figure>

- 알러지 질환 발생 원인 인식 1위 → 집먼지 진드기 (87.5%)
- 집먼지 진드기 서식 장소 인식 1위 → 침구류 (72.2%)

기존 침구 관리 방식의 한계

<div class="fig-row">
  <figure class="figure--sm">
    <img src="{{ '/assets/images/projects/03-voc-bedding/img-04.png' | relative_url }}" alt="아토피피부염 진단 연별 추이 (표준화율)">
    <figcaption>아토피피부염 진단 연별 추이</figcaption>
  </figure>

  <figure class="figure--sm">
    <img src="{{ '/assets/images/projects/03-voc-bedding/img-05.png' | relative_url }}" alt="기존 침구 관리 방식(스타일러, 세탁기, 건조기 등)의 핵심 한계 및 불편사항">
    <figcaption>기존 침구 관리 방식의 한계</figcaption>
  </figure>
</div>

타깃 고객 ⇒ 침구 위생에 관심이 많은 사람들:

- 침구 관리에 소홀한 맞벌이 부부
- 아이 이불 위생이 걱정되는 초보 엄마아빠
- 반려동물을 키우는 가정

## Step2. 데이터 수집 및 분석

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-06.png' | relative_url }}" alt="검색 키워드, 데이터 식별 전략, 데이터 수집 범위와 채널별 건수">
  <figcaption>데이터 수집 범위 (총 55,754건)</figcaption>
</figure>

데이터 전처리: 결측치 및 중복 처리 / 컬럼 병합(제목·내용·댓글) / 10자 이하 짧은 글 제거 / 특수문자·숫자 제거 / 형태소 분석(명사·동사·형용사 추출) / 불용어 처리

자연어 처리 → Doc2Vec 기반 임베딩을 통해 텍스트 데이터를 벡터화

빈도분석, Silhouette Score 기반 최적의 K 선정

<div class="fig-row">
  <figure class="figure--sm">
    <img src="{{ '/assets/images/projects/03-voc-bedding/img-07.png' | relative_url }}" alt="TF-IDF 상위 토큰 표와 워드클라우드">
    <figcaption>TF-IDF 빈도 분석 및 워드클라우드</figcaption>
  </figure>

  <figure class="figure--sm">
    <img src="{{ '/assets/images/projects/03-voc-bedding/img-08.png' | relative_url }}" alt="클러스터 수(K)에 따른 Silhouette Score 변화 그래프">
    <figcaption>Silhouette Score 기반 최적 K 선정</figcaption>
  </figure>
</div>

## Step3. 타깃고객 분석

같은 침대 위생 관리, 서로 다른 욕구의 Actor 7개 도출

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-09.png' | relative_url }}" alt="Actor 0~2 — 냄새 제거 관리형, 침구 위생 가전 활용형, 침구 종류별 관리형">
  <figcaption>Actor 0~2</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-10.png' | relative_url }}" alt="Actor 3~6 — 숙소 침구 위생 중시형, 알레르기·피부 민감형, 가족 위생 관리형, 스마트 가전 기반 숙면 추구형">
  <figcaption>Actor 3~6</figcaption>
</figure>

기회영역 그래프 기반 해결이 시급한 고객 행동 추출

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-11.png' | relative_url }}" alt="Importance-Satisfaction 기반 기회영역 산점도 그래프">
  <figcaption>기회영역 그래프 (Importance × Satisfaction)</figcaption>
</figure>

페르소나 설정: Main Persona - 호흡기 및 피부 안심 케어러 / Sub Persona - 반려가족 공생 위생 케어러 & 스마트 가전 기반 숙면 추구자

각각 Desire, Goal, Pain Points 분석 후 정리

## Step4. 핵심 경험 컨셉 설정

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-12.png' | relative_url }}" alt="4D-CX 프레임워크 — 정신적 공간, 물리적 공간, 문화적 공간, 시스템적 공간">
  <figcaption>4D-CX 분석 프레임워크</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-14.png' | relative_url }}" alt="LG E:VE — Everyday Volume Experience 컨셉 침대 렌더링">
  <figcaption>LG E:VE (Everyday Volume Experience)</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-13.png' | relative_url }}" alt="침대 하부 서랍형 침구 케어 디바이스 컨셉 렌더링">
  <figcaption>침대 하부 내장형 침구 케어 컨셉</figcaption>
</figure>

- 스마트 홈 베딩 케어 - AI 분석을 통해 눈으로 직접 확인하는 안심 리포트

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-15.png' | relative_url }}" alt="스마트 홈 베딩 케어 앱 UI(청결도 리포트)와 UVC 케어·고온 스팀 살균·향기 케어 제품 렌더링">
  <figcaption>스마트 홈 베딩 케어 — 앱 리포트 &amp; 제품 기능</figcaption>
</figure>

- 반려동물 모드 - 고속 진동 털기 모드 및 흡입 기능으로 반려동물의 털 완벽 제거
- 계절별 기능 모드 - 여름철 급속 제습 / 겨울철 온풍 보온
- 고온 + UV 살균 기능 - 고온 열풍·스팀 + UV-C 살균으로 세균, 집먼지 진드기, 냄새 원인균 제거
- AI 기능 - 무게·소재 자동 감지로 최적의 스팀량 및 소요 시간 파악, 소재별 맞춤형 침구 관리
- 저소음 의류 관리 모드, 향기시트를 통한 탈취 기능, 청결도 수치화

## 실현 가능성 및 유사제품 사이 경쟁력 검토

- 제품 안전 리스크: 다중 온도 감지 센서 및 이상 과열 시 자동 전원 차단 시스템(Fail-safe) 필수 도입
- 원단 손상 및 배상 리스크: 원단별 저온 제습 모드 및 안전 가이드라인 제공, 사전 검증된 맞춤형 프리셋(펫 모드, 알러지 모드 등) 위주 설계
- 기술적 완성도: MVP 단계 - '날씨 연동 자동 건조'와 '진드기 퇴치 UV/스팀' 핵심 기능 구현에 집중

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-16.png' | relative_url }}" alt="위생 케어 심도 대비 사용자 편리도 기준 LG E:VE 경쟁 포지셔닝 매트릭스">
  <figcaption>유사 제품 대비 경쟁 포지셔닝</figcaption>
</figure>

고객 가치 지표 및 경영 성과 지표 설정

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-17.png' | relative_url }}" alt="진드기·세균 제거율, 피부 트러블 기록, 월별 침구 관리 시간 변화 그래프">
  <figcaption>고객 가치 지표</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/images/projects/03-voc-bedding/img-18.png' | relative_url }}" alt="스마트 기능 활용 정도, NPS, AI 기능 활용률 그래프">
  <figcaption>경영 성과 지표</figcaption>
</figure>
