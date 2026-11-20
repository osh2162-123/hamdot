---
name: hamdot-release
description: 함닷 릴리스의 버전 표기와 검증을 준비하고 승인된 배포를 확인할 때 적용합니다.
---

1. AGENTS.md와 이번 작업지시의 릴리스 범위를 확인합니다.
2. APP_VERSION과 주석 날짜, h1 small, README 첫 행, CHANGELOG 머리의 버전을 함께 바꿉니다.
3. 두 스킬의 `.claude/skills/<이름>/SKILL.md`와 `.agents/skills/<이름>/SKILL.md`를 각각 `git diff --no-index <경로1> <경로2>`로 비교해 출력과 차이가 없는지 확인합니다.
4. tests/run.html을 페이지 전체 실행 방식으로 검증하고 docs/배포전점검.md를 확인합니다. known_fail과 미확인 항목을 보고합니다.
5. 작업 담당은 파일 수정과 보고를 마칩니다. 사용자 확인 뒤 계획 담당이 dev 변경을 커밋하고 main에 반영하며 버전 태그(vX.Y)를 붙여 push합니다. 작업 담당은 .git 쓰기 명령을 실행하지 않습니다.
6. Pages 배포 완료 후 공개 주소를 강력 새로고침하여 새 버전을 확인합니다. 결과를 보고합니다.
