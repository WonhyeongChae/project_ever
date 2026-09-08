---
name: team-synthesis
description: Merge team research notes into a concise, deduplicated contest knowledge base, separate evidence from hypotheses, update the three core idea tracks, and surface unresolved decisions and research gaps.
---

# Team Synthesis

## Goal

팀원별 Research Note를 비교·병합해 현재 팀의 공모전 아이디어 상태를 하나의 공용 지식으로 정리함.

## Trigger examples

- 팀 전체 자료 합쳐줘
- 리서치 중복 제거해줘
- 현재 아이디어 정리해줘
- 공모전 아이디어 통합해줘

## Required sources

우선 다음 경로 확인함.

- `research/**`
- `ideas/revenue.md`
- `ideas/gamification.md`
- `ideas/concierge.md`
- `synthesis/current-summary.md`

## Workflow

1. 모든 Research Note에서 핵심 주장과 근거를 추출함.
2. 같은 의미의 항목을 하나로 병합함.
3. 상충되는 주장이나 수치가 있으면 하나로 덮지 않고 충돌 상태로 표시함.
4. 각 항목을 다음 중 하나로 구분함.
   - Verified: 출처 또는 내부 근거가 충분함
   - Hypothesis: 아직 검증 필요
   - Proposal: 팀 아이디어
   - Risk: 구현/사업/UX 리스크
   - Decision: 팀에서 합의한 사항
5. 아래 3개 핵심 트랙에 매핑함.
   - Revenue
   - Gamification
   - Concierge
6. 여러 트랙을 연결하는 공통 인프라/데이터 요구사항 별도 추출함.
7. 기존 `ideas/*.md` 문서와 비교해 새 정보만 보강함.
8. `synthesis/current-summary.md`를 현재 상태 기준으로 갱신함.
9. 불필요하게 오래된 가설은 삭제하지 않고 `superseded`로 표시함.

## Output structure for current-summary.md

```md
# Current Team Synthesis

Last updated: YYYY-MM-DD

## Executive Summary

- 현재 가장 강한 방향
- 핵심 차별점
- 가장 큰 리스크

## 1. Revenue

### Current concept
### Evidence
### Expected impact
### Risks
### Open questions

## 2. Gamification

### Current concept
### Evidence
### Expected impact
### Risks
### Open questions

## 3. Concierge

### Current concept
### Evidence
### Expected impact
### Risks
### Open questions

## Shared Infrastructure / Data

- ...

## Decisions

- ...

## Conflicts / Unresolved

- ...

## Research Gaps

- ...
```

## Deduplication rules

- 표현만 다른 동일 주장 → 하나로 병합함.
- 같은 아이디어에 다른 근거가 추가된 경우 → 근거만 누적함.
- 서로 다른 조건에서만 성립하는 주장 → 조건을 분리해 둘 다 유지함.
- 출처가 충돌하는 수치 → 어느 한쪽을 임의 선택하지 않음.

## Quality rules

- 'AI를 사용한다' 자체를 차별점으로 취급하지 않음.
- 기존 에버랜드 서비스 대비 무엇이 달라지는지 명시함.
- 기술 가능성과 사업 효과를 분리함.
- 비용, 인프라, 개인정보, 사용자 피로, 데이터 확보 문제 포함함.
- 발표용 문구와 사실 판단을 혼동하지 않음.

## Completion report

- 읽은 Research Note 수
- 병합한 중복 항목 수
- 갱신한 파일
- 새로 발견한 주요 리스크
- 미해결 의사결정 수
