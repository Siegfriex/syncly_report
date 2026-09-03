# Syncly 연구 현황 — LATEST

갱신: 2026-09-03T05:36Z (KST 14:36) · Run `PRESENTATION_RESULT_MAX_SPRINT_20260903_1500` · Authority sealed `FINAL_CLOSEOUT_20260903` (27535fb) · 작성: Claude C

## 한 줄 현황
**(15:08) THREE-LAYER DIAGNOSIS COMPLETE.** 가설 PARTIAL: '이미지 층 별도 존재'는 반증(실크가 기능 집합 69건 중 34건), '기능으로 회귀'도 기각(가격 정당화 27은 프리미엄 논증); 채택된 결론 = 구매 시점 언어는 닿았고 소유 기간 언어(관리 34·교체 39·고장 22 vs 공급 4/0/6)는 안 닿았으며 어느 층에도 S9 분리가 없다. Notebook QA PASS. 상세: `reports/three_layer_20260903/FINAL.md`

**(14:50) SPRINT COMPLETE — FINAL READOUT published.** 성과 정의 = 공급·화자·번역(응답 metric은 69건 기준 coverage 0.60 미달). NEVO eligible 69 unique posts, W34 34; MEDIA_EVENT 33/69, Brand 3/69; 번역 PARAPHRASE 10/INSUFFICIENT 11; Gong Yoo cohort 127(PAID 114·Creator 100·REELS 82) = 실크 35%·12년 19%·프리미엄 3% → 인지도는 샀고 가격 근거는 못 샀다; 13 claims 중 S9 분리 0. 판정·슬라이드·한계: `reports/presentation_sprint_20260903/FINAL_READOUT.md`

**(14:36) PRESENTATION RESULT-MAX SPRINT START (STOP 15:00).** 봉인된 최종 결합(KEEP 0 / OWN 0 / REPOSITION 2 / REDUCE 3 / TEST 8; 13 claims 중 NEVO를 S9에서 분리하는 claim 0; Media/Event가 10개 claim 중 8개의 dominant actor, Brand 직접 4건)에서 NEVO 런칭 캠페인 소셜 성과 리포트용 결과를 추출. A/B/D 첫 티켓 발행. 상세: `reports/presentation_sprint_20260903/RUN_START.md`

**(00:05) v2.5 CU2 PASS → EM1 실행.** 코드북 감사(D + C 교차검증 17/19): CB_v2.4.0은 comparator-neutral이 아님 — CH4·PMO 메커니즘·PG1이 Braun 기술명(NEVO Sense·SilkGlide·실크)에 편향, Philips 기술명(리프트앤컷·ComfortCut·SkinProtect) 7행은 사전에 없어 "Philips 0"은 사전 artifact. → CB_v2.5.1 수정·ENTITY_DET_v2.5.0(D). Evidence deficit matrix 확정(23 cell) → **B MCP batch 1 = get_post_details 89콜**(frozen id만; S9·Philips External×PAID를 DIRECTIONAL로 올리는 것이 목표). PF-C1: v2.3 수집 시 D00 68건이 로컬 index에서 유실(raw에 보존) → 분모 보충은 Human 결정(HUM-V25-001). Prereg v2.5 초안 68 families 채택(freeze는 coverage gate 후).

**(23:47) v2.5 CU0 PASS → CU1 FROZEN.** 3,435 안의 면도기 model universe 전수 census(D 31 family / B 920 posts / C 독립) 수렴. 판정: comparator truncation **MATERIAL**(Philips S9000/Prestige 71건이 REF에 묶여 있었음), pooled REF heterogeneity **MATERIAL**(REF 68 = Philips+수동+저가전기+클리퍼+adjacent), differential coverage **SEVERE**(verbatim NEVO 16.7% / S9 1.9% / Philips 5.6% / Panasonic 0%). Panasonic은 코퍼스에 family 자체가 없음. Comparator role 동결(outcome 미사용): S9 primary, Philips S9000/Prestige secondary, Laifen sensitivity. 다음: CU2 codebook fairness → evidence deficit matrix → EM1(MCP batch 1).

**(23:32) CYCLE 2 OPEN — v2.5 COMPARATOR UNIVERSE.** v2.4.1은 4f23c39에서 immutable(폴더 무변경 검증). 진단: Cycle 1은 comparator universe census 없이 NEVO vs S9 vs pooled REF로 좁혀졌고, Philips/Panasonic이 REF에 흡수됐을 가능성. 첫 gate CU0 = 3,435 안의 전기면도기 brand→family→model 전수 census(D) ∥ 기존 evidence 인벤토리(B). **MCP 호출은 CU0 PASS 전 금지.** A HOLD.

**(23:12) FINAL REPORT SEALED (v2.4.1).** Recovery 봉인 후 R&D/전략 case study 형식의 최종 보고서 10종 + master(`reports/final_v2.4.1/FINAL_RUN_REPORT_v2.4.1.md`)를 산출, 품질 게이트 Q1~Q13 13/13. 결론: 초기 차별점은 카테고리 공통 문법; 수리 후 BH-유의 로컬 발견 0; NEVO는 메커니즘은 말하지만 문제는 덜 말함; Brand 밖 생존은 텍스트 미수집으로 판정 불가; 결정 = NO-DECISION + targeted evidence; 처방 = '덜 괴롭히면서 깔끔한' 사용 경험 소유. Human 항목: CORR-V24-SLIDE2, gold, 제품층화 텍스트 취득, US street price.

**(23:00) RECOVERY R0~R8 CLOSED → A delta review.** CASE 2 repair(raw caption 2건 물질화, Tier A 182) 후 **CH6가 BH 유의성을 잃음**(21/41 vs 18/68, h=.51, p_BH=.054). 수리 후 로컬 BH-유의 발견은 0건이며 CH6 토큰의 2/3는 '디자인' 등 느슨한 어휘였음 → Slide 1 C3 문구를 "디자인/프리미엄/플래그십 어휘가 더 자주 보인다(방향성, 비유의)"로 강등. L1~L5·decision class(NO-DECISION) 불변. 근본 원인: verbatim 텍스트 180건이 전부 M01 회원으로 제품별 층화 없이 수집됨. A는 delta만 검토.

**(22:58) RECOVERY R0~R5 CLOSED.** 160→2 붕괴는 entity/actor가 아니라 **텍스트 수집**(verbatim 180건 전부 M01, 제품 층화 없음) 때문 → MIXED. actor 11/40은 B 자체 오류(mart 정확). Brand-authored NEVO 0은 evidence-tier artifact. **CH6는 산술은 정확하나 21건 중 14건이 '디자인' 등 느슨 토큰** → material-only는 7/40 vs 6/68(ns), Slide 1 문구 수정 필요. 남은 것: CASE 2 repair(raw caption 2건 물질화 → 표적 재계산) → R7/R8 → A delta review.

**(22:20) Human override → RECOVERY RUN.** C-V24-010은 산술 재현성은 인정되나 실행·측정 완결성 미확인으로 HISTORICALLY_SEALED_BUT_SUSPENDED. 발표 release HOLD, GUARD-V24R-001(coverage collapse: P03 176→S9 entity 160→Tier A 2) ACTIVE. B(frozen data lineage만, MCP/Hey 금지)와 D(독립 측정 파이프라인 감사)에 병렬 티켓 발행, ACK 대기, C watchdog 가동(7/12/15분 정책). A는 R1~R8 gate 전부 닫힐 때까지 HOLD.

**(22:05) RUN SEALED — PRESENTATION_EVIDENCE_PACK_SEALED.** A 최종 해석(A-0089) C 검증 6/6 PASS. **Decision class = NO-DECISION + targeted evidence** (Y축 Brand→External이 로컬에서 계산 불가). 발표는 정성 arc로 운반: ① 초기 차별점(closeness+comfort)은 카테고리 공통 문법(USE) ② 유일 로컬 수치 CH6 기능·소재 프리미엄 52.5% vs 26.5%(h=.54, CONDITIONAL) ③ 반례: NEVO는 메커니즘을 말하지만 문제를 말하지 않음 ④ Brand 밖 검증은 evidence gap. **Human 항목**: Slide 2 초안 headline 교체 비준(CORR-V24-SLIDE2), gold 평정, targeted evidence 7항. 산출: claude-c control/v24/final/*, 보고서 reports/30min/20260902/2205_final_findings.md · 2205_evidence_pack.md

**(21:42) D-V24-001 완료 → C 검증 PASS → LOCAL PAGE SEAL → A 최종 해석 release.** 로컬 검증(Tier A 180; NEVO 40 / S9 2 / 카테고리 참조 68): L1 NO_DECISION(등가 검정 불가), L2 UNDERPOWERED(+반례: NEVO는 문제보다 메커니즘을 말함), L3/L4 UNDERPOWERED, L5 NOT_COMPUTABLE(Brand cell 0). 유일하게 BH를 통과한 로컬 수치 = **CH6 Functional Premium NEVO 52.5% vs 카테고리 26.5% (h=.54, p_BH=.039, CONDITIONAL)**. C가 D 코드 없이 11/11 재계산 일치 확인. Slide 1/2/3 evidence layer 봉인(LOCAL_PAGE_SEAL_v2.4.md). A-V24-001 발행, A 세션 응답 대기. 상세: reports/30min/20260902/2142_v24_local_seal.md

**(21:25) v2.4 PRESENTATION-FIRST RE-ENTRY.** Human이 `Braun_NEVO_Presentation_First_Final_Bundle_v2.4_20260902`를 현재 권위로 확정(main 8e8c74d, 17/17 SHA). C: `PRESENTATION_FIRST_V24_REENTRY` → `GLOBAL_AGENT_REVOKE_V24`(v2.3 release 티켓 실행권한 종료, 결과는 historical evidence 보존) → input ledger SEAL(B/D/E 53행, 절대경로+sha) → **D-V24-001_LOCAL_PRESENTATION_VALIDATION 발행**(WP0~WP8, Tier A headline, Syncly CLOSED). 상태: B CLOSED · E FROZEN · A WAIT · D RELEASED · C ACTIVE. **Human**: D 세션 시작; A/B/D에게 로컬 커밋 push 요청(provenance delivery). 상세: reports/30min/20260902/2125_v24_reentry.md

**(20:25) A ACK 검증 ACCEPT → B/D/E Loop 1 RELEASE.** A-0088(`A-V23-ACK`)은 prereg sha echo 정확, threshold/RQ 변경 없음, result peeking 없음(C-V23-010, 13/13). text-coverage = (b) 제품 subset 한정 read-only 회수 + (a) coverage 공개. B(C-V23-007: P1→P2→P3-Q1..Q4, P3-Q5 HOLD, cap 120콜) · D(C-V23-008: mart → P1/P2 local, MCP 0, M4는 H1-2.1 후) · E(C-V23-009: 독립 desk, 신규 branch claude-e). A는 WAIT. **Human**: B/D/E 세션 시작 + A에게 d603955 origin push 요청. 상세: reports/30min/20260902/2025_v23_loop1_release.md

**(20:10) v2.3 RUN START — `RUN_START_V23_FROZEN_HYPOTHESIS_LOOP`(C-V23-000).** 유일 권위 = main 68f1ad3 v2.3 Final Execution Bundle; v2.1/v2.2/과거 handoff/AD 대기/Batch 1·2 DAG 전부 legacy. Gate V0 PASS(3,435/f8d130c2 등 12/12 재계산 일치, MCP 0콜). P1/P2/P3 사전등록 동결(α=.05, BH q=.05, |h|≥.20, TOST/ROPE, loop 2). A release(C-V23-006) — **Human이 A 세션을 시작해 주세요**; B/D/E는 A ACK 검증 후 HOLD 해제. E lane branch 신설은 Human 결정. 상세: reports/30min/20260902/2010_v23_run_start.md

**(17:50) 세션 종료 — 핸드오프: HANDOFF.md.** v2.2 RATIFIED·REGIONAL_SCHEMA_FREEZE 발효, AD4 screener STAGE 1 READY, AD1~AD5는 생성됐으나 서버 API 미노출(Human UI 확인 필요). 다음 세션 재시작 순서 C→A→B+D.

**(16:58) AD4 screener STAGE 1 READY.** v2.2 RATIFIED·REGIONAL_SCHEMA_FREEZE 발효, 토큰 목록 v2.2(36 검증)·affinity 어휘(AD 키워드 100, PROXY)·회귀 게이트 0/10(C/B/D 수렴) 완료. 남은 조건은 AD1~AD5 query_id 확정뿐인데 서버 API에 아직 미노출(생성 후 ~85분) — Human이 UI 진행률을 확인해 주세요. 상세: reports/30min/20260902/1700_stage1_ready.md

**(15:56) REGIONAL_SCHEMA_FREEZE-2.2.0 발행(C-0099).** A-0061이 AD spec v1.2(as-created)를 RECONCILE로 비준하고 AD4 규칙을 확장(shaving-only 소스는 패널 제외). B(C-0100)·D(C-0101) 활성 — 둘 다 0 MCP 콜, AD 데이터 접근은 C가 query_id를 서버에서 확인해 CONFIRMED 티켓을 낸 뒤. 지금 서버에는 AD 5개가 아직 미노출(수집 중) — C가 주기적으로 확인. Human 할 일 없음.

**(15:50) v2.2 REGIONAL RATIFIED(A-0059, 06:38:33Z).** Human이 AD1~AD5를 **자체 정의로 UI 생성**(A-0053 v1.1 exact와 다름) → C가 as-created를 **AD spec v1.2**로 등록하고 A에 RECONCILE 요청. Baseline 5개 전량 Archive → C canary **ADDRESSABLE**. A/B/D는 C-0096으로 정지(C 지침 전 자발 행동 금지). 다음: C가 B-0045 검증 후 **REGIONAL_SCHEMA_FREEZE** 발행 → B/D 활성 → AD query_id 포착 시 spec 대조·오염 diff → Batch 1 수집.

**(15:41) v2.2 REGIONAL DELTA가 Human 지정 유일 SSOT.** C intake 완료(C-0090), A 비준 요청(C-0091/0095) 대기 — 그 전까지 방법 권위는 v2.1. downstream만 바뀐다(Language/Market → KR mirrored MM → INTL_EN mirrored MM → market-conditioned Activation). **AD1~AD5는 재설계하지 않는다**: Human은 지금 `reports/HUR-009_AD1-AD5_UI_SHEET.md`(A-0053 exact)로 생성. B의 AD downstream 물질화만 A 비준+REGIONAL_SCHEMA_FREEZE 후. 상세: reports/30min/20260902/1540_v22_regional_delta_intake.md

**Baseline(Batch 0) SEALED → SAFE_TO_ROTATE.** 분모 3,435와 모든 enrichment·제약이 해시와 함께 봉인됐다. Baseline은 역량 지도·supply 구조·source universe·방법론 판정(vendor limit 0)을 확정했고, 사업 질문(WHERE/WHO/WHAT/HOW/PROOF)은 답하지 않았다(그럴 배치가 아니다). **이제 Human 차례**: Baseline 5개 Query Archive + AD1~AD5 생성(HUR-009). 상세: reports/30min/20260902/ 최신.

## Gate
(15:26 추가) ALT-2 기대 등급 TEST(A-0057; 결정은 HUI-006 후). Gate 4 CONDITIONAL 유지(C-0088). focal 외삽 인용은 추정량 명시(27 점/67 상한 over 471).

Gate 0 PASS · M0 CONDITIONAL PASS(종결) · **M1 OPEN(d5 대기)** · **Gate 4 CONDITIONAL** · 1/2/3/5 PENDING. HOLD-A0013·GO_PHASE2 보류 유지.

## Human에게
**HUR-009**: ① UI 확인 4건(HUR-007/008, HUI-005/007) ② AD1~AD5 생성·캡처 (A-0053 비준 완료, AD3=옵션 A; spec: claude-c control/rotation/AD_BATCH_QUERY_SPEC_SHEET_v1.md) ③ Archive는 단계적: P02 하나만 먼저 → C canary 검정 → 나머지 4개(Delete 금지). A는 B-0040의 사전승인 2건(D00 77건·ko 언어) 실행 여부를 Archive 전에 결정. 비블로킹: HUI-006, HUI-007, HUR-008. Query 생성/수정/삭제 금지. MCP tool 선택 질문에는 답하지 않아도 됨(agent 책임). 재시작 순서 C→A→B+D.

---
### (이하는 2026-09-02 08:51 KST 세션 종료 시점 스냅샷)
### (이하는 07:30 시점 스냅샷)
Phase 0 마무리 단계 — Human의 SSOT 중간보고(20260902)로 **QUERY_SOURCE_LOCK=TRUE**와 **ANALYSIS_CUTOFF=2026-08-31T00:00:00Z**가 확정되었고, B의 cutoff 재물질화와 C의 Gate 0 독립검증만 남았다. 이후 Phase 1(소스 패널·T_S/T_C·full-details·video pilot) 진입.

## 방금 일어난 일
- Human이 Q1~Q4 쿼리 설정을 UI에서 직접 검증 — 4/4 원명세 일치(MATCH). C가 서버측 대조로 정확 일치 확인 → HUR-001 CONFIRMED.
- 측정모형 개편: 단일 T 폐기 → **T_S**(소스 기반 카테고리 진입)와 **T_C**(콘텐츠 기반 타깃 친화)로 분리. A01은 post corpus에서 **계정 패널(A_SOURCE_PANEL)**로 전환.
- 승인: 절단 caption 복구용 full-details 조회(~857건), promotion/language 열거, 60건 비디오 특징 파일럿.
- A가 PRF-0005(비교 격자 희소성)에 RECONCILE 판정 — Phase 2 정량 제품비교 클레임은 Gate 4 재평가(파일럿 이후)까지 보류.

## 다음 단계
1. A: LOCK/CUTOFF 비준 티켓 + B/C/D 작업 티켓 발행
2. B: cutoff 기준 재물질화 + 정확한 데이터 해시 공표
3. C: Gate 0 독립검증(카운트·해시·소스 튜플·쿼리 멤버십·무drift)
4. Phase 1 착수 (소스 패널 → T_S census → full-details → T_C → video pilot → Gate 1~5 재평가)

## 열린 인간 확인 항목 (연구 전체는 계속 진행)
HUMAN_ACTIONS.md 참조 — 소스 패널 육안 검토(HUI-002~004), 바이럴 outlier 적합성(HUI-005), 비디오 파일럿 spot-check(HUI-006), promotion/language 표본 검증(HUI-007/008), views 부재 판별(HUR-007).

## 핵심 수치 (야간 동결 기준)
| 코퍼스 | 동결 | 라이브 UI(9/2) |
|---|---|---|
| A01 (프리미엄 타깃 소스) | 1,849 | 1,892 |
| M01 (면도 카테고리 분모) | 1,271 | 1,292 |
| P02 (Philips S9000) | 64 | 69 |
| P03 (Braun Series 9) | 179 | 186 |

라이브 증가는 쿼리 변형이 아니라 수집 성장 — cutoff 동결의 근거.
