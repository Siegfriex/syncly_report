# 03 · 어떤 데이터를 왜 썼고, 원본 게시물은 어떻게 분석 가능한 데이터가 되었나
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
