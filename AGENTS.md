# Agent 상태

갱신: 2026-09-01T22:30Z

| Agent | 역할 | Branch | HEAD | 상태 | 현재 작업 |
|---|---|---|---|---|---|
| A | Authority/Governor | claude-a/syncly-authority-governor | fb556af (+미커밋 A-0013) | 활동 중 | C-0027 RECONCILE 완료(A-0013); A-0014(백로그 disposition)·LOCK/CUTOFF 비준 티켓 작성 중 |
| B | Production/Materialization | claude-b/syncly-production-data | 7bddefe | GO-wait | cutoff 재물질화 대기 (A 티켓 대기) |
| C | Assurance/Router/Reporter | claude-c/syncly-assurance-fable | 2989e84 | 활동 중 | SSOT 수리·HUR-001 판정·public reporter 부트스트랩 |
| D | Independent R&D | claude-d/syncly-research-rnd | 682bc90 | P0 standby 해제 중 | T_S/T_C 재개 방향 수신; video pilot 설계 예정 |
| BUS | Ticket ledger | bus/syncly-ledger | 09e2512 | 정상 | 92 canonical rows |

- Worktree cleanliness: 7개 worktree 정상. root main은 human의 SSOT 배치로 의도적 staged 상태(canonicalization 커밋 대기).
- Wake 토폴로지·세션 매핑은 비공개(로컬 운영 정보).
