# Gate 현황

갱신: 2026-09-02T03:36:03Z

| Gate | 정의 | 상태 | 증거/블로커 |
|---|---|---|---|
| Gate 0 | canonical substrate (cutoff 재물질화 + exact hash + C 독립검증) | **PASS** (C-0049) | 3,435 (f8d130c2…); 재시작 시 서버 교차 재확인(A01/P02/P03 EXACT, M01 +1 기지, D00 격차 기지) |
| Gate M0 | MCP Capability Exhaustion | **CONDITIONAL PASS** (C-0070) | 14/14 tool family probe·verdict; features 72 calls·voc 25 calls로 blocker 종결; COND: OBS-0003 라벨(HUI-007)·mention 로컬 route·PROVENANCE-BEFORE-SPEND. 역량 경계 6건 확정 |
| Gate M1 | Baseline MCP Enrichment (3,435 재처리) | **CONDITIONAL PASS** (C-0078) | preview→INDEX_TEXT 전환 완료; batch/aggregate/page enrichment 전부 C 검증; targeted 전문 39·features 72; D 재진단 6건 수용(TRUE_SYNCLY_LIMIT 0); COND: A의 3,408 결정·HUI-007 라벨·lexicon v2 |
| Gate 1 | 소스 유효성 | **CONDITIONAL PASS** (C-0080) | registry 2,856 exact; T_S 6/12 전문 특성화(커머스 노출면); identity 24.1% 미해결(HUR-005); Panel v2 tier는 AD batch 후; T_C 미구축(설계 결정) |
| Gate 2 | 카테고리 유효성 | **CONDITIONAL PASS** (C-0080) | M01 유일 분모; supply STABLE; keyword-tagged membership trigger API 비관측; HUI-005 outlier 미결(변형 의무) |
| Gate 3 | 엔티티/의미/크리에이티브 | **CONDITIONAL** (C-0080) | entity 하한(CIT-10·절단); meaning NOT MEASURED(discovery만); creative NOT MEASURED(prose 도달 72.7%·classifier 없음); VOC 관측 불가 |
| Gate 4 | 비교 격자 최소 n | **CONDITIONAL** (C-0074 재평가) | pilot의 focal(NEVO/S9/S9000) video gain 2/35(상한 5.7%) → PRF-0005 희소셀 23/30 해소 불가; 플랫폼별 정량 focal 비교는 Batch 2(MM1~MM4)로; HOLD-A0013 유지; 최종 disposition은 M1과 함께 |
| Gate 5 | robustness | **CONDITIONAL PASS** (C-0080) | supply RFR 0.5% STABLE; engagement RFR 68.3% UNSTABLE(CIT-09); top-date 67.3%; 변형 의무 |
| Gate 6 | Business Activation | NOT_STARTED | Batch 1(AD)·Batch 2(MM) 이후 |

**BASELINE_BATCH_SEALED (A-0048, 03:42Z) · SAFE_TO_ROTATE (C-0083).** Baseline seal 조건: M0 + M1 + Gate 1~5 최종 disposition(PASS/CONDITIONAL/NO-GO 모두 완결) → BASELINE_BATCH_SEALED → C SAFE_TO_ROTATE → Human만 UI Query 생성.

| Gate R0~R5 (v2.2) | Language Quality / Market Attribution / Mirrored Denominator / Reception Observability / Regional Robustness / Activation Readiness | **NOT_BOUND** — A 비준(C-0091) 후 C REGIONAL_SCHEMA_FREEZE에서 구속 | R3 실패는 Supply/Translation을 막지 않음 → 'Syncly Observed Reception = NO-DECISION'; regional response RFR>25% → UNSTABLE → NO-DECISION; R1은 text/manual basis 기준(region 필드 89.1% 공백, 서버모집단 기준 B-0044) |
