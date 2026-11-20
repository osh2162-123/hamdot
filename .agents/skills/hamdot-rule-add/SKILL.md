---
name: hamdot-rule-add
description: 함닷의 점검 규칙 R, 기관·상호명 사전, ALT_GROUPS를 추가하거나 수정할 때 적용합니다.
---

1. AGENTS.md와 작업지시를 읽고 근거 쪽수, 심각도(err/warn/info), 적용 영역, 오탐 우려 예문을 확인합니다. 빠진 근거는 교사에게 확인합니다.
2. tests/cases.json에 걸려야 할 expect와 걸리면 안 될 not 예문을 먼저 추가합니다. 실제 학생·학교 정보는 쓰지 않습니다.
3. 허가된 규칙·사전을 수정합니다. 대체 표현은 자동 적용하지 않습니다.
4. 사람은 로컬 서버의 `/tests/run.html` 또는 `https://osh2162-123.github.io/hamdot/tests/run.html`을 엽니다. 공개 주소는 배포된 코드이므로 로컬 변경은 로컬 서버에서 확인합니다. 에이전트는 작업 폴더 밖의 jsdom에서 HTTP 로컬 서버의 tests/run.html 전체와 iframe의 index.html을 실행하고 결과표와 콘솔 오류를 확인합니다. 전체·통과·실패·known_fail 수를 기록합니다. 실패가 없어야 하며, known_fail은 통과로 세지 않습니다. 범위 밖 기존 결함은 known_fail과 사유를 남겨 보고합니다.
5. CHANGELOG에 변경 이유를 적고 handoff 보고서에 결과를 기록합니다. 작업 담당은 .git 쓰기 명령을 실행하지 않습니다.
