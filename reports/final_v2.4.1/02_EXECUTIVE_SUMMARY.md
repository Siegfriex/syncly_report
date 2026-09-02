# 02 · Executive Summary — Series 9이 있는데 NEVO는 왜 필요한가?
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
