# 09 · 출처와 claim ledger (final)
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 1. Claim ledger (수리 후)
| ID | 문장 | 강도 | 근거 계층 | 수치(분모) | 가장 강한 반례 | 허용 문구 | 금지 문구 | 추적(artifact → commit) |
|---|---|---|---|---|---|---|---|---|
| C1 | Closeness+Comfort는 NEVO만의 언어가 아니다 | USE(정성) | Hey M01/P03/P02; E CE-01; local CH3 2/41 vs 4/68 | h=−.05, TOST 실패 | CH2 skin comfort는 NEVO가 +20pp(비유의) | "카테고리 공통 benefit 언어" | "통계적으로 같다" | B_PAGE1_HEY_RESULT (c948444); E_OFFICIAL_INTENT_CODEBOOK (b55a743); D_V24R_002 (1ca0481) |
| C2 | Series 9도 이미 closeness/comfort/adaptation/functional premium을 말한다 | USE(desk) | E 공식 S9 PRO+ 코드북; Hey P03 | — | 로컬 S9 3건뿐 | "공식 Series 9 카피는 이미 …" | S9 소셜 비율 수치 | E (b55a743) |
| C3 | NEVO 차별화 후보 = 구체적 마찰 문제 / 저마찰 architecture / 유니바디 | USE(desk) + local DIRECTIONAL_NON_SIGNIFICANT | E 공식; CH6 21/41 vs 18/68 h=.51 p_BH .054; PG3 15% vs 4% | 41 vs 68 | L2: 문제 구체성 .45 < .63 | "디자인·프리미엄·플래그십 어휘가 조금 더 자주(방향성, 비유의, 유료 런칭 창)" | "소재/유니바디 프리미엄을 2배" · "유일하게 살아남은 발견" | D_V24R_002_RECOMPUTE (1ca0481); C recompute |
| C4 | NEVO 캠페인은 기능 위에 디자인/라이프스타일/행사 의미를 증폭한다 | USE WITH CAVEAT | Hey NEVO final N3–N5; N3 31/41 | ratios CI ∋ 1 | product/usage 6건 | "관측 가능한 NEVO 공급은 압도적으로 캠페인/행사 콘텐츠(31/41)" | "X배 증폭" | WP6 (19730c9/1ca0481) |
| C5 | 라이프스타일 프리미엄이 독립 외부에서 유지된다고 입증 못함(absence ≠ rejection) | USE WITH SHORT CAVEAT | Hey N2a=0; Brand cell 0/41; 비유료 외부 1 | — | 01M1EQR7Z9…(외부 화자가 NEVO RTB 반복, 1건, 음차 disclosure) | "아직 입증되지 않음" | "실패" | HEY_SYNCLY_FINAL_RAW (v2.4 bundle); B_NEVO_225_LINEAGE (85314ce) |
| C6 | Series 9도 외부에서 기능 프리미엄은 유지, symbolic은 약화 | USE(Hey-only) | Hey P03 PARTIALLY_RETAINED | — | 로컬 S9 3건 | "Hey Syncly Series 9 판독에서는 …" | 로컬 S9 감쇠 수치 | v2.4 bundle §06 |
| S1 | NEVO는 구체적 문제→메커니즘→경험을 소유해야 한다 | STRATEGIC_INFERENCE(처방) | C3 desk + 방향성 신호 | — | L2 | "소유해야 한다" | "이미 소유한다" | A_V24R_001_DELTA (99dc7c9) |
| L1–L5 | 로컬 검증 | NO_DECISION / UNDERPOWERED(+반례) / UNDERPOWERED / UNDERPOWERED / NOT_COMPUTABLE | D-V24-001 + D-V24R-002 | 위 표 | — | — | — | L_DISPOSITIONS_REISSUED.json (5373fef) |

## 2. 출처 계층
1. 공식 제품 페이지·보도자료(Braun KR/US/DE/JP; Philips; Panasonic) → 의도·스펙·가격 (E ledger 36 units, sha in `E/SHA256SUMS.txt` @ b55a743)
2. Frozen local corpus(3,435, f8d130c2) → 모든 정량 claim
3. Hey Syncly UI 최종 원문(`Braun_NEVO_Presentation_First_Final_Bundle_v2.4_20260902/evidence/HEY_SYNCLY_FINAL_RAW.md`) + B MCP 판독(41콜, raw 38 files @ c948444) → 의미 발굴·사례·반례
4. 독립 에디토리얼(GQ, Men's Health) → 삼각측량(prevalence 아님)
5. 리테일/스폰서 → 사례만

## 3. Hey/MCP evidence 마킹 (48행, `control/v24/B_EVIDENCE_MARKUP.csv`)
IN_DENOM 40(인용 가능, Tier A 5/Tier C 35) · AGGREGATE 5(맥락만) · OFF_DENOMINATOR 3(반례 계보만, 인용 불가). B의 actor 라벨은 인용 불가(mart ACTOR_v2.3.0 정답, 28/40 오류 확인).

## 4. Errata (봉인 후 정정, 역사 보존)
ERRATUM-1: CE-02 "24%"는 구성개념 명시(KR·JP 마찰 감소 / US·DE glide) · CE-08 US 가격 공백 사유(featured offer 부재) · PN-020(Amazon 역직구 KRW 가격은 US/KR 가격으로 금지) · E 계보 b55a743 재지정.
ERRATUM-2/3(recovery): "affiliate transcript" exemplar는 이제 물질화된 실제 transcript(144자)로 인용 가능하되 entity 코딩 disclosure 필수; CH6 "유일한 BH-유의 발견" 철회, C3 문구 교체; 41 inventory row kind → caption_plus_transcript.

## 5. Human 비준 대기
CORR-V24-SLIDE2: 초안 "캠페인을 걷어내자, 제품은 남았지만 Lifestyle은 약해졌다" → A 대체안 **"Brand가 만든 새 의미가 Brand 밖에서 독립적으로 확인된 사례는 아직 충분하지 않다."** (L5 NOT_COMPUTABLE, L4 ratios≈1이므로 '약해졌다'는 측정된 감쇠 주장이 되어 금지)
