# 요청 ① 판단 — 실광고 표현 자산 4종 인계 vs BRAND 단독 축소 실행

작성 Claude C · 2026-09-03 09:5x KST · 대상 Human(의사결정) · 성격: 어드바이스. C는 Desk 문서를 열지 않았고, 이 문서에는 소비자 해석이 없다.

## 0. 한 줄 판단

**자산 인계(단계적)를 권고한다.** 근거는 하나다: 요청 측이 구조적으로 얻을 수 없다고 한 CREATOR 광고 표현이 Syncly 동결 코퍼스 안에서는 NEVO 광고 표현의 **최대 actor 층**(전문 24건 / 미리보기 79건)이기 때문이다. BRAND 단독 축소는 §14의 질문을 포기하는 선택인데, 포기할 이유가 없다. 다만 RETAIL은 인계해도 채워지지 않는다. 이것은 인계 여부와 무관한 코퍼스의 사실이고, 축소 실행을 하더라도 같은 결손이 남는다.

## 1. C가 실제로 넘길 수 있는 것 (측정된 보유량, NEVO 기준)

| actor(요청 측 enum) | 전문(Tier A) 게시물 | 미리보기(Tier C, 203자) 게시물 | 광고 주장(AS) 적중 건수 Tier A / C | 인계 가능 |
|---|---|---|---|---|
| BRAND | 7 (전부 PAID) | 0 | 7 / 0 | ✔ 소량 — 요청 측 88건 공식 copy를 대체하지 않고 "소셜 게시 형태의 브랜드 copy"로 보강 |
| CREATOR | **24** (PAID 17 · SUSPECTED 5 · ORGANIC 2) | **79** (PAID) | 43 / 38 | **✔ 핵심 자산** |
| MEDIA | 3 (PAID) | 10 | 18 / 5 | ✔ 얇음 — 이벤트/런칭 copy 포함 |
| RETAIL (Retail+Commerce) | **0** | 7 (Commerce, PAID) | 0 / 10 | ✗ 전문 없음. 미리보기 절 7건만, 잘린 문장 |
| OTHER_EXTERNAL (핸들 미해결) | 29 (PAID 22 · SUSPECTED 7) | 70 | 129 / 39 | ✔ 인계하되 actor 미확정 꼬리표 |
| 언어 | KO 50 · EN 13 (Tier A) | KO 113 · EN 46 · 기타 8 | | JA·DE 광고 표현 없음 |

주장별 Tier A 적중(NEVO): AS-01 저마찰 70(Creator 12·Media 13·Other 43·Brand 2) · AS-02 24% 23 · AS-03 소재 15 · AS-09 프리미엄 가격 17 · AS-07 센서 23 · AS-06 케어 9 · AS-04 독일 2 · AS-05 보증 1 · **AS-08 교체주기 0**.

읽는 법: CL-01/02/03/07/09는 actor별 앵커가 성립한다. CL-04/05/06/08은 광고 표현 자체가 희소하거나 없으므로, 어느 쪽 실행이든 "앵커 결손"이 아니라 "광고 공급 자체가 낮거나 측정 공백(NOT_MEASURED)"으로 적어야 한다. 특히 AS-06/AS-08은 C 사전의 공백이 기록되어 있어(coverage caveat) 0이 "없음"을 뜻하지 않는다.

## 2. 인계가 요청 측 문제를 실제로 푸는가

| 요청 측 결손 | 인계 후 상태 |
|---|---|
| CREATOR_AD_ANCHOR 0 | **해소** — 24 전문 + 79 미리보기, 유료/의심/자연 구분 보존 |
| RETAIL_AD_ANCHOR 0 | **미해소(구조적)** — NEVO 소매 전문 0. 보고서에 "RETAIL 앵커 결손 = 코퍼스 사실"로 기재. Commerce 미리보기 7절은 참고 등급 |
| MEDIA/EVENT | 부분 해소 — 3 전문 + 10 미리보기 |
| CONSUMER_SUPPORT/REJECT 앵커 | C 범위 밖(요청 측 원칙대로 공개 웹 독립 수집). C는 넘기지 않는다 |
| HARD_NEGATIVE 8 | 보강 가능 — 코퍼스 실측 오탐 사례("72% OFF", "2-in-1 키트", "-0.12mm 눌러 밀착", 미용실 "Prestige", Vertu "prestige")를 실제 표현으로 제공 |
| §14 actor 비교 | **BRAND vs CREATOR vs OTHER_EXTERNAL(±MEDIA)로 수행 가능**; RETAIL 축은 NOT_MEASURED |
| sim_to_brand_copy AMBER | BRAND 단독 centroid 문제는 CREATOR/MEDIA family medoid 추가로 해소 가능. 등급 판단은 요청 측 몫 |

## 3. 인계하지 말아야 할 것 / 인계물의 한계

- **소비자 해석 없음.** 인계물은 광고 표현 원문·출처·actor·홍보유형·플랫폼·언어·tier뿐이다. C의 정렬 판정(X02)·매트릭스 해석은 포함하지 않는다.
- **원문 그대로.** raw_expression은 코딩 기질(캡션+자막, 헤더 제거)의 문자 그대로의 절이며 요약·번역·정규화본은 별도 열(normalized_expression)에만 둔다. 반증 원장에서 이미 33건을 원문 정확 재절단한 절차를 그대로 쓴다.
- **시장(market) 열은 UNRESOLVED.** 게시물 단위 시장이 없다. 언어로 시장을 추정하지 않는다(English≠US, Korean≠Korea). 요청 측이 시장별 앵커를 요구하면 그 축은 언어 축으로만 제공된다고 명시해야 한다.
- **미리보기(Tier C)는 잘린 문장이다.** 203자에서 끊긴 절은 expression 단위로 부적합할 수 있어 evidence_tier=C와 truncated 플래그를 달고 넘긴다. 앵커(medoid)는 Tier A에서만 뽑는다.
- **OTHER_EXTERNAL 29건은 핸들만으로 actor를 못 정한 계정**이다. 크리에이터일 수도 브랜드 연계 계정일 수도 있다. 요청 측이 이를 CREATOR로 흡수하면 안 된다.
- **PAID 1,616건은 보완 규칙으로 파생**된 라벨이다(paid_derived 플래그). 유료/자연 구분을 앵커 선정에 쓸 때 파생 여부를 함께 봐야 한다.
- **JA·DE 광고 표현이 없다.** 요청 측 4개 시장 중 KR/US에만 소셜 광고 표현이 대응한다.

## 4. 시점과 순서

Human 지시(§3)에 따라 표현 bank는 **현재 run 봉인 후** extension(RUN-V25-ADVERTISING-REALITY-HANDOFF-001)에서만 만든다. 현재 봉인 차단 요인은 정규식 오탐·미탐 전수 감사 1건이며 진행 중이다. 봉인 직후 bank 1차분(Tier A 절 단위 분해 + actor/holbo 보존 + 출처 sha)은 서브에이전트 병렬로 수 시간 내 산출 가능하고, family 그룹화와 medoid는 수동 감사가 붙어 그보다 오래 걸린다. 따라서:

- **권고 실행안: 단계적 인계.** 1단계 = AD_EXPRESSION_BANK(Tier A 우선, Tier C 플래그 포함) + DESK_INTERFACE_SCHEMA → 요청 측이 §22 대조 후 즉시 CREATOR/MEDIA/OTHER 앵커 구성 가능. 2단계 = AD_EXPRESSION_FAMILIES + AD_ANCHOR_REGISTRY(medoid_flag, validated).
- 요청 측이 1단계도 기다릴 수 없다면 그 사이에만 BRAND 단독을 **임시(INTERIM)** 로 돌리고, 인계 후 재실행하도록 한다. 축소 실행을 최종으로 확정하는 것은 권하지 않는다.

## 5. 인터페이스 계약(요청 측 §22 대조 항목에 맞춤)

| 항목 | C 제공 방식 |
|---|---|
| SHA | 파일 sha256 + 행별 post_sha(코딩 기질 sha256) + source_ref(MCP dump / baseline / crawl 파일 sha) |
| 행수 | 파일별 행수 + actor×promotion×tier 교차 집계표 동봉 |
| claim ID | CLAIM_ID_CROSSWALK.csv: CL-01…09(Human §6 명칭) ↔ AS-01…09 ↔ Desk CL. CL-03(소재)과 CL-04(독일)는 절대 병합 안 함 |
| actor | ACTOR_v2.3.0 → 요청 enum 매핑표 동봉: Brand→BRAND, Creator→CREATOR, Retail·Commerce→RETAIL, Media→MEDIA, Reviewer→MEDIA(flag REVIEWER), Other→OTHER_EXTERNAL; EVENT는 creative_type=CT-EVENT로 표기 |
| product / model | ENTITY_DET_v2.5.0 결과(NEVO / BRAUN_S9 / PHILIPS_S9000 / LAIFEN), 이중 entity 플래그 |
| market | UNRESOLVED(언어만 제공) — 명시 |
| language | 스크립트 비중 ≥30% + 불용어 휴리스틱(C 참조 구현) |
| source provenance | post_id, platform, url(코퍼스 보유 시), fetched_at, evidence_tier, preview_corrected 플래그 |
| 스키마 | DESK_INTERFACE_SCHEMA.csv(열 이름·타입·enum·필수 여부·검증 규칙) |

불일치 시 반송 규칙은 그대로 수용한다. C 쪽에서도 인계 전 동일 항목을 자체 대조해 대조표를 첨부한다.

## 6. 결론

| 선택지 | 판단 |
|---|---|
| 자산 인계(단계적) | **채택 권고.** CREATOR·MEDIA·OTHER_EXTERNAL 앵커가 생겨 §14 비교가 성립. RETAIL은 어느 쪽이든 결손이며 "코퍼스 사실"로 기재 |
| BRAND 단독 축소(최종) | 비권고. 얻을 수 있는 최대 actor 층을 버리는 선택 |
| BRAND 단독(임시) | 인계 대기 중에만 허용, 재실행 전제 |

Human이 결정할 것: (1) 인계 승인 여부, (2) 1단계 인계에 Tier C 미리보기 절을 포함할지(권고: 포함하되 플래그), (3) OTHER_EXTERNAL 29건의 취급(권고: 별도 actor로 유지).
