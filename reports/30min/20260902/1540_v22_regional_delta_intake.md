# 30분 보고 — 2026-09-02 15:40 KST — v2.2 REGIONAL DELTA intake

## 무엇이 바뀌었나
- Human이 `Braun_NEVO_Syncly_v2.2_Regional_Delta_Bundle_20260902`(v2.2 REGIONAL DELTA)를 **유일 SSOT**로 지정. C가 번들 11/11 SHA 검증 후 main **88908a0**에 정본화(원위치, root CLEAN).
- Addendum 두 표현: PDF(sha 6102e181…, "Revised Final Proposal — FINAL PROPOSAL FOR RATIFICATION", 30p/34절) ⊃ MD(sha cbb02933…, "PROPOSED SUCCESSOR ADDENDUM", 25절). 모순 없음, PDF normative. 정정 항목 **CORR-V22-MD-SYNC**(MD 재생성; Human 문서; 비준 비차단). B·D가 독립 산출한 해시가 C와 3자 일치.
- 설계 delta(downstream만): v2.1 `Target-Affinity → Global MM → Activation` ⇒ v2.2 `Target-Affinity + Language/Market Attribution → KR mirrored MM(KMM1~5) → INTL_EN mirrored MM(EMM1~5) → Market-conditioned Activation`. 신규: Language×Market 9필드, 2AB_TRADEOFF_RESOLUTION, VALUE_ROLE, HR1~HR7, Gate R0~R5, regional marts, GLOBAL CORE + KR + INTL_EN boards.

## 무엇이 바뀌지 않았나
3,435 / f8d130c2 · A-0048 SEALED · C-0083 SAFE_TO_ROTATE · cutoff 2026-08-31T00:00:00Z · MCP-first · TA1~TA5 · 2A~2E · Breadth/Depth/Persistence · RFR · Product N≠market share · search count≠prevalence · Human-only mutation · CIT-01~12 · 모든 gate 판정 · HOLD-A0013 · **AD1~AD5 = A-0053 spec v1.1 exact (재설계 금지)**.

## 권위 상태
- 방법 권위: **MCP_FIRST_DPDD_v2.1 유지** — v2.2는 A 비준(C-0091 발행 06:38Z) 전까지 PROPOSED. C는 자기 비준하지 않는다. 적용 시점: AFTER_RATIFICATION; BEFORE_AD_DOWNSTREAM_MATERIALIZATION.
- 비준 후 C 순서: authority lineage 갱신(v2.1 보존) → REGIONAL_SCHEMA_FREEZE(구속 6항: actor_type 7종·upgrade_reason 7종·KMM/EMM 역할 라벨·mart 이름 분리·regional marts=BUILD ORDER·Gate R1 text/manual basis 기준) → B(C-0092)·D(C-0093) 활성.

## 티켓
C-0090 INTAKE · C-0091 A 비준 요청 · C-0092 B 사전 할당 · C-0093 D 사전 할당 · C-0094 HUR-009 v2.2 개정+시트 · C-0095 A 보충 · 수신 B-0043/B-0044/D-0043. BUS 5c90336 (tickets 239). 브랜치: main 88908a0 · C 3c1f049 · B 8523fbd · D 8090f32 · A 112981c.

## Human 열린 액션
**HUR-009 (지금)**: AD1~AD5를 `reports/HUR-009_AD1-AD5_UI_SHEET.md`(A-0053 exact, P03 화면 필드 순서)대로 생성. Baseline Query 재생성 금지. 생성 후 query_id·tracking_since·keyword 화면·relevance 저장본·platforms·backfill·스크린샷 → C. 6번째 거부 시 중단·통보. 이후 P02 선행 Archive → C canary.
비차단: UI read 4건(HUR-007/008, HUI-005/007), HUI-006, CORR-V22-MD-SYNC.

## 다음 gate
AD 도착 → C list_data_queries 대조·오염 diff·posted-at 겹침 기록 → (A RATIFY + FREEZE 후) B 수집 release → Batch 1. Batch 2는 global MM1~5로 자동 진행 금지: LEXICON_V2_FREEZE → REGIONAL_MM_SPEC_FREEZE → HR1~7 freeze → KMM → seal → EMM → seal.
