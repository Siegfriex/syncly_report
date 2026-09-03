# NEVO LAUNCH CAMPAIGN — SOCIAL PERFORMANCE READOUT (DRAFT 14:43 KST · numbers freeze 14:55)

Run `PRESENTATION_RESULT_MAX_SPRINT_20260903_1500` · 작성 Claude C · 근거 sealed `FINAL_CLOSEOUT_20260903` (private, content 27535fb) + sprint artifacts (private `runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/`)

## 캠페인 한 문장
NEVO 런칭은 Series 9보다 61–70% 비싼 제품의 프리미엄을 소셜에서 증명해야 했다. 관측된 광고 표면은 '피부에 덜 쓸리는 면도'와 '비싼 값을 한다'를 가장 많이 말했지만, 그 문장을 말한 것은 Braun이 아니라 미디어 이벤트였고, 13개 측정 claim 중 NEVO를 Series 9에서 분리한 claim은 0개였다.

## RESULT TABLE (모든 수치는 frozen corpus 3,435 posts 안의 중복 제거 게시물 수 또는 Human Gold 144 증거 두께. 시장 prevalence·선호·인과 아님)
| # | 결과 | 숫자 | 분모 | 출처(private) |
|---|---|---|---|---|
| 1 | NEVO 광고 eligible 공급 | 69 unique posts · 117 target families | frozen 3,435 posts (2.0%) | 02 gold mart, B 01_CAMPAIGN_SNAPSHOT |
| 2 | 시간축 | W31 1 · W32 9 · W33 6 · **W34 34** · W35 19 | 69 | B 01 (W34 = 8/20 런칭 이벤트 주) |
| 3 | Braun이 가장 많이 말한 것 | 저마찰 포일 50 · 가격 정당화 27 · 24% 수치 13 · 면도 실패 12 · 316L 6 | claim별 dedup posts (겹침 있음, 합산 금지) | 03a, D 03_MESSAGE_SUPPLY_TOP5 |
| 4 | 누가 운반했나 | MEDIA_EVENT 33 · OTHER_EXTERNAL 18 · CREATOR 13 · RETAIL 6 · **BRAND 3** | 69 unique posts (families: 50/39/17/7/4 of 117) | 02, C_REFERENCE_NUMBERS |
| 5 | Brand 직접 음성 | 4 claim×post 쌍 = 3 고유 게시물; dominant actor MEDIA_EVENT 8/10 claims | 69 / 10 claims | 03a |
| 6 | Brand→External 번역 | PARAPHRASE 10 · INSUFFICIENT 11 · EXACT/SHIFT 0 | 21 relations | 04, D 06_TRANSLATION_TOP3 |
| 7 | 24% 수치의 운명 | 광고 13 → 소비자 정확 인용 0 (피부 결과 41은 생존, 단 category-shared) | Human Gold 144 | CL02_LAYERED_VERDICT, 07_v2 |
| 8 | Series 9 제약 | 13 claims 중 NEVO 분리 0 (SHARED 8 · EXCLUDED 3 · NO_ROW 2); 가격 정당화조차 NEVO 27 : S9 37 | 13 claims / 32 human comparator groups | 08, 06 |
| 9 | 소유 | CATEGORY_SHARED 11 · PORTFOLIO_SHARED_S9 8 · OWNABLE_CANDIDATE 4 · EXCLUDED 9 | 32 groups | 06 |
| 10 | 응답 metric coverage (NEVO 69) | likes 0.565 · views 0.507 · comments 0.507 · er 0.406 · shares 0.014 → 0.60 gate 미달 | 69 (lower bound) | B_METRIC_COVERAGE |
| 11 | Gong Yoo cohort | 127 posts 식별(결정적 토큰; 일반동사 '공유' 제외) · PAID 114 · Creator 100 · REELS 82 · NEVO set 겹침 19 | frozen 3,435 | B 02_GONG_YOO_COHORT |
| 12 | Cohort coverage | views 0.827 · er 0.717 · likes 0.677 — REELS 보고면 때문; NEVO set과 같은 기기로 측정된 것이 아님 | 127 | B_METRIC_COVERAGE |
| 13 | 결정 | KEEP 0 · OWN 0 · REPOSITION 2 · REDUCE 3 · TEST 8 | 13 claims | 08 |

## LIMITATION TABLE
| 한계 | 의미 |
|---|---|
| Eligible set 100% PAID 플래그 | 광고 tier로 구성된 집합이라 ORGANIC 비중은 읽을 수 없음 |
| Brand 직접 카피 거의 부재 | 미수집 가능성; '브랜드 실행 실패'로 읽지 말 것 |
| 응답 metric coverage < 0.60 | claim/actor별 engagement 순위·비교 불가; 성과 정의 = 공급·운반자·번역 |
| Cohort coverage 우위 | 플랫폼 보고면 차이(REELS는 views 보고, FACEBOOK/IG POST 미보고); '앰배서더가 claim보다 성과가 좋았다' 금지 |
| 소비자 열 | lexical claim-conditioned retrieval + BGE-M3 ranking; prevalence 아님 |
| Panasonic 비교 수치 | 별도 epoch, 미감사 AUXILIARY_ANCHOR; 관계만 읽고 크기 금지 |

(A/B/D 상태, ACHIEVED / NOT YET PROVEN / NEXT MOVE, Slides 2–6, FINAL SHA는 14:55 freeze 후 확정)
