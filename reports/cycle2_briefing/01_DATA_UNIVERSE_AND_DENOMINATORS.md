# 01 — DATA UNIVERSE AND DENOMINATORS (Syncly / local lane, C, 2026-09-03T00:19:00Z)
Scope: measured facts only. No Desk content. Interpretation is A's after G7.

## 1. Primary denominator
| item | value | provenance |
|---|---|---|
| Frozen social corpus | **3,435 posts** | posts_cutoff.jsonl sha f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594 · cutoff 2026-08-31 · immutable; git-clean verified 2026-09-03 |
| Period | ISO 2026-W31–W35 (5 weeks; W31 238 / W32 769 / W33 807 / W34 860 / W35 761) | published_at |
| Platforms | INSTAGRAM_REELS 880 · YOUTUBE_SHORTS 853 · INSTAGRAM_POST 643 · FACEBOOK 560 · TIKTOK 318 · TWITTER 181 | corpus |
| Promotion | PAID 2,554 (1,616 derived by complement, flagged) · ORGANIC 670 · SUSPECTED 211 | mart parent v2.3 |
| Actor (ACTOR_v2.3.0) | Brand 51 · Retail 76 · Commerce 122 · Media 56 · Reviewer 71 · Creator 780 · Other 2,279 (handle-only, 66%) | mart parent |
| Model entity (ENTITY_DET_v2.5.0) | NEVO 227 (+3 NEVO_AND_S9) · BRAUN_S9 156 · PHILIPS_S9000 82 · LAIFEN 22 · no entity 2,945 | post mart rev 2 |
| Language (text) | en 2,335 · ko 765 · und 92 · vi 62 · es 29 · pt 25 · de 24 · id 16 · fr 14 · ar 14 · tr 14 · th 10 · zh 9 · ja 8 | C reference detector (script share ≥30%, stopword heuristic) |

## 2. Text tiers (what can be coded)
| tier | n | rule |
|---|---|---|
| Tier A (verbatim caption/transcript held) | **268** = 182 baseline ∪ 86 EM1 (MCP get_post_details, 89 calls, 86 admitted after v2.5 entity re-detection) | all codes evaluable (language permitting) |
| Tier C (203-char preview only) | 3,167 | PREVIEW_SAFE codes only; FULL_TEXT_ONLY codes = NOT_EVALUABLE (never 0) |
| Contaminated previews | 13 rows (foreign text) → true_preview substituted, flagged preview_corrected=1 | R-8 |
| Language uncovered (no lexicon) | 442 rows at CP1 → per-code NOT_EVALUABLE (ar/th/bn/zh/ru + und 92) | AD0-10 |

Tier A by family: **NEVO 63** (primary E; incl. 2 dual units excluded from K1) · SERIES_9 43 (29–33 evaluable) · PHILIPS_S9000 29 (21–24 evaluable) · LAIFEN 5 · Cycle-1 pooled REF 68.
NEVO Tier A by platform: IG Reels 26 · IG Post 17 · FB 9 · X 7 · YT Shorts 3 · TikTok 1. By promotion: PAID 49 · SUSPECTED 12 · ORGANIC 2. Brand-authored: 7.

## 3. Off-denominator material
| set | n | status |
|---|---|---|
| D00 supplement (parser loss, re-parsed from disk) | 68 (55 with crawl text) | PF-C1_SENSITIVITY_LEDGER — OFF_PRIMARY_DENOMINATOR, never mixed (QA17) |
| Panasonic | 17 brand mentions in corpus, 0 family entity, 0 verbatim | NOT A COMPARATOR in this run; separate epoch if collected later |

## 4. Response-metric availability (why the response layer is qualitative)
views/er/subscribe_count = 0 for 100% of INSTAGRAM_POST and FACEBOOK (treated as MISSING); shares only TWITTER/TIKTOK; collect_count TikTok only; saves absent everywhere; no follower field. Metric used only where platform coverage ≥50%; percentiles computed within platform over all 3,435. Result: H7 49 rows, 46 with n<10 → QUALITATIVE_ONLY; NEVO ORGANIC Tier A = 2 → no paid/organic response comparison.

## 5. Creative type
Rated for 0 posts in metadata; assigned only from VIDEO_ANALYZER FORMAT_ARCHETYPES (60 feature posts) or explicit text cues: MISSING 3,150 / RETAIL_PROMO 84 / EVENT 83 / REVIEW_TESTIMONIAL 49 / OTHER 36 / AMBASSADOR 15 / LIFESTYLE 11 / FEATURE_EXPLAINER 4 / PRODUCT_DEMO 3. H5 is therefore a missingness table (QA7).

## 6. Time axes
No launch-relative week exists in the data and market is unresolved per post. Primary axis = week_iso (W31–W35). Sensitivity clocks: wfl_KR (ref 2026-08-24 → W−4…W0) and wfl_JP (ref 2026-07-31 → W0…W4). W5–W8 = NOT_OBSERVED_BY_DESIGN. CLAIM×MARKET = NOT_MEASURED (no per-post market; English≠US, Korean≠Korea).

## 7. What the denominators permit
| question | ceiling | reason |
|---|---|---|
| NEVO claim supply ranking, paid concentration, platform/actor mix | DIRECTIONAL (E=63; slices mostly QUALITATIVE) | sparse-cell rule |
| NEVO vs Series 9 / Philips claim contrasts | DIRECTIONAL (2 BH families, 11 tests each) | arms 61/29–33 and 63/21–24 |
| NEVO vs Laifen | qualitative only | 5 |
| Product × actor interaction | NOT ESTIMABLE | Brand cells 7/7/0 |
| Equivalence ("same") | unreachable | TOST needs ≈135 per arm |
| Persistence beyond launch burst | NOT_OBSERVED_BY_DESIGN | 5 weeks |
| Response → acceptance | forbidden inference | QA9 |
