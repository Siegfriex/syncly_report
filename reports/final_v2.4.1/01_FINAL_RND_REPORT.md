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
