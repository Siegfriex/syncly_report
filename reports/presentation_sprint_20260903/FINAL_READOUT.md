# NEVO LAUNCH CAMPAIGN — SOCIAL PERFORMANCE READOUT (FINAL · numbers frozen 14:48 KST · private commit 2d999d0)

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
| 14 | Cohort 시간축 | W31 0 · W32 0 · W33 28 · **W34 74** · W35 25 (광고 공급 1/9/6/34/19와 별도 패널; 한 선으로 그리지 않음) | 127 vs 69 | B 02c_GONG_YOO_TIMELINE |
| 15 | Cohort 자기 언어(literal token) | 실크 35% · 12년 만의 플래그십 19% · 이벤트/증정 18% · 플래그십 14% · 가격 7% · 피부 6% · 프리미엄 3% | 127 | B 02b_GONG_YOO_CONTENT |
| 16 | Cohort∩NEVO set 19건의 gold claim | 가격 정당화(CL09) 12/19 — 그러나 cohort 표면 어휘는 premium 4 / price 9 → 앰배서더는 '새로움·플래그십·실크'를 말했고 '왜 비싼가'는 말하지 않았다 | 19 / 127 | B 02b, 02 gold mart |
| 17 | Cohort 대표 게시물(서술 예시만) | views 152,998 / 144,552 / 58,109 — 상위 2건은 이벤트·외모 콘텐츠, 제품 claim 아님; 전부 PAID | 127 (22건 views 미보고) | B 02d |
| 18 | Cohort PAID vs ORGANIC | INSUFFICIENT (ORGANIC n=3, SUSPECTED n=10) | 127 | B 02e |
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



## CAMPAIGN VERDICT (A 작성, C 승인 — private 09_CAMPAIGN_VERDICT.md)
**한 문장:** NEVO 런칭은 "12년 만의 플래그십이 나왔다"를 알리는 데 성공했고, "그래서 1.7배를 낼 이유"를 만드는 데는 아직 도달하지 못했다. 다음 과제는 경쟁사 방어가 아니라 Series 9와의 분리다.

**ACHIEVED**
- '덜 쓸린다' 한 문장을 시장 표면에 얹음 (50 dedup posts, 117 families 중 claim별).
- 런칭 이벤트 주(W34) 공급 집중 34/69; 앰배서더 코호트도 같은 주 정점 74/127 (W31–W32에는 부재, W33 시작).
- 24% 숫자는 죽었지만 피부 결과어 생존 (Human Gold 41/144; 정확 24% 0/144).
- 앰배서더가 '12년 만의 플래그십·실크' 신제품 현저성과 증폭량을 만듦 (실크 45/127, 12년 0.189, 플래그십 0.142).

**NOT YET PROVEN**
- ⓪ 앰배서더는 '왜 비싼가'를 말하지 않았다: 프리미엄 4/127, 가격 9/127. 겹침 19건의 claim 코드는 가격 정당화 12/19이나 본인의 언어는 실크·12년. → 인지도는 샀고 가격 근거는 사지 못했다.
- ① Series 9와의 분리: 비교 가능한 8개 claim 전부 공유, 5개 미측정 (13 중 분리 0). 가격 정당화조차 S9 37 : NEVO 27.
- ② 프리미엄 수용: 저항 38 vs 정당화 17 (144); 채널별 커뮤니티 19:4 · 리테일 리뷰 15:13 · 영상 댓글 4:0 → 지불하는 목소리는 다른 채널에.
- ③ 피부 결과 소유권: semantic 이웃 15 중 타사 14 (미증명, 반증 아님).
- ④ 소재(316L)의 구매 동인: 지지 발화 2, 선택 동인 ABSENT.
- ⑤ 내구성: need 22(P5)·113 이웃, 316L→버튼·배터리·헤드 고장 해결 기전 증거 0.
- ⑥ 브랜드 자기 음성: 3/69 unique posts (4 claim×post 쌍).

**NEXT MOVE** — KEEP 0 · OWN 0 · REPOSITION 2 (저마찰→피부 결과 언어; 가격 정당화→사용·소유 경험 증명) · REDUCE 3 (24% 수치, 센서 기술어, 독일 제조) · TEST 8 (316L 구매 동인, 유지관리/교체주기 need 34·39 vs 공급 0, 신뢰성 기전, 보증 등). 앰배서더 2차는 '새로움'이 아니라 '왜 비싼가'를 말하게 할 것.

## SLIDES 2–6 (headline · primary number · visual) — scripts in private A_SLIDE_SCRIPTS.md
| Slide | Headline | Primary number | Visual |
|---|---|---|---|
| 2 무엇을 가장 많이 말했나 | 런칭이 시장에 얹은 문장은 두 개였다. "덜 쓸린다" 50, "비싼 값을 한다" 27 | 50 / 27 (claim별 dedup, 합산 금지); W34 34/69 | S4_WEEKLY_SUPPLY + V2_MESSAGE_SUPPLY |
| 3 누가 운반했나 (해석 규칙) | NEVO를 말한 것은 Braun이 아니었다. Brand 직접 3/69 | MEDIA_EVENT 33/69; dominant 8/10 claims | S1_WHO_CARRIED_IT |
| 4 브랜드 밖에서 어떻게 바뀌었나 | 죽은 것은 24%라는 숫자다 | PARAPHRASE 10 / INSUFFICIENT 11 (21); 24% 정확 인용 0/144 | V5_24PCT_TRANSLATION + S3_TRANSLATION_FLOW_TOP3 |
| 5 말한 것과 가져간 것은 같았나 | engagement로는 답할 수 없다. 측정이 안 된다 | coverage likes 0.565 · views 0.507 · er 0.406 (69) vs cohort 0.677 · 0.827 · 0.717 (127, REELS 보고면) | S5_RESPONSE_COVERAGE_GAP + S6_GONG_YOO_COHORT_STRIP |
| 6 무엇을 만들었고 무엇을 남겼나 | 첫 경쟁자는 Philips가 아니었다. Braun 자신의 Series 9였다 | 13 claims 중 S9 분리 0 (8 공유 + 5 미측정) | S2_CLAIM_FATE_STRIP (+ V6, V7 appendix) |

## WHAT NOT TO CLAIM
도달·노출·점유·선호·설득·인과·노출→수용; "브랜드 게시물 4건"(4는 쌍, 고유 3); "0/13 전패"(8 미분리 + 5 미측정); 앰배서더 vs 광고 claim 성과 비교(측정면 다름); 코호트 127과 광고 69를 한 곡선으로; 상위 REELS 조회수 = 성과; "Braun은 교체주기를 말하지 않았다"(공급 0 = 미관측); Panasonic 비교 수치의 크기.

## A/B/D FINAL STATES
| Lane | Wave 1 | Wave 2 | C verdict |
|---|---|---|---|
| A 캠페인 스토리 | TOP10 findings + A1–A7 (361d7c5) | 09 verdict + slide scripts (0153b4d) | ACCEPT (C 정정: 타이밍 문구 1건; 분모 검사 0 flags) |
| B 소셜 성과·증거 | snapshot, coverage, cohort 127 (dbc9892) | cohort content/timeline/examples (64f1cb3) | ACCEPT (0 MCP; frozen denominators untouched) |
| D 결과 시각화 | S1–S3 + 4 tables (f65291a) | S4–S6 + final manifest (7ca9634) | ACCEPT (C visual QA; S2 CL02 fix) |

## PRIVATE ARTIFACT POINTERS + HASHES (syncly_demo, commit 2d999d0; A denominator-label audit 9a96ace included)
| path | sha256[:16] |
|---|---|
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/00_RUN_STATE.json | 7f96027b6dd33260 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/01_CAMPAIGN_SNAPSHOT.csv | 63bfc15edf8239f1 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/02_GONG_YOO_COHORT.csv | 2698fb9dfb0ba2f4 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/02b_GONG_YOO_CONTENT.csv | 583f224d67811aaf |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/02c_GONG_YOO_TIMELINE.csv | fd6e081e5baaef77 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/03_MESSAGE_SUPPLY_TOP5.csv | c00518664bf14829 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/04_ACTOR_PERFORMANCE.csv | 24fed8b994af7bf2 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/05_RESPONSE_PERFORMANCE.csv | ab5e4fb0570073b5 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/06_TRANSLATION_TOP3.csv | 717d4661c5ce577e |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/07_SERIES9_CONSTRAINT.csv | 71659967e0d35a91 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/08_PREMIUM_FRAMING.csv | 6aff7de72959b91e |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/09_CAMPAIGN_VERDICT.md | 906a206ad922b6ec |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/10_PRESENTATION_FLOW.md | f8c09ea608688122 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/A_TOP10_FINDINGS.csv | 603ac7a19f3d9ca6 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/A_SLIDE_SCRIPTS.md | 222469e520a1a74e |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/B_METRIC_COVERAGE.csv | add0afd2b988c662 |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/viz/D_SPRINT_VIZ_MANIFEST.csv | 54d19e49d3f18cbe |
| runs/v25/FINAL_ALIGNMENT_90MIN/PRESENTATION_RESULT_SPRINT_20260903/SPRINT_SHA256.csv | 43702c9095b24cdc |

Sealed closeout authority: runs/v25/FINAL_ALIGNMENT_90MIN/FINAL_CLOSEOUT_20260903/ (content 27535fb, FINAL_SHA256 138 rows, B SEAL_VERIFY_PASS_AT_HEAD). MCP calls this sprint: 0. POST_SEAL_SUPPLEMENT: none authorized.
