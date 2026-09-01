# syncly_report — Braun NEVO × Syncly 연구 공개 현황

Braun NEVO × Syncly 소셜 데이터 연구(4-agent harness: A=Authority, B=Production, C=Assurance, D=R&D)의 **공개 상태 보고 repo**입니다.

- 작성자: **Claude C 단독** (Assurance/Reporter). A/B/D는 이 repo에 쓰지 않습니다.
- 내용: PUBLIC-SAFE 상태 정보만 — 집계 수치, gate/phase 상태, 검증된 발견 요약. raw 코퍼스, 개별 포스트/계정 식별자, 자격증명, 내부 MCP payload는 포함하지 않습니다.

## 읽는 법
| 파일 | 내용 |
|---|---|
| [LATEST.md](LATEST.md) | 사람용 현재 현황 (여기부터) |
| [STATE.json](STATE.json) | 기계용 canonical 상태 |
| [AGENTS.md](AGENTS.md) | 에이전트별 상태/브랜치/HEAD |
| [GATES.md](GATES.md) | Gate 0~5 판정 현황 |
| [DECISIONS.md](DECISIONS.md) | 확정/대기/금지 결정 대장 |
| [FINDINGS.md](FINDINGS.md) | C 독립검증 완료 발견 |
| [HUMAN_ACTIONS.md](HUMAN_ACTIONS.md) | Human UI 확인 큐 |
| [TIMELINE.md](TIMELINE.md) | 주요 사건 시간순 |
| `reports/30min/` | 30분 주기 전체 상태 스냅샷 |
| `events/syncly_demo_commit/` | 운영 repo 커밋별 분석 (source commit ↔ event file 1:1) |
