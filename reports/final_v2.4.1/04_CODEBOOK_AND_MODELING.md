# 04 · 게시물의 말을 어떤 분석 변수로 바꿨고, 어떤 모델을 왜 썼나
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
