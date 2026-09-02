# Gate 현황

갱신: 2026-09-02T03:13:21Z

| Gate | 정의 | 상태 | 증거/블로커 |
|---|---|---|---|
| Gate 0 | canonical substrate (cutoff 재물질화 + exact hash + C 독립검증) | **PASS** (C-0049) | 3,435 (f8d130c2…); 재시작 시 서버 교차 재확인(A01/P02/P03 EXACT, M01 +1 기지, D00 격차 기지) |
| Gate M0 | MCP Capability Exhaustion | **CONDITIONAL PASS** (C-0070) | 14/14 tool family probe·verdict; features 72 calls·voc 25 calls로 blocker 종결; COND: OBS-0003 라벨(HUI-007)·mention 로컬 route·PROVENANCE-BEFORE-SPEND. 역량 경계 6건 확정 |
| Gate M1 | Baseline MCP Enrichment (3,435 재처리) | **OPEN** | B checkpoints 1-5 VERIFIED; preview→INDEX_TEXT 전환 완료; promotion 3,435/3,435; per-post-only 잔여=full_caption/transcript/video_features(3,408 무전문); D d5 limitation 재진단 대기 |
| Gate 1 | 소스 유효성(A_SOURCE_PANEL/T_S) + 콘텐츠 유효성(T_C) | PENDING | M1 이후 재판정 |
| Gate 2 | 카테고리 유효성 | PENDING | HUI-005 연동 |
| Gate 3 | 엔티티/의미/크리에이티브 신뢰성 | PENDING | pilot + enrichment 이후 |
| Gate 4 | 비교 격자 최소 n | **CONDITIONAL** (C-0074 재평가) | pilot의 focal(NEVO/S9/S9000) video gain 2/35(상한 5.7%) → PRF-0005 희소셀 23/30 해소 불가; 플랫폼별 정량 focal 비교는 Batch 2(MM1~MM4)로; HOLD-A0013 유지; 최종 disposition은 M1과 함께 |
| Gate 5 | robustness | CONDITIONAL PASS | Full/minus-top1/minus-top1%/minus-top-source/promotion/source-type/format/platform split 의무; RFR>25% UNSTABLE |
| Gate 6 | Business Activation | NOT_STARTED | Batch 1(AD)·Batch 2(MM) 이후 |

Baseline seal 조건: M0 + M1 + Gate 1~5 최종 disposition(PASS/CONDITIONAL/NO-GO 모두 완결) → BASELINE_BATCH_SEALED → C SAFE_TO_ROTATE → Human만 UI Query 생성.
