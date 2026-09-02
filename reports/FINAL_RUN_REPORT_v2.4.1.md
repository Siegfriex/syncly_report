# Series 9이 있는데 NEVO는 왜 필요한가?
## 3,435개 소셜 데이터를 제품 포지셔닝으로 바꾸는 분석
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

> 이 문서는 연구논문도, 감사 로그도, 마케팅 카피도 아니다. **소셜 데이터를 제품·메시지 의사결정으로 바꾼 과정을 처음 보는 사람이 재현할 수 있게** 쓴 R&D / Product Strategy case study다. 문단은 QUESTION → DATA → METHOD → FINDING → COUNTEREVIDENCE → DECISION → NEXT TEST 순서를 반복한다. 세부는 02~10 문서에 있다.

## TL;DR
(02_EXECUTIVE_SUMMARY.md와 동일) 초기 가설 "Closeness + Skin Comfort = NEVO 차별점"은 카테고리·Series 9·Philips 증거 앞에서 카테고리 공통 문법으로 강등됐다. 질문을 "Functional Premium을 넘어 별도의 problem/mechanism/experience/ownership 영역을 만드는가"로 바꿨다. 동결 코퍼스 3,435건에서 entity→증거→코드북→메시지 구조를 재구성하고 B/D 독립 분석과 C 수렴을 거친 결과, **BH를 통과한 로컬 정량 신호는 0건**, 방향성 신호(디자인·프리미엄 어휘 ↑, 문제 구체성 ↓)만 남았다. Brand 밖 생존(RQ2)은 데이터 구조상 관측 불가였다. 최종 전략: **NEVO는 Series 9이 아직 소유하지 않은 '덜 괴롭히면서 깔끔한' 사용 경험을 소유해야 한다(처방).**

---

## 1. Series 9이 있는데, NEVO는 왜 존재해야 하는가?

**A. 포트폴리오 맥락.** Braun의 최상위 전기면도기 Series 9(PRO/PRO+)이 이미 "perfect closeness & skin protection, Pro SensoAdapt, SmartCare, Made in Germany"를 말한다(E 공식 코드북). 2026년 8월 NEVO가 12년 만의 새 플래그십으로 KR 런칭했다(공유 앰버서더, 성수 행사, "실크 쉐이빙", 316L 유니바디, 최대 24% 마찰 감소 주장).

**B. 초기 가설.** "더 밀착되면서도 덜 자극적"(2AB: Closeness ∧ Skin Comfort의 trade-off 해소)이 NEVO의 고유 proposition이다.

**C. 왜 소셜 데이터로 검사했나.** 제품 컨셉이 실제 시장 언어에서 어떻게 말해지는지는 공식 카피만으로 알 수 없다. 소셜 코퍼스는 Brand, 크리에이터, 리테일, 커머스가 각자 무엇을 강조하는지 한 분모 위에서 보여준다.

**D. 가설의 반증.** Hey Syncly 최종 판독에서 M01(카테고리)·P03(Series 9)·P02(Philips) 모두 closeness·comfort·adaptation을 반복했다. E의 공식 카피 코딩(CE-01)은 Series 9 PRO+("ultimate closeness, skin comfort and precision")와 Philips i9000("day-long close shave, ultimate skin comfort")도 2AB 규칙을 충족함을 보였다. B의 MCP 판독은 Braun Thailand의 Series 9 게시물이 "프리미엄 + 밀착 + SmartCare"라는 NEVO와 같은 3부 구조를 쓰는 것을 찾아냈다(가장 강한 반례, Brand 측). 로컬에서는 2AB(CH3)가 NEVO 2/41 vs 카테고리 4/68로 거의 같았지만(h=−.05) 표본이 작아 **등가를 증명할 수도 없었다**(TOST 실패 → L1 NO_DECISION).

**E. 새 질문.** RQ1: NEVO는 Series 9의 Functional Premium 강화형에 머무는가, 아니면 specific problem → distinct mechanism → felt experience → premium ownership으로 제품 자체가 이동하는가? RQ2: 그 새 의미가 Brand 밖에서도 살아남는가(Series 9을 negative control로)? 가격/프리미엄은 제3의 RQ가 아니라 overlay다.

---

## 2. 어떤 데이터를 왜 썼나 (요약; 상세 03)
3,435건 동결 코퍼스가 유일한 측정 분모다. 그 위에 (i) 5 Query 회원(수집 맥락), (ii) 전문 텍스트 182건(Tier A, 5.3%), (iii) 203자 미리보기(Tier C), (iv) Hey/MCP 발굴 증거 48행, (v) 공식 카피·가격(E)이 각기 다른 역할로 얹힌다. Hey는 분모가 아니고, Desk는 소비자 수용이 아니다.

## 3. 원본이 분석 데이터가 되기까지 (요약; 상세 03 §2)
Raw post → 쿼리 회원 → entity 재판별(쿼리 회원 ≠ 제품) → 전문 회수 → evidence tier → 중복 family → actor(계정 증거) → promotion → 메시지 코드(Tier A만) → 분석 셀(NEVO 41 / S9 3 / REF 68) → 모델. 각 단계의 실패 모드와 guard는 03에 표로 있다. 가장 중요한 실패 모드는 **텍스트 회수 단계**였다: 전문이 있는 182건은 전부 M01 회원이고 제품별로 층화되지 않아 Series 9은 3건만 남았다.

## 4. 게시물의 말을 어떤 변수로 바꿨나 (요약; 상세 04)
감성(긍/부정)이 아니라 **무슨 문제를(Problem) 어떤 메커니즘으로(Mechanism) 어떤 결과로(Outcome) 푼다고 말하는가**를 코딩했다. 카테고리 위생 코드 CH1–CH6, 프리미엄 문법 PG0–PGX, PMO 3축 + 완결성, 캠페인 층 N1–N4. 코드북은 라벨 계산 전에 동결됐고(CB_v2.4.0), 규칙 기반 문자열 매칭이라 결정적이다.

## 5. 어떤 모델과 통계를 왜 썼나 (요약; 상세 04 §3)
두 메시지 공급 모집단의 비율 차이(two-proportion + Cohen's h + 부트스트랩), 6개 코드 동시 검정의 거짓 발견 통제(BH-FDR q=.05), "차이 없음" 주장의 등가검정(TOST ±.20), repost 편향 제거(family dedup·top-source 제거), 플랫폼 층화, Brand→External 상호작용(product × actor logistic; Brand cell 0으로 계산 불가), 캠페인 탈오염(product/usage vs event 비율).

## 6. 모델링 요약표

| ANALYTICAL QUESTION | UNIT | MODEL/TEST | N | RESULT | EFFECT | STATUS | BUSINESS INTERPRETATION |
|---|---|---|---|---|---|---|---|
| Closeness+Comfort는 NEVO 고유인가? (L1) | NEVO Tier A vs 카테고리 참조 | CH3 비율 + TOST(h ±.20) | 41 vs 68 | 2/41 vs 4/68 | h=−.05 | NO_DECISION | 카테고리 공통 가설은 유지되나 등가로 "증명"되진 않음 |
| 기능·소재 프리미엄을 더 말하는가? (C3 local) | 동일 | CH6 two-proportion + h + BH(6검정) | 41 vs 68 | 21/41 vs 18/68 | h=.51, p=.009, **p_BH=.054** | DIRECTIONAL (비유의) | 디자인·프리미엄·플래그십 어휘가 조금 더 잦음; 21건 중 14건은 '디자인' 등 느슨 토큰 |
| 구체적 문제를 더 소유하는가? (L2) | 동일 | PMO_COMPLETE 비율 + 축 평균 | 41 vs 68 | 2/41 vs 3/68; 문제 구체성 .45 vs .63 | h=.03 | UNDERPOWERED + 반례 | NEVO는 메커니즘을 말하지만 문제는 카테고리보다 덜 말함 |
| 프리미엄 문법이 S9과 다른가? (L3) | NEVO vs S9 | — | S9 Tier A 3 | 계산 금지(GUARD) | — | UNDERPOWERED | 로컬 S9 비교 불가; 카테고리 대비 PG1 37% vs 18%(h=.45, p_BH .06) 방향만 |
| 캠페인이 프리미엄 문법을 증폭하는가? (L4) | NEVO 내 N1 vs N2∪N3 | Campaign Amplification Ratio + 부트스트랩 | 6 vs 32 | PG1 1.22 [0.47, 3.00]; PG3 0.94 | CI가 1을 포함 | UNDERPOWERED | product/usage 층이 6건뿐 |
| Brand→External 감쇠가 S9보다 큰가? (L5) | product × actor | logistic β3 | Brand cell 0/41, 0/3 | 계산 불가 | — | NOT_COMPUTABLE | 모델 실패가 아니라 필요한 cell이 데이터에 없음 |
| Series 9 cell은 왜 3인가? (R2) | P03 176 → S9 entity 154 → Tier A 3 | 행 단위 lineage(B/D 독립) | 176 | 22 entity-neg + 151 미리보기만 + 3 | — | MIXED | 분석이 아니라 텍스트 수집 설계의 한계 |

## 7. 데이터가 실제로 말한 것

### 7.1 살아남은 것
- 초기 차별점(closeness+comfort)은 카테고리 공통 문법이다 — Hey·공식 카피·로컬 방향 모두 일치(정성 USE).
- NEVO Tier A 메시지에는 디자인·프리미엄·플래그십 어휘가 카테고리보다 조금 더 자주 나온다(21/41 vs 18/68, h=.51) — **방향성, 비유의**, 느슨한 구성개념. 소재 특정 어휘(유니바디·스테인리스)만 세면 6~7/41 vs 3~6/68로 더 약하다.
- NEVO의 관측 메시지 공급은 런칭 캠페인 공급이다: 유료 39/41, 앰버서더/행사 31/41, Brand 저작 전문 0, 비유료 외부 1.

### 7.2 약해진 것
- "NEVO는 구체적 문제(반복 패스·턱/목 마찰)를 소유한다"는 공식·에디토리얼 카피에는 있지만 NEVO 자신의 소셜 언어에는 아직 없다(문제 구체성 .45 < .63; 같은 단위 완결 chain 2/41).
- 수리 전 "유일하게 BH를 통과한 로컬 발견"(CH6 p_BH=.039)은 미물질화된 전문 1건을 추가하자 p_BH=.054로 문턱을 넘지 못했다. **하나의 게시물이 결론을 바꿀 수 있는 표본 크기**라는 사실 자체가 한계다.

### 7.3 아직 답할 수 없는 것
- Brand 밖 생존(RQ2): Brand 저작 NEVO 전문 0건, 비유료 외부 전문 1건(SUSPECTED) → 어느 방향으로도 증거가 없다. Hey 최종 판독도 "clean independent external = 0 식별"이었다.
- NEVO vs Series 9 정량 비교: S9 전문 3건(그중 1건은 '내비/내보'로 쓰인 NEVO 글).
- 소비자 반응: 댓글/VOC가 관측되지 않았다. 가격 수용도 마찬가지.
- 등가(같다) 주장: 표본이 등가검정 마진(±.20)보다 넓다.

## 8. Worked examples — 21/41은 어떻게 만들어졌나 (상세 05 §4)
| post | 원문(발췌) | entity | actor / promo | CH | PG | PMO | 역할 |
|---|---|---|---|---|---|---|---|
| 01M0HQ7G21… (IG, #광고) | "단순한 절삭력보다 여러 번 지나갔을 때 피부에 닿는 느낌 … 실크 글라이드 포일 … 스테인리스 스틸 316L 유니바디" | NEVO | Other / PAID | CH1·CH2·**CH6(소재)** | PG3 | 3/3/3, 완결 | **SUPPORT**: 문제→메커니즘→결과가 한 단위에 있는 드문 예 |
| 01M0HQHV2X… (Reels, 행사 리포스트) | "성수동 쎈느 … 공유, 노홍철 … 기술력과 모던한 디자인을 담아낸 네보" | NEVO | Creator / PAID | CH2·**CH6('디자인'만)** | PG4 | 0/1/2 | **AMBIGUOUS**: CH6 hit이지만 소재·내구 주장 없음 — 느슨한 경계의 대표 사례 |
| 01M1EQ8GVF… (IG, Braun Thailand) | "ยกระดับกิจวัตรเดิม…ให้พรีเมียมกว่าเดิม Braun Series 9 … แนบสนิท … SmartCare" | BRAUN_S9 | Brand / PAID | (Tier C: 코드 없음) | — | — | **COUNTEREXAMPLE**(Hey): Brand 스스로 S9에 프리미엄+밀착+케어 3부 구조를 씀 |
| 01M1EPJKA1… (Twitter) | "가격 선 씨게넘었네 … 공유로 광고모델 바꾸고 … 별로 바뀐것도 없어보이는구만 … 가격 두배" | BRAND_ONLY | Other / ORGANIC | (Tier C) | — | — | **COUNTEREXAMPLE**(정성, n=1): 차별성 부정 + 가격 반론을 동시에 하는 유일한 유기적 발화 |
| 01M0X8S8WP… (FB, 수리로 Tier A) | "면도할 때의 느낌은 9보다 훨씬 더 스무스하고 잘 깍인다. 기변할만한 확실한 차이." | NEVO | Other / PAID | 없음 | PG_NONE | 1/0/2 | **SUPPORT(정성)**: 기존 S9 사용자의 전환 사유 — 그러나 CH 토큰이 없어 CH6 분모만 41로 늘림(p_BH .039→.054) |
| 01M1EQR7Z9… (YT Shorts, 제휴, 수리로 Tier A: 자막+실제 발화 144자) | "브라운 시리즈 9 내비 면도기 … 실코 글라이드 포일이 피부 마찰을 24%나 줄여줘서" | **BRAUN_S9**(lexicon) / 실질 NEVO | Other / PAID | CH1·CH2 | PG0 | 1/3/3 | **AMBIGUOUS**: NEVO의 RTB를 외부 화자가 반복하지만 제품명이 음차로 왜곡('내비/내보'); detector는 S9로 코딩 |

## 9. 초기 가설 → 수정된 이해
| 단계 | 가설 | 증거 | 결과 |
|---|---|---|---|
| 초기 | 2AB(closeness∧comfort)가 NEVO 차별점 | M01/P03/P02 Hey + E CE-01 | 카테고리 공통 문법으로 강등 |
| 수정 1 | 소재·유니바디·기능적 프리미엄이 차별점 | CH6 21/40 (p_BH .039) | 수리 후 21/41 (p_BH .054), 구성개념 느슨 → 방향성으로 강등 |
| 수정 2 | NEVO는 구체적 문제를 소유한다 | PMO: 문제 구체성 .45 vs .63 | 아직 아니다 — 처방으로 전환 |
| 수정 3 | 새 의미는 Brand 밖에서 약해진다 | Brand cell 0, 외부 비유료 1 | 관측 불가 — evidence gap으로 진술 |

## 10. 제품 컨셉과 포지셔닝 (상세 06)
관측(현재 소셜 언어)과 처방(소구 전략)을 분리한다. **관측:** NEVO는 카테고리와 같은 benefit 어휘 위에 디자인·프리미엄·행사 의미를 얹어 말한다; 메커니즘은 말하고 문제는 덜 말한다. **처방:** "더 세게 깎는 면도기가 아니라, 같은 부위를 덜 괴롭히는 플래그십" — Specific Problem(턱/목 반복 패스) → Distinct Mechanism(SilkGlide 저마찰) → Felt Experience(덜 건드리고도 깔끔) → Premium Ownership(유니바디·케어 루틴) → Price Justification. 각 단계의 evidence anchor는 06에 있다.

## 11. 다음 validation (상세 07)
근본 원인이 텍스트 수집 설계였으므로 다음 단계는 분석이 아니라 취득이다: 제품별 층화 verbatim 수집 → NEVO 음차 lexicon → 사람 gold 라벨링(180행 frame) → 비유료·Brand 저작 NEVO 전문 → 리뷰어 검증 질문(Series 9 사용자가 어디서 차이를 느끼는가) → US 동일일자 가격.

## 12. 결정 지도
v2.4 §07: Distinct+Retained→AMPLIFY · Distinct+Weak→RE-EXPLAIN · Weak+Retained→PORTFOLIO REPOSITION · Weak+Weak→REPOSITION/TEST · **Insufficient|Any→NO-DECISION + targeted evidence** ← 현재.

## 13. 하네스 (상세 08)
A(최종 해석) / B(Hey·MCP 발굴 → 이후 frozen data 계보) / C(단독 writer·게이트·수렴 판정) / D(로컬 측정) / E(공식·가격 desk). "AI 여러 명"이 아니라 **병렬 독립 분석 + 적대적 검증 + 중앙 조정**이다: B와 D가 같은 176행 lineage를 독립 재구성 → C가 3행을 행 단위로 판정 → D가 통계 → E가 의도·가격 맥락 → A가 sealed evidence만 보고 판정 → C가 claim-evidence gate 후 작성.

## 14. 추적 가능성 (상세 08 §3, 09)
Slide 1 두 번째 beat → C3 / CH6 → 21/41 vs 18/68 → `TIER_A_LABELS_v2.4_RECOMPUTED.csv` → CB_v2.4.0 → post_id 목록 → claude-d 1ca0481 → C 재계산(`VERIFICATION_*`) → f8d130c2.

## 15. 한계는 결과 옆에 (각 결과의 MEANS / DOES NOT MEAN은 05·06에 병기)

## 16. Final takeaways
- Closeness + Comfort는 NEVO의 독점 언어가 아니었다.
- NEVO에서 가장 강했던 관측 신호(기능·소재 프리미엄)는 수리 후 유의성을 잃었고, 실체는 '디자인·프리미엄' 어휘였다. 남은 것은 방향뿐이다.
- NEVO의 소셜 언어는 메커니즘은 말하지만 구체적 문제는 아직 소유하지 않았다.
- Lifestyle/Brand→External retention은 현재 데이터로 판정할 수 없다 — 없어서가 아니라 텍스트가 수집되지 않아서다.
- 따라서 NEVO는 더 많은 기능보다 구체적인 사용자 문제와 felt experience를 소유해야 한다(처방).
- 소셜 데이터는 concept signal이었고, 다음 단계는 제품별로 층화한 텍스트 취득과 targeted external validation이다.

---

# 부록 A — Executive Summary
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## TL;DR
우리는 처음에 **"더 밀착되면서도 덜 자극적인 면도"(Closeness + Skin Comfort)**가 NEVO의 차별점이라고 가정했다. 그러나 카테고리(M01), Series 9(P03), Philips(P02)의 소셜 메시지와 공식 카피를 나란히 놓자 그 조합은 프리미엄 전기면도기라면 누구나 말하는 **카테고리 공통 문법(category hygiene)**이었다. 그래서 질문을 바꿨다. **"NEVO는 더 좋은 Series 9인가, 아니면 면도기를 새로운 problem→mechanism→experience→ownership 영역으로 옮기는 제품인가?"** 동결된 3,435건 소셜 코퍼스에서 entity → 증거 → 코드북 → 메시지 구조를 다시 세우고, B(데이터 계보)와 D(측정 파이프라인)가 독립적으로 같은 데이터를 재구성한 뒤 C가 행 단위로 수렴시켰다. 그 결과 **BH 다중검정을 통과한 로컬 정량 신호는 하나도 남지 않았다.** 방향만 남았다: NEVO의 Tier A 메시지에는 디자인·프리미엄·플래그십 어휘가 카테고리보다 조금 더 자주 보이고(21/41 vs 18/68, h=.51, p_BH=.054), 메커니즘(SilkGlide, 유니바디)은 자주 말하지만 **그 메커니즘이 푸는 구체적 문제는 카테고리보다 덜 말한다**(문제 구체성 .45 vs .63). **Brand 밖에서 새 의미가 살아남는지(RQ2)는 관측 자체가 불가능했다** — Brand 저작 NEVO 게시물 7건은 전부 미리보기만 있고, 비유료 외부 게시물은 1건뿐이다. 근본 원인은 분석이 아니라 **텍스트 수집 설계**였다: 전문(verbatim) 텍스트가 180건만, 전부 M01 쿼리 회원으로, 제품별 층화 없이 수집됐다. 따라서 최종 전략은 하나의 문장이다: **"NEVO는 더 많은 기능이 아니라, Series 9이 아직 소유하지 않은 '같은 부위를 덜 괴롭히면서 깔끔한' 사용 경험을 소유해야 한다 — 이것은 관측이 아니라 처방이다."**

## 세 슬라이드에 남는 것
| 슬라이드 | 질문 | 남는 문장 | 근거 계층 | 상태 |
|---|---|---|---|---|
| 1 | Series 9이 있는데 NEVO는 왜 존재하는가? | "Closeness+Comfort는 NEVO만의 언어가 아니었다" | Hey(M01/P03/P02) + 공식 카피(E) | USE |
| 1 (2nd beat) | 무엇이 후보로 남는가? | "디자인·프리미엄·플래그십 어휘가 카테고리보다 조금 더 자주 보인다 — 방향성, 비유의" + 반례 "메커니즘은 말하지만 문제는 덜 말한다" | 로컬 Tier A 41 vs 68 | DIRECTIONAL |
| 2 | 새 의미가 Brand 밖에서 살아남는가? | "Brand가 만든 새 의미가 Brand 밖에서 독립적으로 확인된 사례는 아직 충분하지 않다" (Human 비준 대기) | Hey 최종(N2a=0) + 로컬 cell 0/41 | NOT_COMPUTABLE |
| 3 | 그렇다면 무엇을 팔아야 하는가? | "더 좋은 면도가 아니라, Series 9이 아직 소유하지 않은 사용 경험" | 공식 intent(E) + 방향성 신호 + 반례(L2) | PRESCRIPTIVE |

## 결정 클래스
**NO-DECISION + targeted evidence.** v2.4 §07 결정 지도에서 어느 한 축이라도 "insufficient"면 quadrant를 강제하지 않는다. Y축(Brand→External)이 계산 불가이고, X축에는 수리 후 BH-유의 로컬 발견이 0건이다. 발표는 정량 판정 대신 **"초기 가설이 데이터에 깨지고 존재 이유를 다시 정의한 과정"**을 운반한다.

## 이 결과가 의미하는 것 / 의미하지 않는 것
- MEANS: 관측된 메시지 공급(paid 39/41, 런칭 2주)에서 NEVO는 카테고리와 같은 benefit 어휘를 쓰고, 디자인·프리미엄 어휘를 조금 더 쓴다.
- DOES NOT MEAN: 소비자가 NEVO를 더 프리미엄하다고 인식한다 · 시장점유율 · 구매 선호 · 인과 · Series 9과의 정량 비교(S9 Tier A = 3, 판단 불가).

## 다음 검증
1) 제품별로 층화한 verbatim 텍스트 수집(근본 원인 해소) 2) NEVO 음차(내비/내보) lexicon 3) 사람 gold 라벨링(180행 frame 존재) 4) 비유료·비Brand NEVO 텍스트 5) Brand 저작 NEVO 전문 6) US 동일일자 street price. 전부 신규 취득이 필요하다(현재 Syncly CLOSED).

---
# 부록 B — 데이터와 측정 방법
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 1. 데이터 레이어 — 각 층은 다른 질문에만 답한다

| DATA LAYER | SOURCE | ROLE | N | PERIOD | 답할 수 있는 것 | 답할 수 없는 것 |
|---|---|---|---|---|---|---|
| Frozen social corpus | Syncly 수집 5 Query의 cutoff 기준 canonical union, `posts_cutoff.jsonl` (sha f8d130c2…) | **측정 분모**(statistical inference의 유일한 모집단) | 3,435 posts / 2,856 sources | 2026-07-31 ~ 2026-08-30 (cutoff 08-31T00Z) | 메시지 공급의 구성(플랫폼·actor·promotion·코드 비율), 로컬 통계 | 소비자 반응, 시장점유율, 인과 |
| Query membership | D00_NEVO 184 · A01 Premium Lifestyle 1,816 · M01 Male Shaving 1,243 · P02 Philips 63 · P03 Series 9 176 (겹침 47) | **수집 맥락 라벨**(covariate). 제품 진실값 아님 | 3,482 memberships | 동일 | "어느 쿼리로 들어왔나" | "이 글이 무슨 제품 글인가"(entity detector가 답함) |
| Verbatim evidence layer (Tier A) | D 스냅샷 149 + B full_details 27 + casebook 16 + 수리로 추가 2 → 182 (중복 제거) | **코드북 라벨링의 유일한 텍스트 기반**(headline 수치) | 182 (5.3%) · NEVO 41 · S9 3 · 카테고리 참조 68 | 동일 | 메시지 코드 비율 | 나머지 94.7%의 메시지(203자 미리보기는 판단 불가) |
| Preview / index text (Tier C) | 각 게시물 203자 미리보기('...' 절단) | entity 검출 감도, coverage 회계 | 3,253 | 동일 | "이 글이 NEVO/S9 글인가"(재현율 79.8% 하한) | 코드 라벨(축 flip 47.3%) |
| Video / feature evidence | get_post_features 원본 60 (분석기 생성 텍스트) | 보조. Tier A 아님(발화 원문이 아님) | 60 | 동일 | 크리에이티브 유형 참고 | 코드 라벨 |
| Hey Syncly / MCP discovery | Hey UI 최종 원문(NEVO 277/122 traceable, S9 186/116, M01 1,166/29, P02 67/36, A01 1,714/0) + B의 MCP read-only 41콜, 48 evidence rows | **가설 생성·exemplar·반례 발굴** | 48 rows (IN_DENOM 40 / AGGREGATE 5 / OFF_DENOM 3) | 동일 | "이런 패턴이 있다/없다"의 사례 | 비율·prevalence·분모 |
| Desk official evidence (E) | Braun KR/US/DE/JP 공식 페이지·보도자료, Philips/Panasonic 공식, GQ/Men's Health | **OFFICIAL_INTENT**(제품이 말하려는 것)와 사실 맥락 | 36 evidence units · 31 코딩 카피 · 7 campaign rows | 2026-09-02 수집 | 공식 의도, 스펙, 캠페인 언어 | 소비자 수용(reception) |
| Price normalization (E) | 공식 MSRP/UVP + 동일일자 street price, 세금·환율(ECB 2026-09-01) 분리 | **가격 overlay**(제3의 RQ 아님) | 20 rows, KR/US/DE/JP | 2026-07-02 ~ 09-02 | 시장별 NEVO/S9 배수 | 단일 글로벌 배수(불가), US street(NOT_COMPUTABLE) |

**왜 Hey와 Local의 역할이 다른가.** Hey Syncly(및 MCP 의미 검색)는 서버 측 전문을 읽어 "어떤 말이 있는지"를 찾아내지만, 검색 결과 수는 표본이 아니라 검색기의 반환량이다. 그래서 Hey는 가설·사례·반례를 공급하고, 숫자는 항상 frozen corpus의 분모 위에서만 계산했다. Desk 자료는 "제품이 말하려는 것"이지 "시장이 받아들인 것"이 아니므로 `OFFICIAL_INTENT`로 분리해 코딩했다.

## 2. 파이프라인 — 원본 게시물이 분석 셀이 되기까지

```
Raw post (3,435)
 → Query membership (수집 맥락 라벨)
 → Entity detection (ENTITY_DET_v2.4.0)        NEVO 225 · BRAUN_S9 157(+3 NEVO_AND_S9) · PHILIPS_S9000 84
 → Text / evidence recovery (verbatim 보유?)    Tier A 182 · Tier C 3,253
 → Evidence tier (A: 전문 보유 / C: 미리보기)
 → Message-family dedup (M5)                    3,091 families (최대 94)
 → Actor (ACTOR_v2.3.0, 계정 증거)              Brand 51 · Retail 76 · Commerce 122 · Media 56 · Reviewer 71 · Creator 780 · Other 2,279
 → Promotion (server enumeration)               PAID 2,554 · ORGANIC 670 · SUSPECTED 211
 → Message codes (CB_v2.4.0: CH / PMO / PG / N) Tier A만
 → Analytical cell                              NEVO 41 · S9 3 · REF 68
 → Statistical model                            two-proportion + h + BH; TOST; ladder; (Product×Actor: 계산 불가)
```

| 단계 | INPUT | TRANSFORMATION | OUTPUT | 왜 필요한가 | FAILURE MODE / GUARD |
|---|---|---|---|---|---|
| Query membership | 5 Query의 수집 로그 | post_id ↔ query_id 조인, membership hash 5/5 재현 | `child_query_membership` | 수집 맥락은 covariate로만 | 쿼리 회원 = 제품으로 오인 → **entity detector로 재판별** |
| Entity detection | 미리보기 또는 전문 | NFKC·casefold, 한국어 공백무시 substring, Latin `\b` 경계, S9⊂S9000 마스킹, Braun 단독 금지 | `product_entity` | P03 176 중 22건은 S9 토큰이 없다(NONE 9, 브랜드만 12, 타사 1) | `s9`가 `s9000`에 매칭 → 회귀 테스트 10/10; CJK 인접 Latin `\b` 불발(1건, 로그); 음차 내비/내보 미포함(1건, 로그) |
| Text recovery | B full_details, D 스냅샷, casebook, B raw MCP 응답 | 원문 파일 sha 기록, post_id 중복 제거 | `TIER_A_INVENTORY` 182 | 코드 라벨은 절단 텍스트로 만들 수 없음(축 flip 47.3%) | 스냅샷 `transcript` 필드는 boolean이라 41행 kind 오기재(수치 무영향, 정정); B raw 디렉터리 미스캔 → 2건 누락(수리) |
| Evidence tier | 보유 텍스트 종류 | A = verbatim 보유, C = 미리보기 | `evidence_tier` | headline 숫자는 A에서만 | 사전등록 규칙(post-result 변경 0)이지만 **수집이 제품별 층화되지 않아** S9는 3건뿐 |
| Dedup | 정규화 해시·URL·MinHash·임베딩 | 메시지 family id | `message_family_id` | 같은 카피의 repost가 비율을 부풀림 | v2.4에서 v2.3 family를 재사용(재계산 아님, 공개) |
| Actor | handle·display name·창 내 게시수 | 규칙 순서 Brand→Retail→Commerce→Media→Reviewer→Creator(≥2)→Other | `actor_type` | Brand→External 비교의 축 | 게시물 내용으로 역할을 읽으면 오분류(B의 Hey 경로 라벨 40행 중 28행 오류 → 계정 증거 기반 mart가 정답) |
| Promotion | 서버 열거(ORGANIC·SUSPECTED 전수, PAID 보수) | 분할 검정 PASS | `promotion` | paid 캠페인 공급과 유기적 공급 분리 | 서버 라벨은 sentiment가 아님 |
| Codes | Tier A 텍스트 | 규칙 기반 문자열 매칭(CB_v2.4.0, 라벨 전 동결) | CH1–6, PMO, PG, N | 감성이 아니라 "무슨 문제를 어떤 메커니즘으로" | CH6 lexicon에 '디자인' 등 일반 형용사 포함 → 느슨한 경계(공개) |
| Cell | 코드 + entity + tier | NEVO / S9 / REF(M01∪P02 내 타 프리미엄 면도기) | 41 / 3 / 68 | 비교의 단위 | S9 3 → 어떤 NEVO-vs-S9 수치도 금지(GUARD-V24R-001) |

## 3. 동결과 재현
- 분모 3,435와 5개 membership hash, promotion 분할, source 2,856, A_SOURCE_PANEL 1,574는 C가 두 Run에서 독립 재계산해 12/12 일치했다.
- 모든 헤드라인 수치는 D가 계산하고 C가 D 코드를 쓰지 않고 재계산했다(수리 전 11/11, 수리 후 CH1–6·PMO·PG·N·cell 전부 일치).
- 두 독립 lane(B: 데이터 계보, D: 측정 파이프라인)이 P03 176행의 lineage를 각자 재구성해 stage별 rowset sha로 비교했다. STAGE1에서 3행이 어긋나 행 단위로 판정했고(2건 B 구현, 1건 spec 한계), Tier A·headline-eligible 집합은 두 lane과 C가 동일했다.

---
# 부록 C — 코드북과 모델링
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 1. 왜 감성 분석을 메인 변수로 쓰지 않았나
제품 컨셉 검증에서 중요한 것은 "좋다/나쁘다"가 아니라 **무슨 문제를, 어떤 메커니즘으로, 어떤 결과로 푼다고 말하는가**다. 게다가 이 코퍼스는 74%가 유료(PAID)라 "긍정률"은 소비자 감정이 아니라 브랜드가 산 메시지의 톤이다. 그래서 감성은 부속 변수(`message_valence` vs `observed_evaluative_sentiment`로 이름을 분리)로만 두고, 메시지 구조 코드를 메인으로 삼았다.

## 2. 코드북 (CB_v2.4.0 — 라벨 계산 전 동결, 규칙 기반 문자열 매칭, Tier A 텍스트만)

### 2.1 Category Hygiene — "이 말은 카테고리 누구나 하는가?"
| CODE | BUSINESS MEANING | OPERATIONAL DEFINITION | POSITIVE EXAMPLE | HARD NEGATIVE | COMMON CONFUSION |
|---|---|---|---|---|---|
| CH1 Closeness | 밀착·깔끔한 절삭 결과 | v2.3 2A 어휘(밀착, 깔끔, close shave, -0.12mm…) | "깔끔하게 밀착 면도" | 가격·행사만 언급 | '깔끔' 단독은 디자인 묘사일 수 있음 |
| CH2 Skin Comfort | 자극·마찰·편안함 | 2B 어휘(자극 없이, 쏠림, 마찰, 편안, irritation…) | "피부가 하나도 안 당겨서" | 스펙 나열 | 제3자 젤·루틴이 해결하는 comfort(NEVO 무관) |
| CH3 Closeness–Comfort Resolution | 둘을 한 단위에서 trade-off 해소로 말함 | 2AB 구조 규칙(부정된 비용/양보/거부 연결) | "피부 쏠림 없이 **깔끔하게**" | CH1과 CH2가 따로 나열됨(각주 분리) | 나열(co-statement) vs 해소(resolution) |
| CH4 Adaptive Tech RTB | 센서/적응 메커니즘을 근거로 제시 | 2D 어휘 + 기술 alias(NEVO Sense, AutoSense…) hit | "수염 밀도를 감지해 출력을 조절" | 일반 '기술력' | 공식 alias 없으면 잡히지 않음(공식 어휘 편향) |
| CH5 Convenience | 세척·충전·휴대 | 2C 어휘 | "7 in 1 스마트케어 센터" | — | — |
| CH6 Functional/Material Premium | 소재·마감·내구·플래그십을 평가 근거로 | 2E 어휘 − 라이프스타일 토큰(선물, 감성) | "스테인리스 스틸 316L 유니바디" | "프리미엄" 단독(→PGX) | **'디자인', '플래그십', '프리미엄' 같은 일반 형용사가 포함되어 경계가 느슨함**(NEVO 21건 중 14건이 이 토큰만으로 hit) |

### 2.2 Premium Grammar — "프리미엄을 어떤 문법으로 말하는가" (단일값, 우선순위 PGX > PG2 > PG4 > PG3 > PG1 > PG0)
| CODE | BUSINESS MEANING | OPERATIONAL DEFINITION | POSITIVE EXAMPLE | HARD NEGATIVE | CONFUSION |
|---|---|---|---|---|---|
| PG0 Functional Only | 기능만 | CH hit 있고 프리미엄/정체성/디자인/라이프스타일 토큰 없음 | 스펙형 리셀러 글 | — | — |
| PG1 Experience Premium | 감각 경험 프리미엄 | 실크/부드러운 경험/느낌 + 같은 단위의 기능 앵커 | "실크처럼 매끄럽습니다" | 앵커 없는 '실크' 브랜드명 | 캠페인 슬로건 "실크 쉐이빙"이 자동 hit |
| PG2 Identity Premium | 자기표현·지위 | 품격/자존감/statement/heirloom | — | — | NEVO 0건, 참조 2건 |
| PG3 Design Object | 산업디자인·소재 오브제 | 유니바디/스테인리스/316L/일체형/오브제 | "이음새 하나 없이" | '디자인' 단독 | 소재 목록이 타이트 → 6/41 |
| PG4 Lifestyle Tech | 루틴·가젯 프레임, 메커니즘 없음 | 루틴/EDC/데일리 | "매일의 면도 루틴을 새롭게" | 메커니즘 주장 동반 | — |
| PGX Unsupported Premium | 근거 없는 프리미엄 어휘 | 프리미엄/럭셔리/명품 단독 | — | — | NEVO 0건 |

### 2.3 Problem → Mechanism → Outcome (0–3 척도, 코딩 전 정의)
- problem_specificity: 0 없음 / 1 일반("면도가 불편") / 2 조건 명명(목 라인, 억센 수염) / 3 조건 + 실패 모드(반복 패스, 걸림)
- mechanism_specificity: 0 / 1 일반 기술어 / 2 부품 명명(포일·헤드) / 3 고유 메커니즘(SilkGlide, ProLift…)
- outcome_specificity: 0 / 1 일반 결과 / 2 감각·기능 결과 / 3 비교·정량 프레임(24%, 한 번에)
- same_unit_causal_completeness: 세 축이 한 단위 안에서 인과 연결어(덕분에, 로, so that…)로 묶이면 1
- **PMO_COMPLETE** = 세 축 ≥2 ∧ 완결 1

### 2.4 Campaign layer N1–N4 (NEVO만, 우선순위 N3 > N2 > N1 > N4)
N3 앰버서더/행사(공유·성수·언팩; '공유' 동음이의 규칙) · N2 브랜드 캠페인 메커닉(사전예약·증정) · N1 product/usage(써보·사용해·리뷰 또는 메커니즘/결과 주장) · N4 그 외. **주의:** N2가 N1보다 우선하므로 사용기 끝에 사은품 안내가 붙으면 N2로 간다 → N1이 과소(6/41)될 수 있음(공개된 한계).

## 3. 모델과 통계 — 무엇을, 왜

### A. Two-proportion comparison (비율 차이 + Cohen's h + 부트스트랩 CI)
- QUESTION: NEVO Tier A 메시지에서 코드 k가 카테고리 참조보다 더 자주 나타나는가?
- METHOD: 두 비율의 z-검정(raw p), Cohen's h(비율 차이의 표준화 효과크기; |h|≥.20을 실용적 후보 문턱으로 사전등록), source-cluster 부트스트랩 95% CI.
- WHY: 크기가 다른 두 메시지 공급 모집단(41 vs 68)의 비율 차이를 크기와 불확실성으로 같이 보기 위해. p만으로는 "얼마나"를 모른다.
- INPUT: `TIER_A_LABELS_v2.4_RECOMPUTED.csv` · OUTPUT: 코드별 x/n, h, CI, p · DECISION RULE: BH 통과 ∧ |h|≥.20 ∧ ladder → 후보 · LIMITATION: 41 vs 68에서 h=.20의 검정력은 약 .47.

### B. BH-FDR (Benjamini–Hochberg, q=.05)
- QUESTION: CH1~CH6 여섯 번 검정하면서 우연히 하나가 유의해지는 것을 어떻게 막았나?
- METHOD: 같은 family(CH 6개) 안에서 p를 정렬해 q=.05로 조정.
- 예: CH2 raw p=.045지만 BH 후 .090 → headline 아님. CH6 raw p=.009, BH 후 **.054** → 문턱을 넘지 못함(수리 전 21/40에서는 .039로 통과했으나 분모 1 증가로 실패).

### C. Equivalence / TOST
- QUESTION: "차이가 없다"고 말할 수 있는가?
- METHOD: 두 단측 검정(TOST), 등가 마진 h=±.20, 90% CI가 마진 안에 들어야 등가.
- WHY: p>.05는 등가가 아니다. 표본이 작으면 아무 결론도 못 낸다.
- 결과: CH3 h=−.05(거의 0)여도 90% CI [−.37, .29]가 마진보다 넓다 → L1 = NO_DECISION.

### D. Dedup / top-source robustness
- QUESTION: 한 캠페인 카피의 repost가 차이를 만든 것은 아닌가?
- METHOD: message-family(정규화 해시·URL·MinHash·임베딩) 단위 재계산; 최다 source 제거 재계산.
- 결과(CH6): family-level 17/35 vs 18/67 h=.45; top-source 제거 h=.46 — 방향 유지.

### E. Platform robustness
- QUESTION: 결과가 플랫폼 구성 때문인가? METHOD: 플랫폼별 방향 확인(모델 표준화는 cell 부족으로 불가).
- 결과(CH6): IG Post h=1.12(7/10 vs 3/17), IG Reels h=.31(12/21 vs 5/12) — 같은 방향이지만 **이질적**; pooled h=.51은 이를 숨긴다.

### F. Product × Actor model
- QUESTION: Brand 밖으로 갈 때 NEVO의 프리미엄 의미가 Series 9보다 더 사라지는가?
- MODEL: logit(label) = β0 + β1·NEVO + β2·External + **β3·NEVO×External** + platform + promotion + week + tier (source-cluster SE).
- 결과: Brand 저작 Tier A cell이 NEVO 0/41, S9 0/3 → **β3는 존재하지 않는다**. 모델 실패가 아니라 필요한 cell이 데이터에 없는 구조적 결과(NOT_COMPUTABLE). 어떤 계수도 인용하지 않는다.

### G. Campaign decontamination
- QUESTION: 프리미엄/라이프스타일이 제품 고유인가, 런칭 이벤트 증폭인가?
- METHOD: Amplification Ratio_k = P(PGk | N2∪N3) / P(PGk | N1), 부트스트랩 CI.
- 결과: N1=6, N2∪N3=32; PG1 1.22 [0.47, 3.00], PG3 0.94 [0.19, 1.69] → 모든 CI가 1을 포함, UNDERPOWERED.

### H. Robustness ladder (사전등록)
RAW → family dedup → top-source 제거 → platform 층화 → 비유료·비Brand. 5/5 같은 방향 = ROBUST, 3–4 = CONDITIONAL, ≤2 = NO-DECISION. 이 코퍼스에서 5번째 rung은 NEVO 비유료 1건이라 평가 불가 → 어떤 headline도 ROBUST에 도달할 수 없다(구조적).

## 4. 실행 완결성 (D-V24-001 WP 감사)
WP0 재조정·WP1 entity·WP3 CH·WP4 PMO·WP6 N·WP8 ladder = FULLY_EXECUTED(코드+입력+출력+커밋) · WP2 dedup = v2.3 family 재사용(재계산 아님) · WP5 gold 지표 = 사전 게이트로 미실행(D는 평정 불가) · WP7 = 모델 미적합(빈 cell). "C가 11/11 재현했다"는 산술·무결성·provenance 검증이지 실행 완결성 검증이 아니었음을 recovery에서 분리해 기록했다.

---
# 부록 D — 통계 결과
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

모든 수치는 수리 후(Tier A 182; cell NEVO 41 / S9 3 / REF 68) 값이며 D 계산을 C가 D 코드 없이 재계산해 일치시켰다. 각 결과 옆에 MEANS / DOES NOT MEAN을 둔다.

## 1. Category hygiene (NEVO vs 카테고리 참조; BH q=.05, family = 6 코드)
| 코드 | NEVO | REF | pp | h | raw p | p_BH | 판정 |
|---|---|---|---|---|---|---|---|
| CH1 Closeness | 21/41 (51.2%) | 27/68 (39.7%) | +11.5 | .23 | .241 | .289 | 비유의 |
| CH2 Skin Comfort | 25/41 (61.0%) | 28/68 (41.2%) | +19.8 | .40 | .045 | .090 | 비유의(BH) |
| CH3 Resolution | 2/41 (4.9%) | 4/68 (5.9%) | −1.0 | −.05 | .824 | .824 | NO_DECISION(TOST 실패) |
| CH4 Adaptive RTB | 3/41 (7.3%) | 0/68 (0%) | +7.3 | .55 | .024 | .071 | 비유의(BH); n<10 |
| CH5 Convenience | 13/41 (31.7%) | 31/68 (45.6%) | −13.9 | −.29 | .153 | .229 | 비유의 |
| **CH6 Functional/Material Premium** | **21/41 (51.2%)** | **18/68 (26.5%)** | +24.7 | **.51** | .009 | **.054** | **방향성, 비유의** |

- MEANS: 관측된 Tier A 메시지 공급에서 NEVO는 카테고리와 같은 benefit 어휘를 쓰며, 디자인·프리미엄·플래그십 어휘를 조금 더 쓴다.
- DOES NOT MEAN: 소비자 인식 · 시장점유율 · NEVO가 "소재/유니바디" 프리미엄을 더 말한다(21건 중 14건은 '디자인'·'프리미엄'·'플래그십'만으로 hit; 소재 특정 어휘만 세면 6–7/41 vs 3–6/68, ns) · Series 9과의 비교(S9 Tier A 3 → 금지).
- 민감도(사전등록 코드 아님): material-bearing subset D5 목록 7/40 vs 6/68 h=.26 p=.18; tight 목록 6/41 vs 3/68 h=.36 p=.06.
- Robustness(CH6): family-level h=.45 · top-source 제거 h=.46 · IG Post h=1.12 / IG Reels h=.31 · 비유료 rung 평가 불가 → CONDITIONAL(4/4 평가 가능 rung 동일 방향).

## 2. Problem → Mechanism → Outcome (L2)
| 집단 | n | 문제 구체성 | 메커니즘 | 결과 | 완결 | PMO_COMPLETE |
|---|---|---|---|---|---|---|
| NEVO | 41 | **0.45** | 1.58 | 1.83 | .05 | 2/41 (4.9%) |
| REF | 68 | **0.63** | 1.31 | 1.62 | .07 | 3/68 (4.4%) |
| S9 | 3 | (n<10, 정성만) | | | | 1/3 |
- NEVO vs REF: h=.03, p=.89 → UNDERPOWERED. **반례:** NEVO는 메커니즘(SilkGlide, 유니바디 = 3점)을 자주 명명하지만 그 메커니즘이 푸는 문제를 카테고리보다 덜 명명한다.
- MEANS: 현재 NEVO 소셜 언어는 "무엇으로"는 말하고 "무엇을 풀기 위해"는 덜 말한다. DOES NOT MEAN: 제품이 문제를 풀지 못한다(공식·에디토리얼 카피에는 문제 서술이 있음).

## 3. Premium grammar (L3; S9 비교 금지 → 카테고리 참조 대비 방향만)
| PG | NEVO (41) | REF (68) | h | p_BH |
|---|---|---|---|---|
| PG0 Functional only | 7 (17%) | 27 (40%) | −.50 | .064 |
| PG1 Experience | 15 (37%) | 12 (18%) | +.45 | .064 |
| PG2 Identity | 0 | 2 | — | — |
| PG3 Design Object | 6 (15%) | 3 (4%) | +.37 | .109 |
| PG4 Lifestyle Tech | 3 | 2 | +.21 | .331 |
| PGX Unsupported | 0 | 0 | — | — |
| PG_NONE(코드 없음) | 10 | 22 | 대비에서 제외(공개) | |
- 방향: NEVO는 경험·디자인 주도, 카테고리는 기능 주도. 어느 것도 BH를 넘지 못함. Gold 라벨 0 → κ 없음.

## 4. Campaign decontamination (L4)
NEVO Tier A 41 = N3 앰버서더/행사 31 · N1 product/usage 6 · N2 캠페인 메커닉 1 · N4 기타 3. Amplification PG1 1.22 [0.47, 3.00], PG3 0.94 [0.19, 1.69]. UNDERPOWERED — 산술은 되지만 증거가 아니다.

## 5. Product × Actor (L5)
Brand 저작 Tier A: NEVO 0/41, S9 0/3, REF 6/68. β3 정의 불가. NOT_COMPUTABLE. Brand 저작 NEVO 게시물은 7건(braun_korea 3, braun_us 3, braun_global 1) 존재하지만 전부 미리보기만 있다 → **actor 분류 오류가 아니라 evidence-tier artifact**(B·D 독립 감사 수렴).

## 6. 160 → 2(→3) 분해 (recovery gate R2, 정확 합산)
- 코퍼스: BRAUN_S9 entity child rows 160 = unique 157 + NEVO_AND_S9 3(이중 코딩). 157 = 155 미리보기만(Tier C) + 0 Tier B + 0 dedup 제외 + 0 provenance 실패 + 0 actor/promotion 제외 + 2 Tier A(수리 후 3).
- P03 176 = 22 entity 미검출(NONE 9, 브랜드만 12, 타사 1) + 151 미리보기만 + 3 Tier A.
- 판정 MIXED: 1차 원인은 **텍스트 수집 파이프라인**(전문 182건이 전부 M01 회원, 제품별 층화 없음), 2차는 구조(미리보기 절단). 분석 규칙(Tier A = verbatim)은 사전등록되었고 post-result 변경 0.

## 7. 가격 overlay (E; 제3 RQ 아님)
NEVO / Series 9 PRO+ 동일일자·동일 세제 street 배수: DE 1.70(street는 UVP 대비 −43%, €100 보상판매 동반) · KR 1.52(11000C) / 1.27(11010C) · JP 1.56 / 1.40 · **US NOT_COMPUTABLE**(featured offer 없음; MSRP $599.99 vs S9 street $379.99는 금지된 혼합 비교). 단일 글로벌 배수 없음. 소비자의 가격 수용 = NO-DECISION(VOC 없음). Brand 측 NEVO 글에는 가격이 없고(사전예약·사은품), 외부에서는 가격이 프레임이 된다(B Page 3).

## 8. 세 층 요약
- **살아남은 것:** closeness+comfort = 카테고리 공통(정성, USE); NEVO 메시지 공급 = 캠페인 공급(31/41 행사, 39/41 유료); 디자인·프리미엄 어휘 ↑(방향).
- **약해진 것:** "소재/유니바디 프리미엄이 유의하게 더 많다"(수리 후 비유의, 구성개념 느슨); "NEVO가 문제를 소유한다"(반대 방향).
- **답할 수 없는 것:** Brand 밖 생존, NEVO vs S9 정량, 등가, 소비자 반응, 가격 수용.

---
# 부록 E — 제품 컨셉과 포지셔닝
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 1. 관측 (현재 소셜 언어가 실제로 하는 말)
| 관측 | evidence anchor | 상태 |
|---|---|---|
| NEVO는 카테고리와 같은 benefit 어휘(밀착·편안·적응)를 쓴다 | CH1/CH2/CH3 NEVO ≈ REF; Hey M01/P03/P02; E CE-01 | USE(정성) |
| 그 위에 디자인·프리미엄·플래그십 어휘를 조금 더 얹는다 | CH6 21/41 vs 18/68 h=.51 p_BH .054; PG1 37% vs 18% | 방향성, 비유의 |
| 메커니즘(SilkGlide·유니바디·24%)은 자주, 구체적 문제는 덜 말한다 | PMO 문제 .45 vs .63; 완결 2/41 | 반례(L2) |
| 관측 가능한 NEVO 공급은 런칭 캠페인 공급이다 | N3 31/41; PAID 39/41; Brand 전문 0; 비유료 외부 1 | 구조적 사실 |
| 외부에서는 가격이 판단 프레임이 된다 | B Page 2/3: 30만원 훅, 최저가/핫딜, 유기적 반론 n=1 | 정성 |

## 2. 처방 (소구 전략) — "should own", never "already owns"
> **"더 세게 깎는 면도기가 아니라, 같은 부위를 덜 괴롭히는 플래그십."** (제품 약속: "피부를 덜 건드리고도, 원하는 만큼 깔끔하게." / EN 후보: "Closer without working harder on your skin.")

| 단계 | 내용 | evidence anchor | 처방 근거 vs 관측 |
|---|---|---|---|
| Specific Problem | 턱/목·누운 수염 때문에 반복 패스가 생기고 마찰이 누적된다 | E 공식(KR NEVO 페이지, 24% 마찰 주장의 구성); 01M0HQ7G21… 원문("여러 번 지나갔을 때"); GQ/Men's Health(fewer-pass comfort) | **처방**: 소셜에는 아직 희소(문제 구체성 .45) |
| Distinct Mechanism | SilkGlide 저마찰 포일 + 적응 커팅 | E 공식; 기술 alias NEVO_FOIL_TECH 48건; 01M1EQR7Z9… 외부 화자가 24% RTB를 반복 | 관측됨(메커니즘은 이미 말해짐) |
| Felt Experience | 덜 건드리면서 깔끔함 유지 | PG1 Experience 37%(방향); 01M0X8S8WP… "9보다 훨씬 더 스무스하고 잘 깍인다. 기변할만한 확실한 차이" | 부분 관측(유료 표본) |
| Premium Ownership | 316L 유니바디·촉감·케어 루틴 | PG3 15% vs 4%(방향); E 공식(unibody, 7년 lab); CE-01(공식 층위에서 NEVO 고유 격차는 2E) | 방향 관측 |
| Price Justification | 매일 반복되는 friction cost를 줄이는 플래그십 | E 가격 배수 1.27–1.70(시장별); 외부 가격 프레임(B P3) | 처방(소비자 수용 NO-DECISION) |

## 3. 버려야 할 소구 / 가져갈 소구
- 버림: "더 밀착됩니다" · "피부에 더 편안합니다" · "수염에 맞춰 스마트하게 적응합니다" · "가장 프리미엄한 면도기" — Series 9과 Philips가 이미 말한다(CE-01, CH1–CH4 ≈).
- 가져감: 구체적 실패(반복 패스·턱/목 마찰) → 저마찰 메커니즘 → 체감 경험 → 소유 경험. 캠페인은 celebrity·venue보다 **문제 데모(before → mechanism → after)**와 리뷰어 검증 질문("Series 9 사용자라면 어디서 차이를 느끼는가")으로 이동.

## 4. 결정 지도와 클래스
| Product meaning | External translation | Decision |
|---|---|---|
| Distinct | Retained | AMPLIFY |
| Distinct | Weak/lost | RE-EXPLAIN / TRANSLATION REDESIGN |
| Weak | Retained | PORTFOLIO REPOSITION |
| Weak | Weak | REPOSITION / TEST |
| **Insufficient** | **Any** | **NO-DECISION + targeted evidence ← 현재** |
X축: BH-유의 로컬 발견 0(방향만) + 공식 intent. Y축: 계산 불가(evidence gap). Quadrant를 강제하지 않는다.

## 5. Type I / Type II
- Type I(없는 차별화를 있다고): 공통 detector, Tier A만, family dedup, top-source 제거, BH로 통제. 잔여 위험 = gold 0(사람 검증 없음), CH6 구성개념 느슨.
- Type II(있는 차별화를 놓침): 41 vs 68에서 h=.20 검정력 ≈ .47; S9 3건; Brand cell 0 — 실제 차이/손실이 있어도 보이지 않을 수 있다. 그래서 "차이 없음"이라고도 말하지 않는다.

## 6. MEANS / DOES NOT MEAN (전략 문장에 병기)
- "디자인·프리미엄 어휘가 더 자주 보인다" MEANS 메시지 공급의 어휘 구성 / DOES NOT MEAN 소비자가 그렇게 인식한다.
- "NEVO는 문제를 소유해야 한다" MEANS 처방 / DOES NOT MEAN 현재 소유하고 있다.
- "Brand 밖 생존은 미확인" MEANS 텍스트가 수집되지 않았다 / DOES NOT MEAN 실패했다.

---
# 부록 F — 검증 로드맵
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 원칙
이번 Run의 병목은 분석이 아니라 **텍스트 취득 설계**였다(전문 182건, 전부 M01 회원, 제품별 층화 없음). 따라서 다음 단계의 우선순위는 모델을 바꾸는 것이 아니라 분모를 채우는 것이다. 모든 항목은 신규 취득을 요구하며(현재 Syncly CLOSED), 사전등록된 코드북·문턱은 그대로 둔다.

| # | 항목 | 왜(어느 NO_DECISION을 푸는가) | 최소 설계 | 성공 기준 |
|---|---|---|---|---|
| 1 | **제품별 층화 verbatim 텍스트 취득** | R2 근본 원인; S9 Tier A 3 → L3/L5; NEVO Tier A 41/225 | NEVO·Series 9 각각 entity-detected 게시물에서 전문 회수(read-only details), 유료/비유료·Brand/외부·플랫폼 층화; 목표 셀당 ≥20 | Series 9 Tier A ≥ 50, Brand 저작 NEVO ≥ 10, 비유료 NEVO ≥ 20 |
| 2 | NEVO 음차 lexicon (내비/내보 등) | entity 재현율; 01M1EQR7Z9…류 재분류 | ENTITY_DET v2.5에 한국어 음차 변형 추가, 회귀 테스트 확장; CJK 인접 Latin `\b` 규칙(prefix `\b` + suffix `(?![a-z0-9])`) | 회귀 PASS, FN 후보 0 |
| 3 | 사람 gold 라벨링 | gold 0 → 모든 CH/PG가 CONDITIONAL; CH6 구성개념 경계 | 기존 frame(182행, 35 strata)에서 층화 최소 100; Human 최종, A blind 2차; D 배제 | κ ≥ .75; CH6 loose/tight 경계 판정 |
| 4 | 비유료·비Brand NEVO 텍스트 | robustness rung 5; L4 product/usage 분모(6) | 1과 병행, ORGANIC/SUSPECTED 우선 | N1 ≥ 20 |
| 5 | Brand 저작 NEVO 전문 | L5 β3 유일 blocker | braun_korea/us/global 게시물 7건 + 추가 | Brand cell ≥ 10 |
| 6 | 리뷰어 검증 질문(외부 취득) | RQ2 독립 외부 증거(Hey N2a=0) | "Series 9 사용자라면 어디서 차이를 느끼는가 / 턱밑을 몇 번 지나가는가" 브리프 | independent external Tier A ≥ 20 |
| 7 | problem-ownership 코딩 확대 | L2 near-zero 재현 여부 | 1의 표본에 PMO 코딩 | PMO_COMPLETE 방향 재현 |
| 8 | US 동일일자 street price | 가격 overlay US 공백 | featured offer 존재 시 캡처 | 동일일자·동일 세제·동일 번들 |
| 9 | 소비자 VOC | reception NO-DECISION | 댓글/리뷰 취득 경로 확보 | attribute-level 평가 ≥ 50 |

## 게이트
1) 취득 전 사전등록 갱신(셀 크기·family·threshold 동일) 2) 취득 후 Gate V0 재조정(분모 확장은 새 epoch) 3) B/D 독립 lineage 재수렴 4) 그 뒤에만 L1–L5 재판정. GUARD-V24R-001은 S9 Tier A ≥ 20이 되기 전까지 유지된다.

---
# 부록 G — 하네스와 추적성
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 1. 역할과 경계
| Lane | 역할 | 할 수 있는 것 | 할 수 없는 것 |
|---|---|---|---|
| **A** Principal Analyst | 가설 사다리 수락, 발표 claim strength, 결정 클래스 | sealed evidence만 보고 판정; delta review | 새 분석·새 RQ·threshold 변경 |
| **B** Syncly Interaction → Frozen-data lineage | v2.3: Hey/MCP read-only 발굴(41콜, 48 evidence rows) · recovery: 행 단위 데이터 계보(P03/NEVO/REF), actor 감사, alias 감사, 원문 물질화 | 서버 측 의미 검색, raw 보존 | 쿼리 생성/수정, 결과 수를 prevalence로, 통계 해석 |
| **C** Assurance / Control plane | 사전등록 동결, 티켓 라우팅, provenance·게이트, 독립 재계산, B/D 수렴 판정, 단독 writer | 모든 canonical state | 남의 결과를 '좋게' 해석, 연구 방향 결정 |
| **D** Local Data Science | mart, entity, dedup, 코드북 적용, 통계, 반례 생산 · recovery: 측정 파이프라인 감사, 표적 재계산 | Tier A 기반 측정 | MCP, gold 평정, threshold 변경 |
| **E** Desk Evidence | 공식 카피·스펙·가격·캠페인·에디토리얼 독립 수집(36 units, 20 price rows) | OFFICIAL_INTENT 코딩 | Syncly, 소셜 결과 열람, 소비자 수용 주장 |

## 2. 왜 이 구조인가 — parallel independent analysis + adversarial validation + central arbitration
- **병렬 독립:** B와 D는 같은 176행(P03)의 계보를 서로의 결과를 보지 않고 재구성했다(B는 자체 detector 재구현, D는 사전등록 규칙). Stage별 rowset sha를 C가 대조했다.
- **적대적 검증:** D의 임무는 A의 스토리를 증명하는 것이 아니라 깨는 것이었다(L2 반례, CH6 구성개념 감사). B는 자기 Loop-1 actor 라벨이 틀렸음을 스스로 재실행으로 확인했고(28/40 mart 정답), 자기 모니터가 D 수치를 먼저 노출한 독립성 누출을 자진 신고했다.
- **중앙 조정:** C는 3행 divergence를 규칙(spec regex)으로 판정하고, PF-R5(HIGH) 주장을 13/13 분해로 반박했으며, 산술 재현(11/11)과 실행 완결성(WP 6F/2P/1S)을 분리해 기록했다.
- **Human:** 권위 문서 비준, 세션 시작, gold 최종 평정, 발표 문장 비준(CORR-V24-SLIDE2)만 맡는다.

## 3. 타임라인 (UTC, 2026-09-02)
11:04 v2.3 RUN_START → 11:22 B/D/E release → 11:28–12:25 B MCP Loop 1(41콜) · 11:45–12:19 D Loop 1 · 11:46 E → 12:25 Human v2.4 override(발표 우선, Syncly CLOSED) → 12:26–12:36 D-V24-001 → 12:41 C 검증·LOCAL PAGE SEAL → 12:56 A 해석 → 13:05 FINAL SEAL → ~13:15 Human recovery override(seal 보류) → 13:19 B/D recovery 티켓 → 13:22/13:34 CP1 → 13:31 R1(3행) → 13:40/13:55 CP2 → 13:52 D-V24R-002 표적 재계산 → 13:59 A delta → 14:02 RECOVERY SEALED.
운영 교훈: v2.3 Loop 1 동안 C는 watchdog 없이 턴을 종료해 B의 57분 실행을 감시하지 못했다. recovery에서는 Monitor(90초 폴링) + 7/12/15분 정책으로 교정했다.

## 4. 추적 체인 (예: Slide 1 두 번째 beat)
Business claim "디자인·프리미엄 어휘가 조금 더 자주" → Claim ID **C3 (local: DIRECTIONAL_NON_SIGNIFICANT)** → Statistical result 21/41 vs 18/68, h=.514, p_BH=.054 → Analytical table `claude-d v24_recovery/D_V24R_002_RECOMPUTE.json` → Codebook `claude-d v24/specs/CODEBOOK_CH_PMO_PG_N_v2.4.md` (CB_v2.4.0, commit 9d504e9) → Source rows `TIER_A_LABELS_v2.4_RECOMPUTED.csv` (post_id, CH6, grp) → Artifact sha `5bc7862b…` → Agent ticket `D-V24R-002_TARGETED_RECOMPUTE` (claude-d 1ca0481) → C verification (recompute in `control/v24_recovery/DECISION_LOG.md` 13:58Z) → Dataset `posts_cutoff.jsonl` sha `f8d130c2…1594`.
같은 체인이 모든 headline에 대해 `09_SOURCE_AND_CLAIM_LEDGER.md`에 있다.

## 5. 산출물 위치 (절대경로 기준 root `/home/sieg/projects-wsl/syncly_demo/.agent_worktrees/`)
- C: `C_assurance/control/v24/` (LOCAL_PAGE_SEAL, VERIFICATION_D/A, CLAIM/ROBUSTNESS ledgers, B_EVIDENCE_MARKUP, final/), `C_assurance/control/v24_recovery/` (RUN_STATE, CHECKPOINT/COVERAGE/DIVERGENCE/ROOT_CAUSE/REMEDIATION ledgers, L_DISPOSITIONS_REISSUED, RECOVERY_SEAL, final_report/)
- D: `D_research/v24/` (specs, results, gold, viz), `D_research/v24_recovery/` (lineage, audits, recompute)
- B: `B_production/runs/v2.3_20260902/B/` (Hey/MCP), `B_production/runs/v24_recovery/B/` (lineage, actor, alias, materialized)
- E: `E_desk/runs/v2.3_20260902/E/` · A: `A_authority/harness/handoff/` · BUS: `BUS_ledger/harness/ledger/LEDGER.md` (+ tickets/, recovery/, final/)

---
# 부록 H — 출처와 claim ledger
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

---
# 부록 I — 3-Slide Evidence Pack
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

모든 숫자는 분모를 붙인다 · Tier A(verbatim) 기준 · 메시지 공급이지 시장 반응이 아니다 · GUARD-V24R-001: NEVO-vs-Series 9 수치, Product×Actor, 감쇠 결론 금지 · 금지 문구 목록은 §5.

## Slide 1 — 이미 Series 9이 있다. NEVO는 왜 또 필요한가?
- Kicker(USE): **"그런데 이건 NEVO만의 언어가 아니었다."**
- Category table(Closeness / Comfort / Adaptive Tech = Category ● Series 9 ● Philips ● NEVO ●): 근거 = Hey M01/P03/P02 정성 판독 + E 공식 카피 코드북(S9 PRO+ "perfect closeness & skin protection, Pro SensoAdapt"; Philips i9000 "close shave, ultimate skin comfort"). 로컬 등가 수치는 없다(L1 NO_DECISION).
- Second beat(DIRECTIONAL): "NEVO의 Tier A 메시지에는 디자인·프리미엄·플래그십 어휘가 카테고리 참조보다 조금 더 자주 보인다 — 21/41 vs 18/68, h=.51, 다중검정 후 비유의(p_BH .054), 유료 런칭 창." **'소재/유니바디를 2배' 문구는 사용 금지.**
- Footnote(필수): "NEVO의 관측된 소셜 메시지는 메커니즘(SilkGlide·유니바디)을 말하지만, 그 메커니즘이 푸는 구체적 문제(반복 패스·턱/목 마찰)는 카테고리보다 덜 말한다(문제 구체성 .45 vs .63; 완결 chain 2/41)."
- Exemplar: 01M0HQ7G21… (#광고, 절삭력보다 접촉감, 316L 유니바디 — SUPPORT) · 01M1EQ8GVF… (Braun Thailand S9: 프리미엄+밀착+SmartCare — COUNTEREXAMPLE) · 01M0HQHV2X… ('디자인' 한 토큰으로 CH6 — AMBIGUOUS).
- Appendix: CH1–CH6 표(05 §1), 민감도(material-only), ladder, coverage(Tier A 41/225 NEVO · 68/366 REF · 3/157 S9).

## Slide 2 — 그 새로운 의미는 Brand 밖에서도 살아남는가?
- Headline: **A 대체안(CORR-V24-SLIDE2, Human 비준 대기)** "Brand가 만든 새 의미가 Brand 밖에서 독립적으로 확인된 사례는 아직 충분하지 않다." 초안 "…Lifestyle은 약해졌다"는 측정된 감쇠 주장이라 sealed evidence 밖.
- Two-layer visual(Brand/Campaign layer vs Product/Usage layer): 봉인된 구조적 사실 — NEVO Tier A 41 = 앰버서더/행사 31 · product/usage 6 · Brand 저작 0 · 비유료 외부 1(SUSPECTED). PG1 Experience 37% vs 18%(방향).
- Series 9 negative control: Hey-only 정성("Hey Syncly Series 9 판독에서는 기능 프리미엄은 외부에서 유지, symbolic/lifestyle은 약화"). 로컬 S9 수치 없음.
- Exemplars: 01M1EPRAPQ… (뉴시스 기사 리셰어 — 전체 architecture 유지, PR-shaped) · 01M1EQR7Z9… (제휴 YT Shorts, 자막+실제 발화 144자: 외부 화자가 NEVO의 24% RTB를 반복 — **단 detector는 BRAUN_S9로 코딩, 텍스트는 '내비/내보' 음차; 인용 시 매번 disclosure; C5를 격상시키지 않음**) · 01M1EPJKA1… (유기적 가격 반론+차별성 부정, n=1 정성).
- Footnote(verbatim): "Independent post-launch external evidence is limited; absence of evidence ≠ rejection."
- Appendix: WP6 cell·ratio CI(1.22 [0.47, 3.00]); WP7 cell table(0/41, 0/3 → NOT_COMPUTABLE); B Page 2 retention typology; 160→2(3) 분해(05 §6).

## Slide 3 — 그렇다면 NEVO는 무엇을 팔아야 하는가?
- Headline(처방): **"더 좋은 면도가 아니라, Series 9이 아직 소유하지 않은 사용 경험."** Chain: Specific Problem → Distinct Mechanism → Felt Experience → Premium Ownership → Price Justification — "recommended positioning architecture"로 표기, 현재 시장 상태 아님.
- Evidence for the direction: E 공식 intent(SilkGlide, 24% 마찰 감소[KR·JP]/glide[US·DE], −0.12mm, 316L 유니바디) + 방향성 로컬 신호(CH6·PG1·PG3, 전부 비유의) + GQ/Men's Health(refining not reinventing; fewer-pass comfort; S9 사용자에게 value tension).
- Evidence against "already owns": L2(메커니즘은 말하고 문제는 덜 말함).
- Price/value overlay(E): DE 1.70(street −43% vs UVP, €100 보상판매) · KR 1.52 / 1.27 · JP 1.56 / 1.40 · US NOT_COMPUTABLE(featured offer 없음). 단일 글로벌 배수 없음. Brand 측에는 가격이 없고(사전예약·사은품) 외부에서는 가격이 프레임. 소비자 가격 수용 = NO-DECISION.
- Appendix: E_PRICE_NORMALIZATION.csv(20행), E_CAMPAIGN_LANGUAGE_MATRIX.csv, CE-01~CE-12.

## Decision class
**NO-DECISION + targeted evidence** — 발표는 "초기 가설이 데이터에 깨지고 존재 이유를 다시 정의한 과정"으로 운반한다(02 §TL;DR).

## 5. Deck에서 금지
소비자 반응 좋다/나쁘다 · US vs KR 반응 · English=US · 아카이브 건수=시장점유율 · 유료/행사 긍정=만족 · clean external 부재=기각 · P02 일반화 · 8/31 partial-week 감소 · **로컬 NEVO vs Series 9 수치** · **Brand→External 감쇠 수치** · "통계적으로 동일" · S1 "이미 소유" · 단일 글로벌 가격 배수 · "소재/유니바디 프리미엄 2배" · bare "24%".
