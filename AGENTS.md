# Agent 상태

갱신: 2026-09-02T02:28:03Z

| Agent | 역할 | Branch | HEAD | 상태 | 현재 작업 |
|---|---|---|---|---|---|
| A | Authority/Governor | claude-a/syncly-authority-governor | d2ee2d3 | **ACTIVE** | GO_MCP_REBASELINE 발행(A-0023); METHOD_REVISION 비준; B/D/C 지시 DAG; GO_PHASE2 보류 |
| B | Production/Materialization | claude-b/syncly-production-data | a46c878 | RELEASED (세션 시작 대기) | A-0024: MCP_ROUTE_PROBE(field×level×cost) → aggregates → source/term → targeted evidence → mart v2 |
| C | Assurance/Router/Reporter | claude-c/syncly-assurance-fable | 0839a7b | **ACTIVE** | C-0064 ACK; Gate M0 OPEN; B/D checkpoint 독립검증 대기 |
| D | Independent R&D | claude-d/syncly-research-rnd | a501738 | RELEASED (세션 시작 대기) | A-0025: **pilot 60-call 즉시** → semantic/video/VOC exhaustion → BRIDGE_CASEBOOK_6 → limitation 재진단 |
| BUS | Ticket ledger | bus/syncly-ledger | 221ff49 | 정상 | 147 canonical rows |

- Worktree cleanliness: root main 4ccbd94 CLEAN. B worktree 1 file dirty(outbox id 정정 미커밋, 비블로킹 — B fix-forward).
- 재시작 순서: C → A → B+D (bundle SESSION_START_COPYPASTE.md). Human은 Query 생성/수정 금지, MCP tool 선택 질문에 답하지 않음.
