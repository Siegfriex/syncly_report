# Agent 상태

갱신: 2026-09-02T02:48:18Z

| Agent | 역할 | Branch | HEAD | 상태 | 현재 작업 |
|---|---|---|---|---|---|
| A | Authority/Governor | claude-a/syncly-authority-governor | 28b1b56 | **ACTIVE** | A-0029: B-0027 ACK, CIT-01~05 인용 제약 동결, 808 DEFERRED |
| B | Production/Materialization | claude-b/syncly-production-data | 8ae71b9 | **ACTIVE** | checkpoint 1 VERIFIED(C-0065); 2·3(BASELINE_AGGREGATES/SOURCE_TERM) 착륙, C 검증 대기 |
| C | Assurance/Router/Reporter | claude-c/syncly-assurance-fable | 81db69e | **ACTIVE** | C-0065/0066/0067 발행; Gate M0 잔여=search_voc |
| D | Independent R&D | claude-d/syncly-research-rnd | 8934765 | **ACTIVE** | pilot 60/60 실행(PRF-0010 EXPERIMENTAL); d2 exhaustion 진행; raw/ledger/FACT_CORRECTION 부채 |
| BUS | Ticket ledger | bus/syncly-ledger | ba00313 | 정상 | 156 canonical rows |

- Worktree cleanliness: root main 4ccbd94 CLEAN. B worktree 1 file dirty(outbox id 정정 미커밋, 비블로킹 — B fix-forward).
- 재시작 순서: C → A → B+D (bundle SESSION_START_COPYPASTE.md). Human은 Query 생성/수정 금지, MCP tool 선택 질문에 답하지 않음.
