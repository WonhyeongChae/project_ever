# Current Team Synthesis

Last updated: 2026-09-10

## Executive Summary

현재 팀에서 가장 많이 논의되는 방향은 두 가지로 수렴함.

1. **AI 기반 실시간 경로·일정 추천**
2. **대기 시간을 활용한 퀘스트형 게이미피케이션**

두 아이디어는 별개 서비스라기보다 하나의 사용자 여정으로 결합 가능함.

핵심 통합 구조:

```text
실시간 현장 데이터
+ 사용자 선호/일정
↓
AI가 다음 최적 행동 결정
↓
경로 추천
+
남는 시간에 수행 가능한 Quest 제안
↓
혼잡 분산 / 체감 대기 감소 / 체류 경험 향상 / 부대 매출 연결
```

## 1. Core Direction A — AI Route Recommendation

### Current concept

`Everland AI Route Concierge`

사용자의 목적, 현재 위치, 스마트 줄서기 일정, 실시간 대기시간, 공연 일정, 이동시간, 식당/구역 혼잡도 등을 종합해 다음 행동과 경로를 추천함.

### Why this direction is strong

- 기존 스마트 줄서기의 빈 영역인 '예약 전후 남는 시간 활용'을 보완
- 초행 방문객의 일정 의사결정 부담 감소
- 특정 인기 구역 집중을 완화하는 분산 추천으로 확장 가능
- 가족/외국인/고령자 등 다양한 방문객 유형에 적용 가능

### Branch insights

#### wh

스마트 줄서기를 대체하지 않고 상위 의사결정 계층으로 활용. 핵심은 **기다림을 관리하는 시스템에서 기다리는 동안의 시간까지 설계하는 시스템으로 확장**하는 것.

#### gb

- `EVER SHADE`: 날씨, 그늘, 실내 시설, 이동 피로도를 반영한 쾌적 동선
- `PHOTO MOMENT AI`: 인파, 날씨, 햇빛 방향, 공연시간을 반영한 촬영 타이밍 추천

둘 모두 Route Concierge의 상황별 추천 모드로 통합 가능.

#### hg

`EVER DIRECTOR`: Vision AI 기반 혼잡도 분석과 능동적 넛지로 파크 전체 군중을 분산시키는 운영 최적화 접근.

개인 만족뿐 아니라 전체 파크 흐름을 함께 최적화한다는 점이 차별점.

### Recommended sub-modes

- Fast Route
- Balanced Route
- Shade Route
- Photo Route
- Family Route

### Major risks

- 실시간 데이터 연동 난이도
- 위치 데이터 확보
- 추천 오류 시 신뢰 하락
- AI 추천이 다시 특정 시설 집중을 만드는 피드백 루프
- 상시 GPS 사용 시 개인정보/배터리 부담

### Mitigation

- 2~3개 선택지 제공
- QR/NFC 체크포인트 기반 위치 갱신 병행
- 단일 예상값 대신 범위와 혼잡 추세 제공
- 개인 최적화와 전체 혼잡 분산을 동시에 고려

---

## 2. Core Direction B — Waiting-Time Quest

### Current concept

`Everland Waiting Quest`

스마트 줄서기 또는 어트랙션 이용까지 남은 시간을 AI가 계산하고, 현재 위치와 취향에 맞는 짧은 미션을 생성함.

### Why this direction is strong

- 대기시간을 단순 손실이 아니라 콘텐츠 시간으로 전환
- 기존 공간을 신규 콘텐츠처럼 재활용 가능
- Quest를 통해 비인기 구역 방문을 자연스럽게 유도
- 시즌 이벤트, 멤버십, F&B와 확장성이 높음

### Branch insights

#### wh — Invisible Quest

사용자가 앱 미션에 끌려다니는 구조를 피하고, 실제 방문 행동 자체가 자동으로 진행 조건이 되는 방식.

핵심:

> 사람이 Quest를 따라가는 것이 아니라, 자신의 하루가 Quest가 됨.

#### gb — Dynamic Personalized Quest

가족, 친구, 커플 등 동행 유형과 현재 혼잡도에 따라 Quest를 실시간으로 다르게 생성.

정적 스탬프 투어와의 차별점은 **상황에 따라 목표와 장소가 변한다는 점**.

#### hg — Waiting Time × F&B × Membership

남은 대기시간을 인근 F&B 스마트 오더와 짧은 미션으로 연결.

```text
탑승까지 40분
→ 근처 간식 미션
→ 스마트 오더/픽업
→ 포인트 또는 배지
→ 어트랙션 복귀
```

게이미피케이션이 매출로 직접 연결될 수 있다는 장점.

### Recommended quest types

- Explore Quest
- Photo Quest
- Snack Quest
- Party Quest
- Season Quest
- Invisible Quest

### Major risks

- Quest 피로 및 숙제화
- 앱 확인 빈도 증가
- QR 부정 인증
- 대기시간 변동으로 탑승 시간 충돌
- F&B 주문 집중으로 새로운 병목 발생
- 과도한 포인트/쿠폰 지급 비용

### Mitigation

- 선택형 Quest
- 5~20분 단위 짧은 미션
- Invisible Quest 비중 확대
- 시간 계산에 안전 마진 적용
- 혼잡 시설/매장은 Quest 대상에서 자동 제외
- 디지털/경험형 보상 중심 설계

---

## 3. Recommended Integrated Concept

### Working concept

`AI Route + Quest`

AI가 먼저 **어디로 가야 하는지** 결정하고, 이동 또는 대기 사이의 남는 시간에 **무엇을 하면 좋은지** Quest로 제안하는 구조.

```text
[현재 위치 / 선호 / 스마트 줄서기 / 대기시간 / 혼잡도]
                          ↓
                         AI
                          ↓
              Next Best Action 결정
                          ↓
              ┌───────────┴───────────┐
              ↓                       ↓
          Route 추천              Short Quest
              ↓                       ↓
       이동 효율 개선          대기시간 콘텐츠화
              └───────────┬───────────┘
                          ↓
            만족도 / 체류 / 분산 / 매출
```

### Example scenario

```text
현재 13:00
T익스프레스 예약 14:00
현재 위치 판다월드
↓
AI 분석
↓
13:05~13:20 포토 Quest
13:20~13:35 인근 Snack Quest + 픽업
13:35 T익스프레스 방향 이동
13:55 도착
```

상황 변화 시:

```text
T익스프레스 지연
↓
추가 Quest 또는 우회 콘텐츠 추천
```

### Core value proposition

> **AI가 '어디로 갈지'뿐 아니라 '기다리는 동안 무엇을 할지'까지 설계함.**

---

## 4. Supporting Infrastructure / Data

필요 데이터:

- 실시간 어트랙션 대기시간 및 운영 상태
- 스마트 줄서기 예약/이용 시간
- 시설/매장/공연 위치
- 공연·퍼레이드 일정
- 사용자 선호 및 동행 유형
- 익명화된 현재 위치 또는 QR/NFC 체크포인트
- 가능하면 식당 혼잡도와 모바일 오더 처리시간
- 선택적으로 날씨, 그늘, 실내/실외 정보
- 선택적으로 Vision AI 기반 구역 혼잡도

### QR/NFC role

QR/NFC 체크포인트는 상시 GPS 없이 사용자의 현재 위치를 갱신하고, Quest 방문 인증에도 재사용 가능한 공통 인프라 후보.

---

## 5. Revenue Position

Revenue는 현재 독립적인 최종 주제라기보다 **통합 서비스의 기대 효과 및 보조 메커니즘**으로 두는 방향이 적합함.

연결 가능 포인트:

- Waiting Quest와 F&B 스마트 오더 결합
- AI Route를 통한 유휴 매장/비인기 구역 트래픽 유입
- 시즌 Quest와 굿즈 구매 권한 연결
- 개인화된 상황형 추천

단, 광고 노출 자체를 핵심 경험으로 만들지 않는 것이 중요함.

---

## Decisions

- 기존 Revenue / Gamification / Concierge 3축을 유지하되, 최종 주제 후보 우선순위를 재정렬함.
- **1순위 논의 축: AI 경로·일정 추천**
- **2순위 논의 축: 대기시간 활용 Quest**
- 두 축을 결합한 통합 서비스 구조를 최우선 검토함.
- Revenue는 독립 서비스보다 통합 서비스의 사업 효과로 연결하는 방향 선호.

## Remaining Decision Points

1. 최종 제출안을 `AI Route Concierge` 단일 주제로 좁힐지
2. `AI Route + Waiting Quest` 통합안으로 제출할지
3. Quest의 핵심 보상을 디지털 경험 중심으로 할지 F&B/멤버십과 강하게 연결할지
4. 위치 확보 방식을 QR/NFC 중심으로 제안할지 기존 앱 위치 데이터 중심으로 제안할지
5. Vision AI 혼잡 감지를 핵심 기능으로 넣을지 확장 기능으로 둘지

## Research Gaps

- 에버랜드 현재 스마트 줄서기 실제 운영 방식과 남는 시간 UX
- 공식 앱의 지도/추천/모바일 오더 기능 범위
- 실시간 대기시간과 스마트 줄서기 데이터 연동 가능성
- F&B 모바일 주문 및 픽업 인프라 현황
- 기존 스탬프/미션 이벤트와 Dynamic Quest 차별화 근거
- QR/NFC 체크포인트 도입 비용 및 참여율
- 테마파크 혼잡 분산 추천의 실제 사례와 효과
