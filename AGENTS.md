# AGENTS.md

## Repository purpose

이 저장소는 에버랜드 AI 공모전 준비 과정에서 팀 리서치, 아이디어, 의사결정 기록을 구조화하기 위한 협업 저장소임.

## Available skills

- `.agents/skills/research-sync/SKILL.md`
  - 개인 조사 자료 및 현재 AI 대화를 요약해 `research/<github-id>/`에 저장
- `.agents/skills/team-synthesis/SKILL.md`
  - 전체 팀 조사 결과를 비교·중복 제거해 `synthesis/current-summary.md`와 필요 시 `ideas/` 문서를 갱신
- `.agents/skills/meeting-brief/SKILL.md`
  - 회의 직전 결정사항, 미해결 쟁점, 추가 조사, 다음 액션을 브리프로 정리

## Skill routing

사용자가 다음과 같은 의도를 보이면 해당 스킬을 우선 읽고 따름.

- "내 조사 정리", "대화 요약 업로드", "리서치 동기화" → `research-sync`
- "팀 전체 자료 합쳐줘", "중복 정리", "아이디어 통합" → `team-synthesis`
- "회의 준비", "회의용 요약", "결정할 것 정리" → `meeting-brief`

## Research rules

1. 사실, 가설, 제안, 리스크를 구분함.
2. 외부 자료의 출처 URL/문서명을 가능한 한 유지함.
3. 출처가 없는 숫자·시장규모·운영 사실을 임의로 확정하지 않음.
4. 기존 문서와 의미가 같은 내용은 중복 파일을 늘리기보다 기존 지식을 보강함.
5. 원문 대화를 통째로 저장하지 않고 공모전 의사결정에 필요한 내용만 요약함.
6. 개인정보, 계정정보, 불필요한 비공개 세부사항을 저장하지 않음.
7. 팀원의 의견과 외부 사실을 혼동하지 않음.

## Idea taxonomy

공통 아이디어는 우선 다음 3개 축으로 분류함.

- `revenue`: 매출 증가, 객단가, 구매 전환, 매장 분산
- `gamification`: 퀘스트, 보상, 몰입, 체류시간, 재방문
- `concierge`: 동선, 일정, 대기, 개인화 안내, 스마트 줄서기 연계

여러 축에 걸치는 아이디어는 한 문서에 억지로 중복 저장하지 않고 주 축을 정한 뒤 관련 축을 링크함.

## Git workflow

- 합의된 자료: `main`
- 개인 조사: `research/<github-id>-<yyyymmdd>`
- 통합 작업: `synthesis/<yyyymmdd>`
- 가능하면 개인 조사 변경은 PR로 병합함.
- 커밋 메시지는 `research:`, `docs:`, `idea:`, `synthesis:`, `chore:` 접두어 사용 권장.
