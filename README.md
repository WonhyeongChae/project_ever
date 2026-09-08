# project_ever

AI 기반 에버랜드 공모전 준비용 팀 리서치 저장소.

## 목적

- 팀원별 조사 자료와 ChatGPT/Codex 대화 요약 저장
- 아이디어를 매출 증가 / 게이미피케이션 / 컨시어지 관점에서 구조화
- 중복 조사 최소화 및 근거·리스크·후속 조사 항목 관리
- 회의 전 전체 자료를 통합한 브리프 생성

## 기본 구조

```text
project_ever/
├─ AGENTS.md
├─ .agents/
│  └─ skills/
│     ├─ README.md
│     ├─ research-sync/SKILL.md
│     ├─ team-synthesis/SKILL.md
│     └─ meeting-brief/SKILL.md
├─ research/
│  └─ README.md
├─ ideas/
│  ├─ revenue.md
│  ├─ gamification.md
│  └─ concierge.md
└─ synthesis/
   └─ current-summary.md
```

## 팀 사용 흐름

1. 저장소 clone
2. 각자 조사 또는 AI 대화 진행
3. `research-sync` 스킬로 자신의 조사 내용을 `research/<github-id>/`에 정리
4. 필요 시 개인 브랜치에서 commit/push 후 PR 생성
5. 회의 전 `team-synthesis`로 전체 자료 통합
6. `meeting-brief`로 결정 필요 사항과 다음 액션 정리

## 권장 브랜치 규칙

- `main`: 합의된 자료와 공용 문서
- `research/<github-id>-<yyyymmdd>`: 개인 조사 업로드
- `synthesis/<yyyymmdd>`: 통합 정리 작업

## 핵심 원칙

- 출처 없는 외부 사실을 확정적으로 기록하지 않음
- 기존 문서와 중복되는 내용은 새 파일을 늘리기보다 보강
- 사실 / 가설 / 제안 / 리스크를 구분
- 원문 전체 대화를 업로드하지 않고, 공모전 의사결정에 필요한 내용만 요약
- 개인식별정보, 계정정보, 비공개 대화의 불필요한 세부사항은 저장하지 않음
