---
name: research-sync
description: Summarize one team member's current research, notes, files, and AI conversation into a structured contest research note, preserve sources, avoid duplication, and save the result to that member's assigned branch in the shared project_ever repository.
---

# Research Sync

## Goal

현재 사용자의 조사 결과와 AI 대화를 공모전 의사결정에 바로 활용 가능한 Research Note로 변환하고, 반드시 지정된 개인 브랜치에 우선 저장함.

## Assigned member branches

팀 작업 브랜치는 아래 4개만 사용함.

- `wh`
- `hj`
- `gb`
- `hg`

Research Note를 `main`에 직접 저장하지 않음.
사용자의 개인 브랜치를 현재 대화나 작업 환경에서 확인할 수 없으면 `wh`, `hj`, `gb`, `hg` 중 어느 브랜치를 사용할지 먼저 확인함.
임의로 브랜치를 추정하지 않음.

## Trigger examples

- 내 조사 내용 정리해줘
- 지금 대화 리서치로 업로드해줘
- 오늘 조사한 자료 sync 해줘
- 공모전 repo에 정리해줘

## Inputs

가능한 입력 소스:

- 현재 대화
- 사용자가 첨부한 파일
- 사용자가 제공한 링크와 메모
- 사용자가 명시한 조사 결론
- 저장소에 이미 존재하는 Research Note와 아이디어 문서

현재 대화에 없는 개인 과거 대화 내용을 임의로 추정하지 않음.

## Workflow

1. 작업자의 개인 브랜치를 확인함.
   - 허용 브랜치: `wh`, `hj`, `gb`, `hg`
   - 확인 불가 시 사용자에게 브랜치 선택을 요청하고 쓰기 작업을 중단함.
2. 대상 브랜치의 최신 내용을 기준으로 작업함.
3. 현재 조사 주제를 한 문장으로 정의함.
4. 관련 자료에서 다음 요소 추출함.
   - 핵심 발견
   - 근거/출처
   - 아이디어
   - 기대효과
   - 리스크
   - 반론 또는 한계
   - 추가 조사 필요 항목
5. 대상 브랜치와 `main`의 기존 `research/`, `ideas/`, `synthesis/current-summary.md`를 확인함.
6. 의미상 동일한 내용이 이미 있으면 중복 기록하지 않고 차이점/보강점만 기록함.
7. 사실과 의견을 분리함.
8. 적절한 주 축을 선택함.
   - revenue
   - gamification
   - concierge
   - infrastructure
   - general
9. Markdown Research Note 생성함.
10. 작성자 식별자는 우선 개인 브랜치명을 사용함.
    - 예: `research/wh/`, `research/hj/`, `research/gb/`, `research/hg/`
11. 파일명은 `YYYY-MM-DD-<short-topic>.md` 형식 사용함.
12. 생성/수정 파일은 반드시 확인된 개인 브랜치에 commit함.
13. `main` merge 또는 PR 생성은 별도 요청이 있을 때만 수행함.

## Branch safety rules

- `main` 직접 commit 금지.
- 다른 팀원의 개인 브랜치 수정 금지.
- 개인 브랜치가 확인되기 전 파일 생성/수정 금지.
- 기존 개인 브랜치를 사용하며 매 작업마다 새로운 브랜치를 만들지 않음.
- 공용 문서 반영이 필요해도 우선 개인 브랜치에서 수정함.
- 이후 검토/통합 단계에서만 `main`으로 PR 또는 merge함.

## Output template

```md
---
author: <wh|hj|gb|hg>
branch: <wh|hj|gb|hg>
date: YYYY-MM-DD
topic: <topic>
category: <revenue|gamification|concierge|infrastructure|general>
status: research
---

# <Topic>

## 한 줄 요약

<핵심 결론>

## 문제 정의

- ...

## 핵심 발견

- ...

## 아이디어 / 적용 가능성

- ...

## 기대 효과

- ...

## 리스크 / 반론

- ...

## 근거 / 출처

- [자료명](URL) — 무엇을 뒷받침하는지

## 기존 팀 자료와의 관계

- 기존 아이디어 보강 / 신규 관점 / 반박 / 중복 여부

## 추가 조사 필요

- ...
```

## Quality rules

- 원문 대화를 그대로 복사하지 않음.
- 외부 사실은 가능한 한 출처 포함함.
- 출처 없는 수치 사용 금지.
- 팀원이 제안한 가설을 이미 검증된 사실처럼 표현하지 않음.
- 결론이 불확실하면 `가설`, `추정`, `검증 필요`로 표시함.
- 개인 정보와 공모전에 불필요한 사적 대화 제외함.
- 하나의 Research Note는 하나의 중심 주제를 유지함.

## Completion report

작업 후 사용자에게 다음만 간단히 보고함.

- 저장한 개인 브랜치
- 생성/수정한 파일
- 분류한 카테고리
- 중복 처리 여부
- 추가 조사 필요 항목 수
- PR/merge는 수행하지 않았는지 여부
