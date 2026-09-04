---
title: "데이터 기반 LG 커뮤니티 CX 혁신 및 AI 서비스 전략 기획"
period: "2026/02/02 → 2026/02/06"
order: 5
cover: "/assets/images/projects/11-lg-jammy-cx-ai-strategy/cover.jpg"
field: ["AI", "기업", "커뮤니티", "고객", "가전"]
skills: ["서비스기획", "고객여정분석", "웹크롤링", "TF-IDF", "텍스트마이닝", "시각화", "Python"]
---

LG전자 DX School 5기 BX 프로젝트
데이터 기반 LG 팬덤 커뮤니티 CX 혁신 전략
→ Jammy 사용자 행동 분석을 통한 고객 참여 개선 및 AI 기반 개인화 서비스 제안

- 팀: 미술랭 쓰리스타 (발표일 2026.02.06)

| 구분 | 내용 |
|---|---|
| Problem | 사용자 행동 데이터 분석 결과, Jammy는 지속적인 정보 탐색 공간보다 이벤트 중심의 일회성 참여 플랫폼으로 활용되고 있음을 확인 |
| Target | 구매 전 다양한 리뷰와 정보를 비교하는 30~40대 실용주의 소비자 Persona 정의 |
| Insight | 흩어진 고객의 정보 탐색 경험을 하나로 연결하고, 구매 확신을 제공하는 All-in-one 가전 커뮤니티 필요 |
| Solution | AI 제품 탐색 어시스턴트, 통합 검색, 참여형 챌린지, Life Stage 커뮤니티, 리워드 시스템으로 구성된 CX 혁신 전략 제안 |
| KPI | 사용자 활성 지표(DAU, 체류시간, 재방문율)와 비즈니스 지표(구매 전환율, 만족도)를 기반으로 성과 관리 체계 구축 |

## 1. 추진 배경

**Jammy란?**

Jammy는 LG전자 제품 경험을 공유하고 고객 참여 데이터를 확보하기 위한 라이프스타일 기반 팬덤 플랫폼이다. 매거진 콘텐츠와 사용자 참여형 리뷰를 통해 Z세대와의 관계 형성을 목표로 운영되고 있다.

### 1-1. Jammy 현황 분석 및 핵심 문제 정의

**①  UX·UI 문제**

- 정보 탐색 경험 부족으로 인한 사용자 이탈
- 메뉴 구조가 서비스 목적과 기능을 명확하게 전달하지 못함
- 검색 기능 부재로 제품 정보 탐색 플랫폼 역할 제한
- 모바일 접근성 부족으로 반복 방문 경험 부족
- 일방향 리액션 구조로 사용자 간 상호작용 부족

사용자가 방문해야 할 명확한 이유와 지속 참여를 유도하는 경험 설계 필요

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-01-ux-ui-issues.png' | relative_url }}" alt="Jammy UX·UI 문제 스크린샷 모음 — 목적이 불분명한 카테고리 메뉴(테크·스타일·낭만·일상), 종료일 없이 이어지는 이벤트 페이지, '#LGJammy' 해시태그 게시물이 500여 건에 그치는 검색 결과">
  <figcaption>Jammy UX·UI 문제</figcaption>
</figure>

**②  이벤트 의존적 참여 구조로 인한 고객 관계 형성 한계**

Jammy 사용자 활동 데이터를 분석한 결과, 게시글 작성과 댓글 활동이 특정 이벤트 기간에 집중되는 패턴을 확인했다. 이는 사용자가 플랫폼을 지속적인 정보 탐색 및 소통 공간보다 이벤트 참여 채널로 인식하고 있음을 의미한다.

**2025년 Jammy 일별 게시글 작성 추이**

<figure class="figure--wide">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-02-post-trend.png' | relative_url }}" alt="2025년 Jammy 일별 게시글 작성 추이 그래프 — 2025년 8월 1일 최대 71건, 그 외 기간은 대체로 10건 미만으로 등락하는 이벤트 의존적 패턴">
  <figcaption>2025년 Jammy 일별 게시글 작성 추이</figcaption>
</figure>

| 지표 | 총합 | 일평균 | 비고 |
|---|---|---|---|
| 게시글 | 2,646개 | 7.25개 | 게시글 없는 날 23일 (6.30%) |
| 좋아요 | 817개 | 2.24개 | 좋아요 없는 날 179일 (49.04%) |
| 댓글 | 37,416개 | 102.51개 | 댓글 없는 날 32일 (8.77%) |

따라서 Jammy는 이벤트 이후에도 사용자가 방문할 수 있는 정보 탐색·소통 기반의 지속 가능한 커뮤니티 경험 구축이 필요하다.

### 1-2. 브랜드 커뮤니티 기반 CX 강화 필요성

가전 구매 과정에서는 브랜드가 제공하는 정보보다 실제 사용자의 경험과 리뷰가 구매 결정에 중요한 영향을 미친다.

**근거 1. 구매 의사결정 과정에서 사용자 리뷰 영향력 증가**

<div class="fig-row" markdown="1">
<div markdown="1">

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-03-review-influence.png' | relative_url }}" alt="온라인 상품 구매 시 리뷰 참고 비율 도넛차트 — 참고한다 80%, 보통이다 18%, 참고하지 않는다 2%">
  <figcaption>온라인 쇼핑 시 리뷰 참고 비율</figcaption>
</figure>

온라인 제품 구매 시 15~59세 80%가 리뷰를 참고한다.

</div>
<div markdown="1">

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-04-industry-trust.png' | relative_url }}" alt="업종별 리뷰 신뢰도 비교 막대그래프 — 전자·가전·IT 68%로 8개 업종 중 신뢰도 1위, 식품·음료 66%, 패션·잡화 62%, 여행·숙박 62% 순">
  <figcaption>업종별 리뷰 신뢰도 비교</figcaption>
</figure>

전자·가전·IT 분야는 타 구매자의 리뷰 신뢰도가 가장 높다.

</div>
</div>

**근거 2. 가전 제품 특성상 실제 사용 경험 기반 정보 요구 증가**

<div class="fig-row" markdown="1">
<div markdown="1">

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-05-consumer-trend.png' | relative_url }}" alt="가전 소비자 성향 분석 결과(2023 vs 2024) 레이더차트 — 정보탐색 65.0으로 유행지향(56.1)·가격중시(53.9)·감성추구(52.5) 등 다른 지표보다 뚜렷하게 높고 전년 대비 상승">
  <figcaption>가전 소비자 성향 분석 결과 (2023 vs 2024)</figcaption>
</figure>

</div>
<div markdown="1">

가전 소비자는 '정보탐색' 성향이 강하며 정보 탐색 활동에 적극적이다. 2024년 기준 정보탐색 지수는 65.0으로, 가격 중시·유행 지향 등 다른 소비 성향 지표보다 뚜렷하게 높았고 전년 대비로도 상승했다.

</div>
</div>

**근거 3. 브랜드 커뮤니티는 고객 관계 형성 및 UGC 확보 채널로 활용 가능**

2026년 트렌드 코리아 키워드 '1.5가구' — 독립성(1)과 연결성(0.5)을 함께 추구하는 새로운 생활 단위. → 혼자 살지만 외롭지 않게 필요할 때 느슨하게 연결되는 커뮤니티 선호로, 커뮤니티 마케팅 효과를 기대할 수 있다.

- 고객 유지율 5% 증가 → 수익 25~95% 증가 (Bain & Company)
- 크리에이터의 콘텐츠(UGC) 활용 시 → 구매 전환율 102.4% 상승 (PowerReviews)

**[성공 사례] 오늘의집 '이용자 주도형 커뮤니티'**

<div class="fig-row" markdown="1">
<div markdown="1">

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-06-ohou-pie-chart.png' | relative_url }}" alt="오늘의집 '쇼핑수다' 게시판 카테고리별 포스트 비중 — 고수의 추천템 41.5%, 가구 15.6%, 예쁜템러버 7.0%, 홈데코 5.5% 순">
  <figcaption>오늘의집 쇼핑수다 게시판 카테고리별 포스트 비중 파이차트</figcaption>
</figure>

</div>
<div markdown="1">

- 콘텐츠와 커머스의 결합 → 잠재 소비자 확보
- 언제든 구매 가능한 원스톱 환경 구축
- 취향 데이터의 선순환: UGC 축적 ↔ 신규 이용자 유입
- '쇼핑수다' 게시판 포스트당 평균 조회수 238.75회, 하루 평균 새 포스트 51개
- 일요일에 포스트 작성이 뚜렷하게 급증하는 패턴 확인
- 사용자가 자주 작성하는 카테고리: 고수의 추천템(41.5%), 가구(15.6%), 예쁜템러버(7.0%), 홈데코(5.5%)

</div>
</div>

## 2. 데이터 기반 핵심 고객 정의 (Target Persona)

구매 전 다양한 정보를 비교·검증하며 합리적인 구매 결정을 원하는 30~40대 고객을 핵심 타깃으로 선정

<div class="fig-row" markdown="1">
<div markdown="1">

2024년 가전 구매 경험 조사 결과, 30대 여성과 40대 남성에서 많이 관찰되었다.

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-07-purchase-experience.png' | relative_url }}" alt="2024년 가전 구매 경험 비율 — 전체 74.7%, 성별·연령대별로는 30대 여성 86.7%, 40대 남성 80.7%로 가장 높음">
  <figcaption>2024년 가전 구매 경험</figcaption>
</figure>

</div>
<div markdown="1">

MZ세대 중 온라인 커뮤니티 이용이 가장 활발한 30대

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-08-community-frequency.png' | relative_url }}" alt="연령대별 온라인 커뮤니티 주간 평균 이용 일수 — 30대가 4.8일로 전체 연령대 중 가장 높고, 30대의 51.4%가 매일 이용한다고 응답">
  <figcaption>온라인 커뮤니티 이용 빈도 (단위: %)</figcaption>
</figure>

</div>
</div>

**Text Mining 기반 고객 관심사 및 정보 탐색 패턴 분석**

3040세대의 가전 구매 관련 온라인 데이터를 분석하여 고객이 중요하게 고려하는 구매 요인과 정보 탐색 패턴을 도출하였다.

- 3040세대 가전 관련 5년간 블로그 데이터 수집
- Python 기반 분석 방법: Web Crawling → Text Preprocessing → TF-IDF 기반 중요 키워드 추출 → WordCloud Visualization

분석 결과, 가격·성능 정보 뿐만 아니라 실제 사용 경험 기반 추천 콘텐츠를 통해 구매 확신을 형성하는 것으로 분석되었다.

<div class="fig-row" markdown="1">
<div markdown="1">

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-09-3040-wordcloud.png' | relative_url }}" alt="3040세대 가전제품 관련 블로그 텍스트 TF-IDF 워드클라우드 — '다양', '정보', '구매', '선택', '가격' 등의 키워드가 크게 부각됨">
  <figcaption>TF-IDF 워드클라우드</figcaption>
</figure>

</div>
<div markdown="1">

<figure class="figure--sm2">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-10-tfidf-keywords.png' | relative_url }}" alt="TF-IDF 상위 15개 키워드 순위표 — 1위 다양, 2위 정보, 3위 구매, 4위 선택, 5위 가격, 6위 공간, 7위 시장, 8위 정리, 9위 생활, 10위 경제, 11위 비용, 12위 관리, 13위 브랜드, 14위 추천, 15위 부담">
  <figcaption>TF-IDF 상위 15개 키워드</figcaption>
</figure>

</div>
</div>

**페르소나 설정 → 김지민 (가상인물)**

30-40대 / 직장인 / 구매 고민 단계 · #실용주의 #성능비교 #신뢰할리뷰

- 구매 전 유튜브 리뷰, 블로그, 커뮤니티(뽐뿌, 클리앙 등) 후기를 교차 검증
- 최고 사양보다 가성비와 실사용 만족도, 유지비를 중시
- 광고성 콘텐츠나 기술 설명 위주 콘텐츠는 신뢰하지 않고 빠르게 이탈

**Customer Needs**

- ①  신뢰 가능한 실사용 정보 탐색
- ②  유사 환경 사용자의 구매 경험 공유
- ③  참여와 보상이 연결되는 커뮤니티 경험

## 3. 고객 여정 분석을 통한 CX 혁신 방향 도출

### 3-1. 고객 여정 분석 (Customer Journey Analysis)

데이터 분석과 사용자 행동 패턴 분석을 기반으로 고객 구매 여정별 Pain Point를 정의하였다.

<figure class="figure--wide">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-11-customer-journey.jpg' | relative_url }}" alt="Jammy 고객 여정 6단계 다이어그램 — 인지및유입(호기심)→탐색및참여(거부감, 이탈위험 매우 높음)→심화탐색(불신)→구매의사결정(배신감, 구매포기위험)→구매이후(무관심, 활동중단)→장기관계(망각, 완전이탈)로 이어지는 감정·Pain Point 변화">
  <figcaption>Jammy 고객 여정 6단계 다이어그램</figcaption>
</figure>

- 구매 전 탐색 과정에서 신뢰 가능한 정보 확보 경험 부족
- 외부 플랫폼으로 이동하는 이탈 구조 확인
- 커뮤니티 내 검색·추천 기능 부족

→ 제품 탐색부터 구매 후 경험 공유까지 연결하는 End-to-End 고객 경험 설계 필요

### 3-2. 고객 감동 목표

**Customer Experience Vision**

고객의 탐색 경험을 연결하고, 사용자의 경험이 다시 새로운 고객 가치를 만드는 LG 대표 가전 커뮤니티 구축

- Discover — 제품 정보를 가장 먼저 찾는 탐색 플랫폼
- Trust — 실제 사용자 경험 기반 구매 신뢰 제공
- Engage — 참여와 보상이 연결되는 커뮤니티 경험
- Connect — LG와 고객이 지속적으로 관계를 형성하는 공간

**관찰(Fact) - 고찰(Cause) - 통찰(Insight) 분석**

Jammy의 낮은 사용성과 소비자의 적극적 정보 탐색 성향을 종합해 인사이트 도출

<figure class="figure--wide">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-12-insight-diagram.jpg' | relative_url }}" alt="관찰(Fact)-고찰(Cause)-통찰(Insight) 분석 다이어그램 — 이벤트 의존적 참여, 낮은 사용성, 리뷰 기반 구매결정 데이터를 근거로 'All-in-one 정보 커뮤니티' 인사이트를 도출하는 흐름">
  <figcaption>관찰(Fact) - 고찰(Cause) - 통찰(Insight) 분석</figcaption>
</figure>

→ "흩어진 소비자의 관심을 모으고 구매에 확신을 더하는 All-in-one 정보 커뮤니티"

## 4. CX 혁신을 위한 AI 기반 서비스 전략

### 4-1. AI 재미피티 : 개인 맞춤형 제품 탐색 어시스턴트

고객의 생활 환경과 관심 데이터를 기반으로 제품 탐색부터 구매 의사결정까지 지원하는 AI 서비스

<div class="fig-row fig-row--img-sm" markdown="1">
<div markdown="1">

<figure class="figure--sm" style="max-width:220px;margin-left:0">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-13-ai-assistant-ui.jpg' | relative_url }}" alt="AI 재미피티 제품 비교 챗봇 UI — 사용자 라이프스타일 기반으로 A제품·B제품을 비교해 'A제품이 98% 더 적합' 추천 결과를 보여주는 화면">
  <figcaption>AI 제품 비교 챗봇 UI</figcaption>
</figure>

</div>
<div markdown="1">

- ①  사용자 관심사, 사용 환경, 활동 데이터 분석 기반 맞춤형 제품 및 콘텐츠 추천
- ②  복잡한 제품 스펙을 사용자의 생활 상황 중심 정보로 변환하여 이해도 향상

**기대효과**

- 제품 탐색 시간 감소
- 구매 의사결정 지원
- 개인화 경험 강화

</div>
</div>

### 4-2. AI 기반 Seamless Information Experience

<div class="fig-row fig-row--img-sm" markdown="1">
<div markdown="1">

<figure class="figure--sm" style="max-width:220px;margin-left:0">
  <img src="{{ '/assets/images/projects/11-lg-jammy-cx-ai-strategy/img-14-ai-lounge-ui.jpg' | relative_url }}" alt="AI 라이프스타일 라운지 UI — 매칭 태그(30평대 아파트, 아이 있는 집, 고양이 1마리 등) 기반으로 비슷한 라이프스타일의 이웃 사용자 후기를 추천하는 화면">
  <figcaption>AI 라이프스타일 라운지 UI</figcaption>
</figure>

</div>
<div markdown="1">

- ①  검색 기능 — 상단 통합 검색창, 실시간 급상승 검색어
- ②  푸시 알림 — 관심 기기 관련 글 업로드 시 푸시 알림
- ③  비슷한 유저 — "나와 같은 평수·환경" 사람 찾기 & 추천

**기대효과**

- 트렌드 파악 수월
- 정보 놓침 방지
- 실패 없는 구매 유도

</div>
</div>

### 4-3. 참여형 챌린지

사용자 참여 활성화를 위한 Engagement Program

- Utility Challenge → 에어컨 전기요금 절약 챌린지
- Fun Challenge → 언박싱 쇼츠 챌린지, '나 이렇게까지 잘못 써봤다!'
- Brand Challenge → 옛날 제품 찍어 올려보기, 우리집 가전 꾸미기

### 4-4. Life Stage 기반 커뮤니티 세분화 전략

취향과 관심사로 묶이는 찐 소통

- Info → 고수의 추천템 (찐 사용기 공유)
- Life Stage → 맘스 홀릭(육아·홈데코·시월드), 고독한 집사(1인가구·혼밥·혼술)
- Interest → 스포츠 덕후(LG트윈스 야구방), 맛집 탐방러, 게이머 라운지

### 4-5. 활동 가치 기반 Reward System

활동으로 쌓은 포인트가 보상으로

- Care → 전자제품 점검 서비스, 소모품 교환
- Experience → 신제품 체험단 우선권, 오프라인 팝업(AI 키친·쿠킹클래스) 초청
- Mileage → LG전자 구매 포인트 연동

## 5. 서비스 활성화를 위한 KPI 및 성과 관리 체계

| 구분 | KPI |
|---|---|
| Activation | 가입자 수, DAU·WAU·MAU, 앱 다운로드 수 |
| Engagement | 평균 체류 시간, 게시글 작성률, 댓글 참여율 |
| Retention | 재방문율, 이탈률, 평균 방문 빈도 |
| Business | 구매 전환율, 제품 관심도 |
| Experience | AI 추천 만족도, NPS, AI 검색량 및 사용율 |

## 6. 기술 스택 (Data Analytics Framework)

| 분야 | 활용 기술 |
|---|---|
| Programming | Python |
| Data Processing | Pandas |
| Text Analysis | TF-IDF Vectorizer |
| Visualization | Matplotlib, Seaborn, WordCloud |
| Data Collection | Web Crawling |
| Machine Learning | Scikit-learn |
