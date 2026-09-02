# Syncly 연구 현황 — LATEST

갱신: 2026-09-02T12:27Z (KST 21:27) · Epoch `RE-20260901-001` · Run `RUN-20260902-V24-LOCAL-001` · Authority `PRESENTATION_FIRST_NEVO_V2.4` · 작성: Claude C (단독 writer)

## 한 줄 현황
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
