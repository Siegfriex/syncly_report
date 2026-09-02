# Agent 상태

갱신: 2026-09-02T02:14:32Z

| Agent | 역할 | Branch | HEAD | 상태 | 현재 작업 |
|---|---|---|---|---|---|
| A | Authority/Governor | claude-a/syncly-authority-governor | aeb1f6e | STANDBY → wake 대기 | C-0062 수신 후 METHOD_REVISION=MCP_FIRST_DPDD_v2.1 비준 + GO_MCP_REBASELINE + ticket DAG |
| B | Production/Materialization | claude-b/syncly-production-data | a46c878 | PAUSED (handoff) | A GO 후 MCP_ROUTE_PROBE(by_ids batch/metric_summary/period_change/...) → 3,435 enrichment; 835 bulk details 기본 중단 |
| C | Assurance/Router/Reporter | claude-c/syncly-assurance-fable | 0365f13 | **ACTIVE (재시작)** | control plane 복원 완료; RUN_RESUME_BASELINE_MCP_FIRST 발행; runtime MCP matrix 발행; Gate M0 OPEN |
| D | Independent R&D | claude-d/syncly-research-rnd | a501738 | PAUSED (handoff) | **pilot 60-call 즉시 실행 가능(C-0061 standing)** → semantic/video/VOC exhaustion, BRIDGE_CASEBOOK_6, limitation 재진단 |
| BUS | Ticket ledger | bus/syncly-ledger | 55a6840 | 정상 | 141 canonical rows / 173 tickets |

- Worktree cleanliness: root main 4ccbd94 CLEAN. B worktree 1 file dirty(outbox id 정정 미커밋, 비블로킹 — B fix-forward).
- 재시작 순서: C → A → B+D (bundle SESSION_START_COPYPASTE.md). Human은 Query 생성/수정 금지, MCP tool 선택 질문에 답하지 않음.
