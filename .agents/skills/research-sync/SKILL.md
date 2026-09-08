---
name: research-sync
description: Summarize one team member's current research, notes, files, and AI conversation into a structured contest research note, preserve sources, avoid duplication, and prepare the result for the shared project_ever repository.
---

# Research Sync

## Goal

현재 사용자의 조사 결과와 AI 대화를 공모전 의사결정에 바로 활용 가능한 Research Note로 변환함.

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

1. 현재 조사 주제를 한 문장으로 정의함.
2. 관련 자료에서 다음 요소 추출함.
   - 핵심 발견
   - 근거/출처
   - 아이디어
   - 기대효과
   - 리스크
   - 반론 또는 한계
   - 추가 조사 필요 항목
3. 저장소의 기존 `research/`, `ideas/`, `synthesis/current-summary.md`를 확인함.
4. 의미상 동일한 내용이 이미 있으면 중복 기록하지 않고 차이점/보강점만 기록함.
5. 사실과 의견을 분리함.
6. 적절한 주 축을 선택함.
   - revenue
   - gamification
   - concierge
   - infrastructure
   - general
7. Markdown Research Note 생성함.
8. 사용자의 GitHub ID를 확인할 수 있으면 `research/<github-id>/` 사용함. 확인 불가 시 사용자에게 ID를 요청하거나 `research/unassigned/`를 사용하지 말고 작업을 중단함.
9. 파일명은 `YYYY-MM-DD-<short-topic>.md` 형식 사용함.
10. GitHub 쓰기 권한이 있다면 개인 브랜치 생성 후 파일 저장과 PR 생성을 우선함. 직접 main 수정은 사용자가 명시적으로 요청한 경우에만 수행함.

## Output template

```md
---
author: <github-id>
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

- 생성/수정한 파일
- 분류한 카테고리
- 중복 처리 여부
- PR을 생성했다면 PR 번호
- 추가 조사 필요 항목 수
