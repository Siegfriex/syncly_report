# 검증된 발견 (C 독립검증 완료분만)

갱신: 2026-09-01T22:30Z · 라벨: VERIFIED = C가 독립 재구현/재현으로 확인; PRELIMINARY = pre-LOCK 시점 산출(LOCK 확정으로 승격 후보, cutoff 재물질화 검증 후 일괄 재판정)

## 구조적 발견 (모두 VERIFIED · PRELIMINARY 라벨 병기)
1. **소스 생태 분리** — A01 소스 1,598 vs M01 소스 1,077, 공유 소스 6개뿐. 프리미엄 타깃 지향 소스의 면도 카테고리 진입 후보 12/1,271 = 0.94%. 단순 "T 실패"가 아니라 `premium target-facing source → shaving category entry gap`이라는 독립 연구질문으로 승격됨.
2. **목록계 절단(203자)** — A01 77.2% / M01 67.4% 절단. 절단 표본에서 full-text 복구 시 45.0%가 최소 1개 분류축 변경; 핵심 축(TA1) recall 24%. 트랜스크립트 기여는 8.3%에 불과 — 회수 대상은 caption. → preview-only 의미 분류는 결정-등급 아님.
3. **비교 격자 붕괴** — M01 30개 플랫폼×제품 셀 중 23개 n<10, 6개 n=0. 초점 제품(Braun S9 1.1%, Philips S9000 1.6%)은 어떤 플랫폼에서도 n≥10 미달. 이중 구현(C/D 독립)에서 구조 결론 정확 일치.
4. **플랫폼 metric 비동등성** — likes/comments만 6/6 공통; views/ER/구독 4/6; shares 2/6; saves 1/6. Facebook/IG Post는 view 분모 구조적 부재. → 크로스플랫폼 비교는 공통 코어(likes+comments) 명시 시에만.
5. **참여 합성 항등식** — 서버 Engagement = 가용 구성요소 합 (전 6플랫폼 오차 0) — 플랫폼별 구성요소 차이 확인.
6. **Paid 지배 코퍼스** — M01 서버 집계 Paid 82.8% / Organic 15.2%. → 2A~2E 분포는 "브랜드 제시 소구 빈도"이지 consumer need가 아님 (이중 게이트 유지).
7. **단일 포스트 지배** — TikTok 1개 포스트가 M01 공통코어 참여의 52.8%, 상위 2일이 67.3%. → 모든 주요 집계에 robust variants 의무.
8. **상류 목록화 이상(D00)** — 집계 계층 270 vs 목록 계층 193 (71.5%). 날짜 브래킷으로 상류 원인 확인 (materialization 무결).

9. **소스 생태 비반복 (PRF-0008, 구조 수치 VERIFIED-EXACT)** — A01 소스 1,574 중 91.0%가 1회 등장; CORE_A 77(4.9%, WINDOW-BOUND — 1개월 창 측정, 계정 행동 아님); 편집매체·매거진 CORE_A 0; 순환 누수 2.6%. source_type 세부 분포는 단일구현 관찰로 강등(코드북 v2 대기).
10. **T_S 진입 구성 (PRF-0009, VERIFIED·정성)** — 진입 6계정 중 프리미엄 편집 생태 0곳 (전자상거래 2·팬 재게시 1·바버 시연 1·해시태그 상품 1·기술 채널 1); 유일한 NEVO 증거는 팬 계정의 동일 기사 3회 재게시; census 21셀 전부 n<10 → 정량 비교 금지.

## 프로세스 기록
- 정정 13건째 전부 downstream 소비 전 포착. 상호 감사 루프 가동: C→B(층 규칙), D→C(층 판정 텍스트 기준), B 자기정정 — 삼방향 모두 작동.
- 재현성 패스: zero drift.
- 검증 분류 체계: IMPLEMENTATION-VERIFIED(독립 재구현) vs CONSTRUCT-CHECKED(도구 결함 공유 가능) 구분 운용; lexicon 측정은 negative-control 게이트 의무.

상세 근거(포스트/계정 식별자 포함)는 비공개 운영 repo의 C 감사 기록에 있음 — 본 public repo에는 집계 수치만 기재.


## 검증된 역량 발견 (2026-09-02, VERIFIED)
- **PRF-0011** — video-feature 검색이 get_post_features와 동일한 analyzer 문자열을 반환(표적 7/7 + C 1/1). discovery엔 우월, 전수 enrichment엔 결정성 부재(랭킹 비결정·post_id 주소 불가).
- **BRIDGE_CASEBOOK_6** — T_S 6계정 12건 전문(details 12 calls): 독립 unit 7; Braun을 담은 유일한 소스는 팬계정의 보도자료 재유통; 전문가 1(미국 바버·Andis); 나머지 커머스/EDC. 203자 preview가 shaver 리뷰를 테크 채널로 오독시키는 실물 표본 1건. 벤더 promotion 분류기가 구조적 동등 포스트에 다른 라벨(3/6 계정) — B가 자기일관성 측정 예정. (WINDOW-BOUND, n=12 정성)
- **PRF-0007 REBASE** — ALT-2 도달 특징 8/11=72.7%(81.8% 폐기). 도달=prose(이진 라벨 아님), 숏폼 전용, timing 미도달.

## EXPERIMENTAL (C 검증 완료 · 사람 확인 대기 · 인용 시 caveat 필수)
- **PRF-0010 video pilot (2026-09-02)** — get_post_features 60/60. 짧은 캡션(SHORT-CAPTION-SCOPE) 층1에서 영상 서술이 코드북 엔티티를 드러내는 비율 **상한 57.1%(20/35)**, 경계 제외 40.0%, 전기면도기 엔티티만 34.3%; 층2 민감도 15/15. 모든 arm MATERIAL(상한 독해: "상한이 임계를 넘었다"까지만). FB/IG Post는 영상 feature set 없음(10/10). C 검증 완료: 사전 지정 12건 독립 재호출(구절 12/12) + D가 세션 transcript에서 복구한 60건 원본(12건 겹침이 C recall과 전문 동일) 위에서 라벨 60/60·문자열 매칭 60/60·호출 순서(timestamp) 검증. 인용 규칙: electric+PRIMARY 11/35(31.4%)를 20/35와 병기, 57.1% 단독 인용 금지. 코드북 외 브랜드(DIXIX/JOAS/Daiso)는 NEG 처리됨(coverage caveat). HUI-006 사람 spot-check만 대기.
- **OBS-0003 (VOC)** — search_voc 25회 전건 무반환, 동일 질의가 summary 검색엔 반환 → 이 workspace의 댓글 index 공백. 라벨(vendor vs 수집설정)은 HUI-007 후. **CIT-07: 소비자 발화(Observed Reception)는 현재 코퍼스에서 관측 불가.**
- **PRF-0012** — top_influencers 상위 24 handle 전부 로컬 1,574 registry에 기포함(신규 0); PRF-0008 재현. AD1~AD5 vocabulary 후보는 설계 근거 전용.

## Limitation 재진단 (D d5, C-0078 수용 · 2026-09-02)
| 항목 | 재분류 | 근거 |
|---|---|---|
| 203자 preview | RESOLVED_BY_MCP (가용성) | details/features/video 검색으로 전문·analyzer 산문 회수 가능; FaceByte 실물 표본 |
| 제품 희소성 | MEASUREMENT_DESIGN_LIMIT | 코드북 ko/en 전용·브랜드 커버리지 협소(CIT-10); 단 focal 희소성은 텍스트 한계가 아님(video로도 2/35) |
| T_C 비용 | PARTIALLY_RESOLVED | 싼 경로는 영상 산문, 캡션 전문은 아님 — T_C 정의에 의존 |
| 크리에이티브 관측 | PARTIALLY_RESOLVED | 72.7% prose 도달, timing 미도달, 숏폼 전용 |
| VOC 가용성 | 미확정 (HUI-007) | 도구 정상·index 공백; vendor vs 수집설정 |
| 소스 생태 | MEASUREMENT_DESIGN_LIMIT | 1개월 키워드 Query 프레임 |
**TRUE_SYNCLY_LIMIT 확정 0건.**
- **GATE_R1 입력(Batch 0 증거기반, 허용 경로)**: market_basis HIGH/MEDIUM 도달 134/3,435(3.9%); UNKNOWN 96.1%; OFFICIAL 8·RETAIL 127(B-002 상한)/114(B-003 digit-anchored)/51(domain floor)·COMMERCE 51; CAMPAIGN 관측불가; CREATOR_LOCATION은 집계 상한만(region 89.1% 공백). 이는 Batch 0 증거기반 기술이며 KMM/EMM 한계 판정이 아니다(A-0059 R8). B-0046 / C-0103 정확 재현.
- **KR Philips premium 명명(naming-recall 진단, A01+M01 preview 3,119, C 정확 재현)**: i9000 18 · 프레스티지 16 · SkinIQ 10 · XP9xxx 5 · S9000 2. KR 비교군 Query를 S9000으로 seed하면 하위 tier(S5000/S3000)를 검색 → tier 불일치가 시장 차이로 위장. OneBlade 28~29는 하이브리드 트리머로 premium 셀에서 제외 필요(D-0049/C-0105). 유병률·점유율 아님.
- **OBS (C-0107)**: Archive 후 M01/A01의 서버 'Collected'가 감소(1,292→1,020 / 1,892→1,043)했으나 cutoff(2026-08-31) 창 총계는 canonical과 일치(A01 1,816 / M01 1,244 / P03 176) → 감소는 cutoff 이후 구간에 한정, 봉인 substrate 무손상. 원인은 미단정. archived Query의 'Collected'는 canonical 수치가 아니다(ARCHIVED-LIVE-COUNT-UNSTABLE).
- **screener 토큰 검증(D-0053, C 재현)**: held frame에서 bare '브라운' 85 hit 중 11이 면도 맥락 밖(색상 8·디자인 아이콘 3: 디터 람스/브라운 오디오) → 디자인 아이콘 포스트는 TA2 소스이므로 bare 토큰으로 screen하면 가장 전략적인 소스를 삭제. v2는 조합/동반 토큰만 허용. razor 199/shave 291(단어경계)의 맥락 밖 hit는 v1 목록 사각지대의 진짜 면도 콘텐츠.
