# NEVO × Syncly 데이터 효용 종합 브리핑 v2 — 규모·품질·정의·판정기준

작성 Claude C(assurance / control plane) · 2026-09-03 09:55 KST · 대상 Human · 상태 CURRENT_AD_SIGNAL_RUN_SEALED(측정 봉인) / extension RUN-V25-ADVERTISING-REALITY-HANDOFF-001 진행 중 · Desk 문서 미열람, 소비자 해석 없음.

한 줄 요약: 3,435건 동결 소셜 코퍼스 위에 광고 신호 측정 체계가 검증된 상태로 봉인되었다. 전문 텍스트가 268건(NEVO 63)뿐이어서 판정 상한은 DIRECTIONAL이고 응답층은 정성 수준이다. 방법은 재현 가능하고 원장에 남아 있으며, 데이터는 얇다.

---

## 0. 용어 정의 (처음 나올 때 한 번만)

| 용어 | 정의 |
|---|---|
| 동결 코퍼스(frozen corpus) | 2026-08-31 cutoff로 확정된 3,435개 소셜 게시물. sha256 f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594. 어떤 결과도 이 분모 밖에서 만들지 않는다. |
| 게시물(post) / 단위 | 분석 단위는 canonical post_id 1건. 모든 코드는 게시물 단위 이진 다중 라벨. |
| Tier A | 캡션 원문(+자막 transcript)을 로컬에 verbatim 보유한 게시물. 268건. |
| Tier C | 203자 미리보기(말줄임 "…"로 끝남)만 있는 게시물. 3,167건. |
| 코딩 기질(substrate) | 실제로 정규식을 돌리는 텍스트 = 캡션 + 자막. 메타데이터 헤더(Post ID, URL, Sentiment 등)는 제거. 오염 13행은 true_preview로 대체(R-8). |
| PREVIEW_SAFE / FULL_TEXT_ONLY / EITHER | 코드별 tier 규칙. 토큰이 통상 203자 안에 나타나면 PREVIEW_SAFE, 밖에 나타나면 FULL_TEXT_ONLY. FULL_TEXT_ONLY 코드는 Tier C에서 NOT_EVALUABLE(절대 0 아님). |
| NOT_EVALUABLE(NE) | 평가 불가. 분모(E)에서 제외. 0과 구분. |
| LANG_UNCOVERED | 해당 (코드, 언어)에 사전이 없음 → NE. 사전 보유 언어: KO EN DE JA FR PT ES IT VI. |
| 광고 신호(advertising signal) | 브랜드·유료 크리에이터·소매·미디어 생태계가 실제로 밀어낸 메시지. 소비자 수용과 무관. |
| 응답(response) | 플랫폼 관측 지표(views/likes/comments/shares). 소비자 수용·선호·설득이 아니다. |
| E(eligible denominator) | 슬라이스 안에서 해당 코드를 평가할 수 있는 게시물 수(NE 제외). 1차 E = NEVO Tier A 63. |
| SUPPLY_SHARE | 신호 게시물 k / E. |
| PAID_CONCENTRATION | P(PAID \| 신호). |
| ORGANIC_PENETRATION | P(신호 \| ORGANIC). |
| BRAND_TO_EXTERNAL_TRANSLATION | 브랜드(Braun 소유 계정) 신호 share − 외부 actor 신호 share (pp, Cohen h). |
| PERSISTENCE | 주차별 신호 존재(ISO W31–W35). |
| Cohen h | 두 비율의 아크사인 변환 차이. 실무 효과 문턱 \|h\| ≥ .20, 반드시 pp와 병기. |
| BH-FDR q=.05 | Benjamini–Hochberg 거짓발견율 통제. 사전 선언된 가족 안에서만. |
| TOST | 등가 검정. "같다" 주장은 h ±.20 구간에 90% CI가 들어올 때만. 이번 데이터에서는 도달 불가. |
| 강건성 사다리(ladder) | 같은 결과를 raw / 메시지군 dedup / 최상위 출처 제외 / 플랫폼 층화 / 유료·무료 / 브랜드·외부 6단에서 재확인. |
| ECHO | 크리에이터·소매 등이 브랜드 copy를 그대로 반복한 표현. 소비자 언어가 아니다. |

---

## 1. 큰 숫자

| 항목 | 값 | 의미 |
|---|---|---|
| 동결 코퍼스 | 3,435 | 모든 1차 결과의 분모. 불변. git-clean 확인 |
| 전문(Tier A) | 268 = 기존 182 + EM1 신규 86 | 코드 대부분은 여기서만 평가 |
| NEVO Tier A | 63 (entity 231 중) | 광고 신호 주 분모 E |
| Series 9 / Philips / Laifen Tier A | 43 / 29 / 5 | 비교군. 언어 커버 후 평가 가능 팔 S9 29–33, Philips 21–24 |
| 미리보기만 | 3,167 (92.2%) | FULL_TEXT_ONLY 코드 평가 불가 |
| 언어 미커버 | 442 → 코드별 NE | AR/TH/BN/ZH/RU + 미판정 92 |
| creative type 결측 | 3,150 / 3,435 | 메타데이터 부재, 추정 금지 |
| 정규식 사전 | 1,935 패턴, 9개 언어 | 코드북 v1(v1.1 = 통화 regex 수리 3건, 토큰 증감 없음) |
| claim mart 적중 | 11,008 (post×code×offset, dedup) | 광고 표현 bank의 원재료 |
| D00 보충 68건 | OFF_PRIMARY_DENOMINATOR | 파서 손실분 재파싱; sensitivity 전용 |

---

## 2. 데이터 규모와 구성

### 2.1 플랫폼·기간·홍보·행위자
- 플랫폼: Instagram Reels 880 · YouTube Shorts 853 · Instagram Post 643 · Facebook 560 · TikTok 318 · X 181.
- 기간: ISO 2026-W31~W35(5주). 출시 burst 구간만 관측. W5+ 관측 불가.
- 홍보: PAID 2,554(1,616은 보완 규칙 파생, paid_derived 플래그) · ORGANIC 670 · SUSPECTED 211. SUSPECTED는 어느 쪽에도 합치지 않는다.
- 행위자(ACTOR_v2.3.0, 핸들 토큰 규칙): Brand 51 · Retail 76 · Commerce 122 · Media 56 · Reviewer 71 · Creator 780 · Other 2,279(핸들 미해결 66%). Other ≠ 소비자.
- NEVO Tier A 63의 행위자: Brand 7(전부 PAID) · Creator 24(PAID 17 · SUSPECTED 5 · ORGANIC 2) · Media 3 · Other 29(PAID 22 · SUSPECTED 7) · Retail/Commerce 0.

### 2.2 언어
- 텍스트 언어: en 2,335 · ko 765 · und 92 · vi 62 · es 29 · pt 25 · de 24 · id 16 · fr 14 · ar 14 · tr 14 · th 10 · zh 9 · ja 8.
- NEVO Tier A: ko 50 · en 13. JA·DE 광고 표현은 없다. 언어로 시장을 추정하지 않는다(English≠US, Korean≠Korea). 게시물 단위 market은 전부 UNRESOLVED.

### 2.3 참여 지표 가용성
| 지표 | 가용 플랫폼 | 비고 |
|---|---|---|
| views / er / subscribe_count | Reels·Shorts·TikTok·X | Instagram Post·Facebook은 100% 0 = 결측 처리 |
| likes | 전 플랫폼(>0 75.6%) | |
| comments | 전 플랫폼(>0 45.7%) | |
| shares | X·TikTok만 | |
| collect_count | TikTok만 | |
| saves | 없음 | 열은 두되 비움 |
| 팔로워 분모 | 없음 | 정규화 불가 |
규칙: 플랫폼 내 커버리지 ≥50%인 지표만 사용, 플랫폼 내부 백분위로만 비교, 유료/무료 노출 동등 가정 금지.

### 2.4 시간 축
출시 기준 주차(week_from_launch)는 데이터에 없다. 1차 축 = ISO 주차. 민감도 clock 2개: wfl_KR(기준 2026-08-24 → W−4…W0), wfl_JP(기준 2026-07-31 → W0…W4). W5~W8 = NOT_OBSERVED_BY_DESIGN.

---

## 3. 데이터 품질

### 3.1 수집층 근본 원인(3층 분리, 원장 RC-Q/RC-F/RC-P)
| 층 | 내용 | 결과 |
|---|---|---|
| RC-Q 쿼리 설계 | 최대 쿼리 A01(코퍼스 53%)이 제품 seed를 배제한 라이프스타일 쿼리 | 비-Braun 비교군은 co-mention으로만 존재 |
| RC-F fetch 예산 | Cycle 1 상세 조회 27/835건이 파일 순서상 전부 NEVO; Series 9는 P03 쿼리에 92% | 텍스트 확보 격차(NEVO:S9 수집 1.05:1 → 텍스트 20:1). EM1 89콜로 해소(S9 External×PAID 3→29, Philips 4→26) |
| RC-P 파서 regex | 단일 파일(D00 page_0002) 결함 | 오염 13행·손실 68건·집계 23 동시 발생. 38페이지 전수 감사에서 결함 파일 1개뿐 |

### 3.2 검증 결과(C 독립 재현)
| 항목 | 결과 |
|---|---|
| EM1 MCP 89콜 | pool 89/89, raw sha 전수 일치, 실패 0. 크롤 교차검증 62 EXACT + 2 PREFIX / 64 |
| entity 재탐지(ENTITY_DET_v2.5.0) | 86 admit / 3 제외(오염 1, bare "prestige" 오탐 2) |
| 광고 신호 post mart | C 독립 코더 vs D: 13 claim 코드·10 역할 코드 3,435/3,435 동일; 언어·tier 3,435/3,435 |
| 매트릭스 6종(H1/H3/H4/H5/H6/H8) | 398/398 셀 (k, E) 동일. 셀→post_id 인덱스 641/641(QA11) |
| 비교군 검정 | K2(vs Philips) 11/11 동일. K1(vs S9) 이중 entity 2건 양팔 제외(61) 후 10/11 + AS-08 BH 경계(D q=.022 / C q=.057, 추정치 동일) |
| 블라인드 라벨 감사(광고 신호, 40) | D 양성 전부 실제 사전 사례; tier 규칙 위반 0; 언어 커버 규칙 오류 1건 → 수정 |
| 정규식 전수 감사(590 토큰 = 부하 코드 적중 100%) | 정밀도 AS-01 .97 / AS-02 1.00 / AS-03 .80 / AS-04 1.00 / AS-06 .97 / AS-07 .81 / AS-08 .68 / AS-09 .79 / AS-W1 .80 / AS-W4 .97 |
| 반증 원장 | 61행, 인용 33건 원문 정확 재절단, NONE_FOUND 24 재현, 강등 13 |
| v2.5 비교군 콘텐츠 코드북(CB_v2.4.0/2.5.1) 라벨 | 3회 블라인드 감사 FAIL → 루프 한도(2) 소진 → NO-DECISION 종결. 코드북은 유지, 코더 결함 이월 |

### 3.3 남은 결함·한계(모두 공시)
- 사전 공백: AS-06(케어), AS-W2(보증 후 증명), AS-W3(유지 부담), MR-PROMOTION, MR-CONVENIENCE. 이 코드의 낮음/없음은 NOT_MEASURED 또는 LOW_OBSERVED_WITH_COVERAGE_CAVEAT로만 쓴다.
- 비교군 사전 비대칭: 사전이 NEVO 공식 어휘를 담고 비교군 등가 표현(Philips SkinGlide/clean pod/"50% 더 부드럽게", S9 SensoAdapt)을 빠뜨림 → K2 AS-01, K1/K2 AS-06, K1 AS-07/08은 INSUFFICIENT로 강등.
- 응답층 49행 중 46행 n<10. NEVO ORGANIC 전문 2건 → 유료/무료 응답 비교 불가.
- Brand 셀 7/7/0 → 제품×행위자 상호작용 추정 불가, 사다리 5·6단 평가 불가 → ROBUST 도달 불가(상한 CONDITIONAL).
- 등가(TOST) 불가(팔당 135 필요).
- 구현 독립성: D가 C 참조 코더를 그대로 채택. "독립 파이프라인" 표현 금지. 블라인드 감사 2회 + C 독립 수치 재계산으로 대체(METH-01).
- prereg 사후 추가 2건(§N-2 판정→Q4 매핑, lexicon v1.1 regex 수리). 결과표 이전, 판정 이전. sha 이력 기록(METH-02).
- Human 지시 §19 문서 목록이 잘렸고 §20–21 누락.

---

## 4. 분류 코드북 — 정의와 판정 기준

### 4.1 공통 규칙
- 토큰 출처는 동결 사전(AD_SIGNAL_LEXICON_v1.json, 1,935 패턴)만. 사전 밖 토큰은 구현 결함.
- 매칭 표면: NFKC + casefold + '#'→공백(fold). 라틴은 \b 접두 + (?![a-z0-9]) 접미. 한국어·일본어는 띄어쓰기 무시(nospace) 매칭 후 오프셋 역매핑.
- 언어 선언: 스크립트 비중 ≥30%로 비라틴 판정, 라틴은 불용어 휴리스틱, 증거 없으면 en. 'und'는 언어가 아니다.
- 파생 union(RTB/BENEFIT/CONVENIENCE/QUALITY_CUE/OWNERSHIP)은 Tier C에서 PREVIEW_SAFE/EITHER 구성요소만 사용(판정 3b).
- 제외는 인접(adjacency) 수준. 단위 수준 제외 금지.

### 4.2 주장 축 AS-01~09 (Desk CL-01~09 대응)
| 코드 | 명칭(Human §6) | 정의 | 포함 | 제외(hard negative 실사례) | tier |
|---|---|---|---|---|---|
| AS-01 | LOW_FRICTION_FOIL | 마찰 기제를 통한 밀착+편안함 | 초저마찰 포일, SilkGlide 기제, 마찰 감소로 인한 밀착 | 일반적 "밀착"만, "-0.12mm 눌러 밀착"(공식 copy 압력 문구), "#실크쉐이빙" 캠페인 해시태그 단독 | EITHER |
| AS-02 | 24PCT_FRICTION_GLIDE_RTB | 글라이드/마찰 수치(24%, >20%) | 마찰·글라이드 ±60자 내 % 수치 | 할인 %(72% OFF), 배터리 % | PREVIEW_SAFE |
| AS-03 | STAINLESS_UNIBODY_MATERIAL_OWNERSHIP | 316L/스테인리스/메탈 유니바디/소재·장인 | 스테인리스, 유니바디, 316L, Edelstahl, ステンレス, 削り出し | Made in Germany(AS-04와 절대 병합 금지), 일반 "고급" | FULL_TEXT_ONLY |
| AS-04 | MADE_IN_GERMANY | 독일 제조·엔지니어링 | Made in Germany, 독일산, deutsche Ingenieurskunst | 소재 어휘 | EITHER |
| AS-05 | WARRANTY_REASSURANCE | 보증 기간·장기 안심 | 5년 보증, N년 무상 A/S, Garantie | 리퍼 판매자 1년 보증(CL-05 아님) | FULL_TEXT_ONLY |
| AS-06 | CARE_SYSTEM_CONVENIENCE | SmartCare/클린스테이션/5–7in1 | 세척기, 클린&차지, SmartCare | 2-in-1/3-in-1 키트, 동사 clean | FULL_TEXT_ONLY |
| AS-07 | DENSITY_SENSOR_ADAPTATION | 밀도 감지·적응 출력(340회/초) | 센서, 자동 인식(수염), NEVO Sense | flex head "adapt to"(6건), 세척 프로그램 "자동으로 인식"(5건) | FULL_TEXT_ONLY |
| AS-08 | REPLACEMENT_CYCLE | 18개월 교체 주기·교체 권장 | 18개월, replacement head 권장 문맥 | 소매 SKU 나열 | FULL_TEXT_ONLY |
| AS-09 | PREMIUM_PRICE_JUSTIFICATION | 프리미엄/플래그십 가격 정당화 | 프리미엄, 플래그십, worth it | 일반 형용사 premium(문맥 없음), 타사 제품(LG) | EITHER |
AS-08 파생 프레임: F_CONV(AS-08 ∧ MR-CONVENIENCE), F_MAINT(AS-08 ∧ (AS-W3 ∨ MR-OWNERSHIP)), F_NEUTRAL, F_ABSENT.

### 4.3 공백 축 AS-W1~W4 (GAP-01~04)
| 코드 | 정의 | 근거 상태 |
|---|---|---|
| AS-W1 LONG_TERM_RELIABILITY | 오래 씀·튼튼·내구·고장 없음 | 코퍼스 근거 있음, 정밀도 .80 |
| AS-W2 POST_WARRANTY_PROOF | 보증 후 증명(사용 연수·고장률·내구 테스트·수리 가능성) | 코퍼스 2건, THIN → NOT_MEASURED |
| AS-W3 LOW_MAINTENANCE_BURDEN | 유지 부담·소모품 비용 | KO 토큰 미실측 → KO NOT_MEASURED |
| AS-W4 SPECIFIC_SHAVING_FAILURE | 반복 패스·목/턱·당김·상처·압력 | 좁은 facet(a)(c)(e) NEVO 4 / S9 5 / Philips 0 = QUALITATIVE; 넓은 facet(d) "자극 없이"는 편안함 copy → 분리 보고 |

### 4.4 메시지 역할 MR(다중, 강제 단일화 없음)
MR-HOOK(첫 80자 fold 창, 토큰 전체 포함) · MR-BENEFIT · MR-RTB · MR-PRICE_JUSTIFIER · MR-OWNERSHIP · MR-CONVENIENCE · MR-QUALITY_CUE · MR-PROMOTION(할인·사은품·예약·보상판매·번들·쿠폰·통화가격) · MR-SOCIAL_PROOF(앰배서더·리뷰어·수상·후기; KO '공유' 동음이의 제외) · MR-CATEGORY_HYGIENE(일반 밀착·편안·성능).

### 4.5 크리에이티브 유형 CT
CT-PRODUCT_DEMO / FEATURE_EXPLAINER / LIFESTYLE / AMBASSADOR(endorser 토큰 필수) / EVENT / REVIEW_TESTIMONIAL / COMPARISON / RETAIL_PROMO / STATIC_PRODUCT / UGC_STYLE / OTHER(카테고리 밖 게시물) / MISSING. 근거는 VIDEO_ANALYZER FORMAT_ARCHETYPES(60건) 또는 명시 텍스트 단서만. 미디어 형식(Reels/Shorts) ≠ 크리에이티브 유형. 부재로 추정 금지. 결과: MISSING 3,150.

### 4.6 행위자·홍보 매핑(Desk 인계용)
Brand→BRAND · Creator→CREATOR · Retail/Commerce→RETAIL · Media→MEDIA · Reviewer→MEDIA(플래그) · Other→OTHER_EXTERNAL · EVENT는 CT-EVENT. 홍보 PAID/ORGANIC/SUSPECTED + paid_derived. actor로 소비자 수용을 추정하지 않는다.

---

## 5. 측정·통계·판정 기준 (결과 보기 전 동결)

### 5.1 공급 등급
MATERIAL ⇔ share ≥ 20% ∧ Wilson 95% 하한 ≥ 10% ∧ k ≥ 5 · LOW ⇔ Wilson 상한 < 20% · 그 외 INDETERMINATE. E<10 QUALITATIVE_ONLY · E 10–19 등급 보류 · 20–49 DIRECTIONAL · 50+ QUANTITATIVE.

### 5.2 통계
α=.05 양측. BH q=.05는 동결 가족 2개(F-AD-K1 NEVO 61 vs S9, F-AD-K2 NEVO 63 vs Philips; 각 11검정 AS-01~09, W1, W2)에만. 출처 블록 순열검정 10,000회, 출처 블록 부트스트랩. 효과 Cohen h ≥ .20 + pp. 판정 상한 DIRECTIONAL. TOST 불가 선언. 히트맵 셀마다 검정하지 않는다.

### 5.3 강건성 사다리
6단(raw / 메시지군 dedup / 최상위 출처 제외 / 플랫폼 층화 / 유료·무료[팔<10이면 NE] / 브랜드·외부[NE]). 평가 가능 4단 전부 통과 = CONDITIONAL(상한). ROBUST 도달 불가는 설계 사실.

### 5.4 응답층
플랫폼별 분리, 플랫폼 내 백분위, 신호 有/無 게시물의 중앙 백분위 비교(n, IQR, 부트스트랩 CI). n<10 QUALITATIVE. 허용 문장: "이 신호는 이 코퍼스에서 더 높은/낮은 관측 반응과 공존했다". 금지: 참여=선호/설득/구매의도.

### 5.5 정렬 판정(Desk 결합 시 적용, 현재 run에서는 미부여)
입력 튜플 (S 공급등급, P 유료의존, X 외부전이, C 비교군 공통성, F 지속성, L 사다리) + Desk fate → 결정표. 단일 p값으로 결정하지 않는다.
| 최종 상태 | 정의 | Q4 리스트 / 기본 결정 |
|---|---|---|
| ALIGNED_CORE | 광고 신호 MATERIAL ∧ 소비자 증거 수용/유지 | KEEP AS SUPPORT(NEVO 고유이면 OWN) / KEEP |
| SUPPORTING_RTB | 신호 존재, 부분 유지, 브랜드 선택 축 아님 | KEEP AS SUPPORT / KEEP |
| CATEGORY_HYGIENE | S9/Philips/카테고리 공통, NEVO 소유 불가 | KEEP AS SUPPORT(OWN 금지) / KEEP·REDUCE |
| OVER_COMMUNICATED_UNTRANSLATED | 신호 MATERIAL, 소비자 언어 부재 | STOP/DE-EMPHASIZE / REDUCE(STOP 조건부) |
| OVER_COMMUNICATED_REJECTED | 신호 MATERIAL, 소비자 거부 | STOP/DE-EMPHASIZE / STOP 또는 REPOSITION |
| TRANSFORMED_BY_MARKET | 의미는 살되 다른 문제/가치로 번역 | OWN/BUILD(재프레임) / REPOSITION |
| UNDERCOMMUNICATED_WHITESPACE | 소비자 필요 MATERIAL, 광고 신호 약함 | OWN/BUILD / OWN(THIN이면 TEST) |
| INSUFFICIENT | 증거 희소 | TEST 부록 / NO_DECISION |
전체 상태: ALIGNED / PARTIALLY_ALIGNED / STRUCTURALLY_MISALIGNED / NO_DECISION(≥4 INSUFFICIENT).

### 5.6 결론 강도 어휘(현재 run 구속)
HIGH · MEDIUM · DIRECTIONAL · INSUFFICIENT · NOT_MEASURED · LOW_OBSERVED_WITH_COVERAGE_CAVEAT. "광고에 없다"는 금지. whitespace 검정(AS-03 MATERIAL ∧ W1·W2 LOW)은 AS-03이 LOW라 PREMISE_NOT_MET.

### 5.7 금지 추론
engagement=선호 · 유료 긍정=만족 · 게시물 수=점유율 · English=US · Korean=Korea · Syncly 부재=소비자 거부 · Desk 302/305=모집단 · 공급 높음=효과 높음 · 조회수=설득 · p>.05=동일 · S9 희소 셀=차이 없음.

### 5.8 품질 게이트 QA1–17(17/17 필수)
QA1 Desk CL 9개 표현 · QA2 Desk 판정 불변 · QA3 광고 공급과 소비자 수용 분리 · QA4 유료/무료 분리 · QA5 브랜드/외부 분리 · QA6 플랫폼 분모 명시 · QA7 크리에이티브 결측 명시 · QA8 응답 플랫폼 정규화 · QA9 참여→선호 추론 없음 · QA10 비교군 역할 보존 · QA11 히트맵 셀→post_id 추적 · QA12/13 모든 권고에 반증·Desk+Syncly 증거 · QA14 whitespace는 낮은 광고 신호로 입증 · QA15 라이프사이클에 두 clock · QA16 3,435 1차 분모 · QA17 D00 68 미혼합.

---

## 6. 효용 판단 — 이 데이터로 답할 수 있는 것

| 질문 | 가능 여부 | 근거 |
|---|---|---|
| 광고가 어떤 주장을 얼마나 밀었는가 | 가능 — DIRECTIONAL | NEVO Tier A 63 위 13코드 공급 등급, 유료 집중, 플랫폼·행위자 분포 |
| 누가 어디서 증폭했는가 | 부분 | 플랫폼·홍보·행위자 매트릭스 성립; 크리에이티브 유형은 결측 지배 |
| NEVO만의 광고 언어인가 | 가능 — DIRECTIONAL, 단 사전 비대칭 코드 제외 | K1/K2 각 11검정; AS-01(K2)·AS-06·AS-07/08(K1)은 INSUFFICIENT |
| 광고 신호가 소비자 언어까지 살아남았나 | Desk 결합 후 | 현재 run은 Desk 미열람. 결합은 별도 결정 |
| 출시 후 메시지가 이동했나 | 제한적 | 5주 burst만. 형태 비교만 |
| 참여 반응이 높았나 | 정성만 | 46/49 셀 n<10 |
| 같다/차이 없다 | 불가 | TOST 불가 |
| 제품×행위자 상호작용 | 불가 | Brand 셀 7/7/0 |

종합: 설계·검증 절차는 재현 가능하고 원장에 남아 있다. 결론의 강도는 데이터가 정한다. 이 코퍼스는 "무엇을 세게 말했는가"에는 답하지만 "그것이 통했는가"에는 답하지 못하며, 후자는 Desk 소비자 원장과의 결합으로만 부분 응답된다.

---

## 7. Desk 인계 자산 판단(요청 ①)
자산 인계(단계적) 권고. CREATOR 광고 표현(전문 24·미리보기 79)이 최대 actor 층이므로 BRAND 단독 축소는 §14 비교를 포기하는 선택. RETAIL은 어느 쪽이든 결손(NEVO 소매 전문 0). 넘기는 것은 광고 표현 원문·출처·actor·홍보·플랫폼·언어·tier뿐, 소비자 해석 없음. 상세: DESK_HANDOFF_DECISION_ADVICE.md.

## 8. 남은 단계
현재 run 봉인 완료 → extension(RUN-V25-ADVERTISING-REALITY-HANDOFF-001): CLAIM_ID_CROSSWALK·DESK_INTERFACE_SCHEMA 완료, AD_EXPRESSION_BANK·FAMILIES·ANCHOR_REGISTRY, 03/04/05 문서, H1–H12 atlas, Panasonic identity registry(1차 출처) 진행 중; Panasonic 수집 수단과 §19–21 지시문은 Human 결정 대기. 최종 Desk merge 금지.

## 9. 근거 파일
control/v25_ad_signal/{RUN_STATE.json, AD0_DESIGN_DECISIONS.md, G3_POST_MART_VERDICT.md, CP2_DENOMINATOR_AUDIT.md, CP3_VERIFICATION_ROUND1/2.md, LEXICON_ROBUSTNESS_VERDICT.md, COUNTEREVIDENCE_LEDGER.csv, CURRENT_RUN_SEAL_MANIFEST.csv, docs/METHODOLOGY_DISCLOSURE.md}, control/v25_ad_signal/qa/{AD_SIGNAL_FIELD_INVENTORY.md, LEXICON_FP_AUDIT_FULL.md, ADSIG_LABEL_AUDIT_C.md, CE_LEDGER_REVIEW_C.md}, control/v25_comparator_universe/{ROOT_PROBLEM_VERDICTS_CU0.json, COMPARATOR_CONTENT_LAYER_CLOSURE.md}.
