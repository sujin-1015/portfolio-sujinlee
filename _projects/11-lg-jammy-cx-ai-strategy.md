---
title: "데이터 기반 LG 커뮤니티 CX 혁신 및 AI 서비스 전략 기획"
period: "2026/02/02 → 2026/02/06"
order: 5
cover: "/assets/images/projects/11-lg-jammy-cx-ai-strategy/cover.jpg"
field: ["AI", "기업", "커뮤니티", "고객", "가전"]
skills: ["서비스기획", "고객여정분석", "웹크롤링", "TF-IDF", "텍스트마이닝", "시각화", "Python"]
---

LG전자 DX School 5기 BX 프로젝트 — 팬덤 커뮤니티 Jammy의 사용자 행동 데이터를 분석해 CX 혁신 전략과 AI 서비스를 기획한 팀 프로젝트

- 데이터 기반 LG 팬덤 커뮤니티 CX 혁신 전략 → Jammy 사용자 행동 분석을 통한 고객 참여 개선 및 AI 기반 개인화 서비스 제안
- 팀: 미술랭 쓰리스타 (발표일 2026.02.06)

| 구분 | 내용 |
|---|---|
| Problem | 사용자 행동 데이터 분석 결과, Jammy는 지속적인 정보 탐색 공간보다 이벤트 중심의 일회성 참여 플랫폼으로 활용되고 있음을 확인 |
| Target | 구매 전 다양한 리뷰와 정보를 비교하는 30~40대 실용주의 소비자 Persona 정의 |
| Insight | 흩어진 고객의 정보 탐색 경험을 하나로 연결하고, 구매 확신을 제공하는 All-in-one 가전 커뮤니티 필요 |
| Solution | AI 제품 탐색 어시스턴트, 통합 검색, 참여형 챌린지, Life Stage 커뮤니티, 리워드 시스템으로 구성된 CX 혁신 전략 제안 |
| KPI | 사용자 활성 지표(DAU, 체류시간, 재방문율)와 비즈니스 지표(구매 전환율, 만족도)를 기반으로 성과 관리 체계 구축 |

## 1. 프로젝트 추진 배경

Jammy는 LG전자 제품 경험을 공유하고 고객 참여 데이터를 확보하기 위한 라이프스타일 기반 팬덤 플랫폼이다. 매거진 콘텐츠와 사용자 참여형 리뷰를 통해 Z세대와의 관계 형성을 목표로 운영되고 있다.

### 1-1. Jammy 현황 분석 및 핵심 문제 정의

**UX·UI 문제**

- 정보 탐색 경험 부족으로 인한 사용자 이탈
- 메뉴 구조가 서비스 목적과 기능을 명확하게 전달하지 못함
- 검색 기능 부재로 제품 정보 탐색 플랫폼 역할 제한
- 모바일 접근성 부족으로 반복 방문 경험 부족
- 일방향 리액션 구조로 사용자 간 상호작용 부족

**이벤트 의존적 참여 구조로 인한 고객 관계 형성 한계**

2025년 Jammy 일별 게시글 작성 추이를 분석한 결과, 게시글 작성과 댓글 활동이 특정 이벤트 기간에 집중되는 패턴을 확인했다. 이는 사용자가 플랫폼을 지속적인 정보 탐색·소통 공간보다 이벤트 참여 채널로 인식하고 있음을 의미한다.

<figure class="figure--wide">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-01-post-trend.png' | relative_url }}" alt="2025년 Jammy 일별 게시글 작성 추이 그래프 — 2025년 8월 1일 최대 71건, 그 외 기간은 대체로 10건 미만으로 등락하는 이벤트 의존적 패턴">
  <figcaption>2025년 Jammy 일별 게시글 작성 추이</figcaption>
</figure>

| 지표 | 총합 | 일평균 | 비고 |
|---|---|---|---|
| 게시글 | 2,646개 | 7.25개 | 게시글 없는 날 23일 (6.30%) |
| 좋아요 | 817개 | 2.24개 | 좋아요 없는 날 179일 (49.04%) |
| 댓글 | 37,416개 | 102.51개 | 댓글 없는 날 32일 (8.77%) |

<figure>
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-02-jammy-wordcloud.png' | relative_url }}" alt="LG전자 Jammy 관련 블로그 텍스트 TF-IDF 워드클라우드 — '이벤트', '참여', '가입', '혜택', '쿠폰' 등 이벤트·프로모션 관련 키워드가 두드러짐">
  <figcaption>Jammy 관련 블로그 텍스트 TF-IDF 워드클라우드</figcaption>
</figure>

따라서 Jammy는 이벤트 이후에도 사용자가 방문할 수 있는 정보 탐색·소통 기반의 지속 가능한 커뮤니티 경험 구축이 필요하다.

### 1-2. 브랜드 커뮤니티 기반 CX 강화 필요성

가전 구매 과정에서는 브랜드가 제공하는 정보보다 실제 사용자의 경험과 리뷰가 구매 결정에 중요한 영향을 미친다.

- 온라인 제품 구매 시 15~59세의 80%가 리뷰를 참고하며, 전자·가전·IT 분야는 타 구매자 리뷰 신뢰도가 가장 높음
- 2024년 기준 가전 소비자의 '정보탐색' 성향 지수는 65.0으로, 가격중시·유행지향 등 타 소비 성향 지표보다 뚜렷하게 높고 전년 대비로도 상승
- 2026년 트렌드 코리아 키워드 '1.5가구' — 독립성과 연결성을 함께 추구하는 생활 단위 확산으로 느슨하게 연결되는 커뮤니티 선호 증가
- 고객 유지율 5% 증가 시 수익 25~95% 증가 (Bain & Company), UGC 활용 시 구매 전환율 102.4% 상승 (PowerReviews)

**성공 사례 — 오늘의집 '이용자 주도형 커뮤니티'**

콘텐츠와 커머스를 결합해 잠재 소비자를 확보하고, 언제든 구매 가능한 원스톱 환경과 UGC 축적↔신규 이용자 유입의 선순환 구조를 구축했다. '쇼핑수다' 게시판은 포스트당 평균 조회수 238.75회, 하루 평균 새 포스트 51개이며 일요일에 포스트 작성이 뚜렷하게 급증한다.

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-03-ohou-pie-chart.png' | relative_url }}" alt="오늘의집 '쇼핑수다' 게시판 카테고리별 포스트 비중 — 고수의 추천템 41.5%, 가구 15.6%, 예쁜템러버 7.0%, 홈데코 5.5% 순">
  <figcaption>오늘의집 카테고리별 포스트 비중</figcaption>
</figure>

## 2. 데이터 기반 핵심 고객 정의 (Target Persona)

구매 전 다양한 정보를 비교·검증하며 합리적인 구매 결정을 원하는 30~40대 고객을 핵심 타깃으로 선정했다. 2024년 가전 구매 경험 조사에서 30대 여성과 40대 남성이 많이 관찰되었으며, MZ세대 중에서는 30대의 온라인 커뮤니티 이용이 가장 활발했다.

**Text Mining 기반 고객 관심사 및 정보 탐색 패턴 분석**

3040세대의 가전 구매 관련 온라인 데이터(5년간 블로그)를 Python 기반으로 분석(Web Crawling → Text Preprocessing → TF-IDF 키워드 추출 → WordCloud 시각화)해 고객이 중요하게 고려하는 구매 요인과 정보 탐색 패턴을 도출했다. 그 결과 가격·성능 정보뿐 아니라 실제 사용 경험 기반 추천 콘텐츠를 통해 구매 확신을 형성하는 것으로 분석되었다.

<figure>
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-04-3040-wordcloud.png' | relative_url }}" alt="3040세대 가전제품 관련 블로그 텍스트 TF-IDF 워드클라우드 — '생활', '가전', '다양', '매장', '추천' 등 실사용·정보탐색 관련 키워드가 크게 부각됨">
  <figcaption>3040세대 가전제품 관련 블로그 TF-IDF 워드클라우드</figcaption>
</figure>

**페르소나 — 김지민 (가상인물)**

30-40대 / 직장인 / 구매 고민 단계 · #실용주의 #성능비교 #신뢰할리뷰

- 구매 전 유튜브 리뷰, 블로그, 커뮤니티(뽐뿌, 클리앙 등) 후기를 교차 검증
- 최고 사양보다 가성비와 실사용 만족도, 유지비를 중시
- 광고성 콘텐츠나 기술 설명 위주 콘텐츠는 신뢰하지 않고 빠르게 이탈

**Customer Needs**

- 신뢰 가능한 실사용 정보 탐색
- 유사 환경 사용자의 구매 경험 공유
- 참여와 보상이 연결되는 커뮤니티 경험

## 3. 고객 여정 분석을 통한 CX 혁신 방향 도출

### 3-1. 고객 여정 분석 (Customer Journey Analysis)

데이터 분석과 사용자 행동 패턴 분석을 기반으로 고객 구매 여정별 Pain Point를 정의했다.

<figure class="figure--wide">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-05-customer-journey.jpg' | relative_url }}" alt="Jammy 고객 여정 6단계 다이어그램 — 인지및유입(호기심)→탐색및참여(거부감, 이탈위험 매우 높음)→심화탐색(불신)→구매의사결정(배신감, 구매포기위험)→구매이후(무관심, 활동중단)→장기관계(망각, 완전이탈)로 이어지는 감정·Pain Point 변화">
  <figcaption>Jammy 고객 여정 6단계 분석</figcaption>
</figure>

- 구매 전 탐색 과정에서 신뢰 가능한 정보 확보 경험 부족
- 외부 플랫폼으로 이동하는 이탈 구조 확인
- 커뮤니티 내 검색·추천 기능 부족

→ 제품 탐색부터 구매 후 경험 공유까지 연결하는 End-to-End 고객 경험 설계 필요

### 3-2. 고객 감동 목표 및 인사이트 도출

**Customer Experience Vision**

고객의 탐색 경험을 연결하고, 사용자의 경험이 다시 새로운 고객 가치를 만드는 LG 대표 가전 커뮤니티 구축

- Discover — 제품 정보를 가장 먼저 찾는 탐색 플랫폼
- Trust — 실제 사용자 경험 기반 구매 신뢰 제공
- Engage — 참여와 보상이 연결되는 커뮤니티 경험
- Connect — LG와 고객이 지속적으로 관계를 형성하는 공간

Jammy의 낮은 사용성과 소비자의 적극적 정보 탐색 성향을 종합해 관찰(Fact)-고찰(Cause)-통찰(Insight) 분석으로 핵심 인사이트를 도출했다.

<figure class="figure--wide">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-06-insight-diagram.jpg' | relative_url }}" alt="관찰(Fact)-고찰(Cause)-통찰(Insight) 분석 다이어그램 — 이벤트 의존적 참여, 낮은 사용성, 리뷰 기반 구매결정 데이터를 근거로 'All-in-one 정보 커뮤니티' 인사이트를 도출하는 흐름">
  <figcaption>관찰-고찰-통찰 분석</figcaption>
</figure>

> "흩어진 소비자의 관심을 모으고 구매에 확신을 더하는 All-in-one 정보 커뮤니티"

## 4. CX 혁신을 위한 AI 기반 서비스 전략

### 4-1. AI 재미피티 — 개인 맞춤형 제품 탐색 어시스턴트

고객의 생활 환경과 관심 데이터를 기반으로 제품 탐색부터 구매 의사결정까지 지원하는 AI 서비스

- 사용자 관심사, 사용 환경, 활동 데이터 분석 기반 맞춤형 제품 및 콘텐츠 추천
- 복잡한 제품 스펙을 사용자의 생활 상황 중심 정보로 변환하여 이해도 향상

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-07-ai-assistant-ui.jpg' | relative_url }}" alt="AI 재미피티 제품 비교 챗봇 UI — 사용자 라이프스타일 기반으로 A제품·B제품을 비교해 'A제품이 98% 더 적합' 추천 결과를 보여주는 화면">
  <figcaption>AI 제품 비교 챗봇 UI</figcaption>
</figure>

기대효과: 제품 탐색 시간 감소 · 구매 의사결정 지원 · 개인화 경험 강화

### 4-2. AI 기반 Seamless Information Experience

- 검색 기능 — 상단 통합 검색창, 실시간 급상승 검색어
- 푸시 알림 — 관심 기기 관련 글 업로드 시 알림
- 비슷한 유저 — "나와 같은 평수/환경" 사람 찾기 & 추천

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-08-ai-lounge-ui.jpg' | relative_url }}" alt="AI 라이프스타일 라운지 UI — 매칭 태그(30평대 아파트, 아이 있는 집, 고양이 1마리 등) 기반으로 비슷한 라이프스타일의 이웃 사용자 후기를 추천하는 화면">
  <figcaption>AI 라이프스타일 라운지 UI</figcaption>
</figure>

기대효과: 트렌드 파악 수월 · 정보 놓침 방지 · 실패 없는 구매 유도

### 4-3. 참여형 챌린지

- Utility Challenge — 에어컨 전기요금 절약 챌린지
- Fun Challenge — 언박싱 쇼츠 챌린지, '나 이렇게까지 잘못 써봤다!'
- Brand Challenge — 옛날 제품 찍어 올려보기, 우리집 가전 꾸미기

### 4-4. Life Stage 기반 커뮤니티 세분화 전략

- Info — 고수의 추천템 (찐 사용기 공유)
- Life Stage — 맘스 홀릭(육아/홈데코/시월드), 고독한 집사(1인가구/혼밥/혼술)
- Interest — 스포츠 덕후(LG트윈스 야구방), 맛집 탐방러, 게이머 라운지

### 4-5. 활동 가치 기반 Reward System

- Care — 전자제품 점검 서비스, 소모품 교환
- Experience — 신제품 체험단 우선권, 오프라인 팝업(AI 키친/쿠킹클래스) 초청
- Mileage — LG전자 구매 포인트 연동

## 5. 서비스 활성화를 위한 KPI 및 성과 관리 체계

| 구분 | KPI |
|---|---|
| Activation | 가입자 수, DAU·WAU·MAU, 앱 다운로드 수 |
| Engagement | 평균 체류 시간, 게시글 작성률, 댓글 참여율 |
| Retention | 재방문율, 이탈률, 평균 방문 빈도 |
| Business | 구매 전환율, 제품 관심도 |
| Experience | AI 추천 만족도, NPS, AI 검색량 및 사용율 |

## 6. 기술 스택

| 영역 | 기술 |
|---|---|
| Programming | Python |
| Data Processing | Pandas |
| Text Analysis | TF-IDF Vectorizer |
| Visualization | Matplotlib, Seaborn, WordCloud |
| Data Collection | Web Crawling |
| Machine Learning | Scikit-learn |
