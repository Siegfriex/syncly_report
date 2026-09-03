# NEVO × Syncly 데이터 효용 브리핑

작성 Claude C (assurance / control plane) · 2026-09-03 09:13 KST · 대상 Human · 상태: CP3 검증 단계(Desk 결합 전)

**한 줄 요약: 3,435건 동결 코퍼스 위에 광고 신호 측정 체계가 검증된 상태로 올라와 있으나, 전문 텍스트가 268건뿐이어서 판정 상한은 "방향성(DIRECTIONAL)"이고 응답층은 정성 수준이다. 방법은 맞고, 데이터는 얇다.**

## 1. 큰 숫자

| 항목 | 값 | 의미 |
|---|---|---|
| 동결 코퍼스 | 3,435 posts (sha f8d130c2…1594, cutoff 2026-08-31) | 모든 1차 결과의 분모. 불변 |
| 전문(Tier A) 텍스트 | 268 = 기존 182 + EM1 신규 86 | 코드 대부분은 이 268에서만 평가 가능 |
| NEVO Tier A | 63 (of 231 entity posts) | 광고 신호 주 분모(E). 설계 셀과 정확히 일치 |
| Series 9 / Philips / Laifen Tier A | 43(44) / 29 / 5 | 비교군. Laifen은 정성 전용 |
| 미리보기(203자)만 있는 행 | 3,167 (92.2%) | FULL_TEXT_ONLY 코드는 여기서 평가 불가(NOT_EVALUABLE) |
| 언어 미커버 행 | 442 → 코드별 NE | AR/TH/BN/ZH/RU + 언어 미판정 92 |
| creative type 결측 | 3,150 / 3,435 | 메타데이터 부재. 추정하지 않음 |
| D00 추가 68건 | SUPPLEMENTAL(분모 밖) | 디스크 재파싱으로 복구, sensitivity 전용 |

## 2. 데이터 규모와 구성

플랫폼: Instagram Reels 880 · YouTube Shorts 853 · Instagram Post 643 · Facebook 560 · TikTok 318 · X 181. 기간: ISO 2026-W31~W35(5주, 출시 burst 구간만). 홍보 유형: PAID 2,554(이 중 1,616은 보완 규칙으로 파생) · ORGANIC 670 · SUSPECTED 211. 행위자: Brand 51 · Retail 76 · Commerce 122 · Media 56 · Reviewer 71 · Creator 780 · Other 2,279(핸들 미해결 66%).

언어(텍스트 기준): en 2,335 · ko 765 · vi 62 · es 29 · pt 25 · de 24 · id 16 · fr 14 · ar 14 · tr 14 · th 10 · zh 9 · ja 8 · 미판정 92. 사전이 있는 언어는 KO/EN/DE/JA/FR/PT/ES/IT/VI 9개.

참여 지표 가용성: views/er/subscribe_count는 Instagram Post·Facebook에서 100% 0(=결측), shares는 X·TikTok에서만, collect_count는 TikTok 전용, saves는 어디에도 없음. 팔로워 분모 없음. 따라서 응답층은 플랫폼 내부 백분위로만 계산했다.

시계열: 출시 기준 주차(week_from_launch)는 데이터에 존재하지 않고 시장도 게시물 단위로 미해결이라, ISO 주차를 1차 축으로 쓰고 KR(8/24)·JP(7/31) 두 기준 clock을 민감도 열로 둔다. W5~W8은 설계상 관측 불가.

## 3. 데이터 품질 — 무엇이 검증되었고 무엇이 결함인가

### 3.1 수집층 근본 원인(B-0079, 3층 분리 원장)

- RC-Q 쿼리 설계: 최대 쿼리 A01(코퍼스 53%)이 제품 seed를 배제한 라이프스타일 쿼리. 비-Braun 비교군은 co-mention으로만 존재.

- RC-F fetch 예산: Cycle 1 상세 조회 27/835건이 파일 순서상 전부 NEVO. Series 9는 P03 쿼리에 92%가 있어 조회 우주 밖 → 텍스트 확보 격차(NEVO:S9 = 1.05:1 수집 → 20:1 텍스트). EM1 89콜로 실증 해소(S9 External×PAID 3→29, Philips 4→26).

- RC-P 파서 regex: 단일 파일(D00 page_0002) 결함이 오염 13행·손실 68건·집계 23을 동시에 만듦. 38페이지 전수 감사에서 결함 파일은 1개뿐.

### 3.2 검증 결과(C 독립 재현)

| 검증 항목 | 결과 |
|---|---|
| EM1 MCP 89콜 | pool 89/89, raw sha 전수 일치, 실패 0; 크롤 교차검증 62 EXACT + 2 PREFIX / 64, 불일치 0 |
| entity 재탐지(v2.5) | 86 admit / 3 제외(오염 1, bare "prestige" 오탐 2) |
| 광고 신호 post mart | C 독립 코더 vs D: 13 claim 코드·10 역할 코드 3,435/3,435 동일; 언어·tier 3,435/3,435 |
| 매트릭스 6종 | 398/398 셀 (k, E) 동일; 셀→post_id 인덱스 641/641 |
| 비교군 검정 | K2(vs Philips) 11/11 동일; K1(vs S9) 이중 entity 1건 처리 차이 → AS-08만 BH 경계 |
| 블라인드 라벨 감사(광고 신호) | 40표본: D 양성 전부 실제 사전 사례, tier 규칙 위반 0; 언어 커버 규칙 오류 1건 → 수정 완료 |
| 블라인드 라벨 감사(v2.5 비교군 코드북) | 1차 FAIL(사전 KO/EN뿐, 헤더 오코딩) → 재실행 → 2차 CH/N/PGX 통과, PMO 가족 FAIL → 3차 수정 진행 중(P1) |

### 3.3 남은 결함·한계(공시 대상)

- 사전 공백: AS-06(케어 시스템), AS-W2(보증 후 증명), AS-W3(유지 부담), MR-PROMOTION, MR-CONVENIENCE — 이 코드의 "낮음/없음"은 반드시 caveat 부착.

- creative type 3,150 결측 → H5(주장×크리에이티브)는 사실상 메타데이터 결측 보고.

- 응답층: 49행 중 46행이 n<10 정성. ORGANIC NEVO 전문은 2건뿐이라 유료/무료 응답 비교 불가.

- Brand 셀(NEVO 7, S9 7, Philips 0)이 상한이라 제품×행위자 상호작용 추정 불가, 강건성 사다리 5·6단 평가 불가 → ROBUST 도달 불가(상한 CONDITIONAL).

- 등가(TOST) 판정 불가: 팔당 135건 필요, 최대 63.

- 구현 독립성: D가 C 참조 코더를 그대로 채택해 이중 구현 독립성이 사라짐. 블라인드 감사 2회로 대체(방법 노트).

- prereg 사후 추가 2회(§N-2 판정→Q4 매핑, lexicon v1.1 regex 수리) — 모두 판정값 산출 전, sha 이력 기록.

## 4. 분류 코드북과 판정 기준

### 4.1 광고 신호 코드북 AD_SIGNAL_CODEBOOK_v1 (동결, sha 79a831dd…)

단위 = 게시물 1건. 이진 다중 라벨. 토큰 출처는 동결 사전(1,935 정규식, 9개 언어)만 허용. 기질 = 캡션+자막(메타데이터 헤더 제거). 언어 선언 후 (코드, 언어) 사전이 없으면 NOT_EVALUABLE(절대 0 아님).

| 축 | 코드 | 대응 Desk 코드 | 텍스트 tier |
|---|---|---|---|
| 주장 AS-01 | 저마찰 포일 / 밀착+편안함 | CL-01 | EITHER |
| AS-02 | 24% 마찰·글라이드 수치 | CL-02 | PREVIEW_SAFE |
| AS-03 | 316L/스테인리스 유니바디/소재 | CL-03 | FULL_TEXT_ONLY |
| AS-04 | Made in Germany | CL-04 | EITHER |
| AS-05 | 장기 보증(5년) | CL-05 | FULL_TEXT_ONLY |
| AS-06 | 케어 시스템(SmartCare/7in1) | CL-06 | FULL_TEXT_ONLY |
| AS-07 | 적응형 센서(340회/초) | CL-07 | FULL_TEXT_ONLY |
| AS-08 | 18개월 교체 주기 (+파생 프레임 F_CONV/F_MAINT/F_NEUTRAL) | CL-08 | FULL_TEXT_ONLY |
| AS-09 | 프리미엄 가격 정당화 | CL-09 | EITHER |
| 공백 AS-W1 | 장기 신뢰성/안 망가짐 | GAP-01 | FULL_TEXT_ONLY |
| AS-W2 | 보증 후 증명 | GAP-02 | FULL_TEXT_ONLY (근거 THIN) |
| AS-W3 | 유지 부담/소모품 비용 | GAP-03 | FULL_TEXT_ONLY (KO THIN) |
| AS-W4 | 구체적 면도 실패 | GAP-04 | FULL_TEXT_ONLY |
| 메시지 역할 MR ×10 | HOOK/BENEFIT/RTB/PRICE_JUSTIFIER/OWNERSHIP/CONVENIENCE/QUALITY_CUE/PROMOTION/SOCIAL_PROOF/CATEGORY_HYGIENE | — | 다중, 강제 단일화 없음 |
| 크리에이티브 CT ×11 | DEMO/EXPLAINER/LIFESTYLE/AMBASSADOR/EVENT/REVIEW/COMPARISON/RETAIL_PROMO/STATIC/UGC/OTHER + MISSING | — | 분석기(60건) 또는 명시 텍스트 단서만; 부재로 추정 금지 |

### 4.2 판정 기준(결과 보기 전 동결)

- 공급 등급: MATERIAL ⇔ share ≥ 20% ∧ Wilson 95% 하한 ≥ 10% ∧ k ≥ 5; LOW ⇔ Wilson 상한 < 20%; 그 외 INDETERMINATE. E<10 QUALITATIVE_ONLY, 10–19 등급 보류.

- 분모 E = 해당 코드에서 평가 가능한 NEVO Tier A(63). PREVIEW_EXTENDED는 PREVIEW_SAFE 코드에만 별도 열, 등급 상향 불가.

- 통계: α=.05 양측, BH-FDR q=.05는 동결 가족 2개(NEVO vs S9, NEVO vs Philips; 각 11검정)에만. 효과 크기 Cohen h ≥ .20 + pp. 출처 블록 순열검정 10,000회.

- 강건성 사다리 6단(raw/메시지군 dedup/최상위 출처 제외/플랫폼 층화/유료·무료/브랜드·외부). 5·6단 평가 불가 → 상한 CONDITIONAL.

- 정렬 판정 8상태(ALIGNED_CORE / SUPPORTING_RTB / CATEGORY_HYGIENE / OVER_COMMUNICATED_UNTRANSLATED / OVER_COMMUNICATED_REJECTED / TRANSFORMED_BY_MARKET / UNDERCOMMUNICATED_WHITESPACE / INSUFFICIENT)은 (공급, 유료 의존, 외부 전이, 비교군 공통성, 지속성, 사다리) 튜플 + Desk fate로 결정표 적용. 단일 p값으로 결정하지 않음.

- whitespace 검정: AS-03 MATERIAL ∧ W1·W2 LOW 이면 MESSAGE_WHITESPACE_CONFIRMED, 단 W2/W3 사전 THIN caveat 동반.

### 4.3 v2.5 비교군 콘텐츠 코드북(보고서 비교군 섹션 입력)

CB_v2.4.0(legacy: CH1–CH6 카테고리 위생, PG0–PGX 프리미엄 문법, PMO 문제→기제→결과, N1–N4 endorser)은 감사에서 비교군 비중립(CH4·PMO 기제·PG1이 Braun alias 편향, CH6 느슨)으로 판정되어 CB_v2.5.1 COMPARATOR_NEUTRAL(sha a73c4e5d…)을 병행 트랙으로 동결했다. 두 코드북은 항상 분리 실행·분리 보고. 현재 라벨 구현은 3차 수정 중(PMO 가족, CH3 트리거)이며 이 결과는 아직 봉인되지 않았다.

## 5. 효용 판단 — 이 데이터로 무엇을 말할 수 있는가

| 질문 | 가능 여부 | 근거 |
|---|---|---|
| 광고가 어떤 주장을 얼마나 밀었는가(Q1) | 가능 — DIRECTIONAL | NEVO Tier A 63 위 13코드 공급 등급, 유료 집중도, 플랫폼·행위자 분포 |
| 누가 어디서 증폭했는가(Q2) | 부분 가능 | 플랫폼·홍보·행위자 매트릭스는 됨; 크리에이티브 유형은 결측이 지배 |
| NEVO만의 광고 언어인가(비교군) | 가능 — DIRECTIONAL | K1/K2 각 11검정, 방향 일관 |
| 광고 신호가 소비자 언어까지 살아남았나(Q3) | Desk 결합 후 가능 | Desk fate(불변) × Syncly 튜플 결정표. 현재 결합 직전 |
| 광고가 출시 후 이동했나(T9) | 제한적 | 5주 burst만 관측, W5+ 불가 — 형태 비교만 |
| 참여 반응이 높았나 | 정성만 | 46/49 셀 n<10; 참여=선호 추론 금지 |
| 같다/차이 없다 | 불가 | TOST 도달 불가(팔당 135 필요) |
| 제품×행위자 상호작용 | 불가 | Brand 셀 7/7/0 |

**종합: 설계·검증 절차는 재현 가능하고 원장에 남아 있다. 결론의 강도는 데이터가 정한다 — 이 코퍼스는 "무엇을 세게 말했는가"에는 답하지만 "그것이 통했는가"에는 답하지 못하며, 후자는 Desk 소비자 원장과의 결합으로만 부분 응답된다.**

## 6. 남은 단계

- CP3 2라운드 검증(K1 61 재실행, Human §19 6방향 반증 원장) — 수신, 검증 중

- G5 Desk fate 결합 → MESSAGE_MARKET_ALIGNMENT / CLAIM_ALIGNMENT_VERDICTS(C) — Human 지시로 결합 전 정지

- G6 반증 감사 → G7 판정 봉인 → A 해석(A-ADSIG-001) → C 적대 검토 → FINAL_AD_SIGNAL_REPORT(bones 13개, 슬롯 2,483 준비) → SEAL

- v2.5 비교군 라벨 3차 수정(D-V25-006, P1) → 보고서 08 섹션 입력

근거 파일: control/v25_ad_signal/{RUN_STATE.json, AD0_DESIGN_DECISIONS.md, G3_POST_MART_VERDICT.md, CP2_DENOMINATOR_AUDIT.md, CP3_VERIFICATION_ROUND1.md, HUMAN_ESCALATIONS.md}, qa/AD_SIGNAL_FIELD_INVENTORY.md, control/v25_comparator_universe/ROOT_PROBLEM_VERDICTS_CU0.json.
