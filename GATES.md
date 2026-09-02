# Gate 현황

갱신: 2026-09-02T02:48:18Z

| Gate | 정의 | 상태 | 증거/블로커 |
|---|---|---|---|
| Gate 0 | canonical substrate (cutoff 재물질화 + exact hash + C 독립검증) | **PASS** (C-0049) | 3,435 (f8d130c2…); 재시작 시 서버 교차 재확인(A01/P02/P03 EXACT, M01 +1 기지, D00 격차 기지) |
| Gate M0 | MCP Capability Exhaustion | **OPEN (1 blocker)** | 14/14 tools probed (get_post_features: pilot 60/60, 0 failures; 비숏폼은 feature set 없음). 잔여 blocker = search_voc exhaustion (D d2). top_influencers=EXPLORATORY_ONLY(sort inert) |
| Gate M1 | Baseline MCP Enrichment (3,435 재처리) | NOT_STARTED | B MCP_ROUTE_PROBE → aggregates/source/term/semantic/video/VOC/targeted details |
| Gate 1 | 소스 유효성(A_SOURCE_PANEL/T_S) + 콘텐츠 유효성(T_C) | PENDING | M1 이후 재판정 |
| Gate 2 | 카테고리 유효성 | PENDING | HUI-005 연동 |
| Gate 3 | 엔티티/의미/크리에이티브 신뢰성 | PENDING | pilot + enrichment 이후 |
| Gate 4 | 비교 격자 최소 n | PROVISIONAL (n≥10 정량, 미만 정성) | pilot 후 재평가; HOLD-A0013 |
| Gate 5 | robustness | CONDITIONAL PASS | Full/minus-top1/minus-top1%/minus-top-source/promotion/source-type/format/platform split 의무; RFR>25% UNSTABLE |
| Gate 6 | Business Activation | NOT_STARTED | Batch 1(AD)·Batch 2(MM) 이후 |

Baseline seal 조건: M0 + M1 + Gate 1~5 최종 disposition(PASS/CONDITIONAL/NO-GO 모두 완결) → BASELINE_BATCH_SEALED → C SAFE_TO_ROTATE → Human만 UI Query 생성.
