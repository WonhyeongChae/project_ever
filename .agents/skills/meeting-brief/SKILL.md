---
name: meeting-brief
description: Turn the current project_ever research and synthesis into a concise team meeting brief with decisions needed, unresolved conflicts, evidence gaps, owners, and next actions.
---

# Meeting Brief

## Goal

회의 직전 현재 팀 지식을 읽고, 토론보다 의사결정에 집중할 수 있는 브리프 생성함.

## Trigger examples

- 회의 준비해줘
- 오늘 회의용 요약 만들어줘
- 결정할 것만 정리해줘
- 팀 미팅 브리프 생성해줘

## Required sources

우선 다음 파일 확인함.

- `synthesis/current-summary.md`
- `ideas/revenue.md`
- `ideas/gamification.md`
- `ideas/concierge.md`
- 최근 `research/**` 문서

## Workflow

1. 현재 합의된 방향 추출함.
2. 아직 결정되지 않은 선택지 추출함.
3. 서로 충돌하는 주장과 근거 확인함.
4. 추가 조사 없이는 결정하기 어려운 항목 표시함.
5. 회의에서 반드시 결정할 항목을 우선순위 순으로 정렬함.
6. 각 항목에 추천 선택지와 판단 기준 제시함.
7. 담당자가 정해져 있으면 Owner 유지함. 없으면 `미정`으로 표시함.
8. 회의 후 바로 실행 가능한 Action Item 형식으로 정리함.

## Output

파일명:
`synthesis/meeting-YYYY-MM-DD.md`

```md
# Meeting Brief — YYYY-MM-DD

## 30초 요약

- ...

## 현재 합의

- ...

## 오늘 반드시 결정할 것

### 1. <Decision>
- 선택지 A:
- 선택지 B:
- 판단 기준:
- 현재 추천:
- 부족한 근거:

## 주요 리스크

- ...

## 추가 조사 필요

| Topic | Why | Owner | Deadline |
| --- | --- | --- | --- |
| ... | ... | 미정 | ... |

## Action Items

- [ ] ...
```

## Quality rules

- 자료 요약을 길게 반복하지 않음.
- 결정 불필요한 배경 설명 최소화함.
- 추천 의견은 근거와 함께 표시함.
- 근거 부족 시 억지 결론을 만들지 않음.
- 회의에서 바로 읽을 수 있는 수준으로 압축함.

## Completion report

- 반드시 결정할 항목 수
- 주요 리스크 수
- 추가 조사 항목 수
- 생성한 meeting brief 경로
