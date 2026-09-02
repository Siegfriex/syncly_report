# HUR-009 — AD1~AD5 UI 생성용 복붙 시트 (A-0053 RATIFIED spec v1.1 · exact · v2.2로 변경 없음)

작성: Claude C · 2026-09-02 15:35 KST · 정본: `control/rotation/AD_BATCH_QUERY_SPEC_SHEET_v1.md` (A-0053, 2026-09-02T03:52:00Z 비준, AD3 = 옵션 A)
형식: Baseline P03 화면과 동일한 필드 순서(legacy `queries/Q4_P03_Braun_Series9.yaml` 구조). keywords·relevance는 spec v1.1에서 **한 글자도 바꾸지 않고** 옮겼다. AD2·AD5의 relevance 마지막 문장은 spec §0 공통 규칙("relevance 문안에도 '면도/브랜드 언급은 관련성 근거가 아니다'를 명시")에 따라 포함한 것이다.

**v2.2 관련 주의**: Query 정의는 v2.1 A-0053 그대로다. KR/EN 분할 금지, 용어 추가 금지. Language/Market은 downstream 필드로 붙는다(Addendum §7·§27·§32).
**금지**: P03 등 Baseline Query 재생성 금지. Delete 금지(Archive만, 단계적·C-0085 canary). UI가 6번째 Query 생성을 거부하면 변경 없이 중단하고 C에 통보.

## 공통 (5개 동일)
- query_type: **Topic**
- accounts_to_track: [] · exclude_keywords: [] · exclude_accounts: []
- platforms: TikTok · Instagram Reels · Instagram Post · YouTube Shorts · X · Facebook
- history: UI가 허용하는 가장 긴 backfill (Baseline 1 MONTH 규칙 준용)
- 생성 직후 캡처: query_id · tracking_since · keyword 화면 · relevance 저장본 · platforms · backfill · 스크린샷 1장 → C

---
```yaml
query_type: Topic
query_name: AD1_PremiumConsumption_HighInvolvement
keywords:
- 프리미엄 소비
- 명품 리뷰
- 하이엔드
- 플래그십
- 소장 가치
- 프리미엄 오디오
- 기계식 시계
- 프리미엄 가전
- premium consumption
- luxury review
- high-end
- flagship product
- collection piece
- premium audio
- mechanical watch
- premium appliance
accounts_to_track: []
exclude_keywords: []
exclude_accounts: []
platforms:
- TikTok
- Instagram Reels
- Instagram Post
- YouTube Shorts
- X
- Facebook
history_rule: UI가 허용하는 가장 긴 backfill
relevance: '품질·소재·마감·브랜드 헤리티지·소유 경험을 실질적 중심 주제로 다루는 고관여 소비재(시계·오디오·자동차·가전·가구) 콘텐츠와 그것을 반복 생산하는 큐레이터/리뷰어/매체. 단순 명품 해시태그·판매링크-only·경품 제외. 면도기/브랜드 언급은 관련성 근거가 아님.'
```

```yaml
query_type: Topic
query_name: AD2_Design_Material_Object
keywords:
- 제품 디자인
- 디자인 오브젝트
- 산업 디자인
- 소재 마감
- 알루미늄 유니바디
- 미니멀 디자인
- 디자인 리뷰
- product design
- design object
- industrial design
- material finish
- aluminum unibody
- minimal design
- design review
accounts_to_track: []
exclude_keywords: []
exclude_accounts: []
platforms:
- TikTok
- Instagram Reels
- Instagram Post
- YouTube Shorts
- X
- Facebook
history_rule: UI가 허용하는 가장 긴 backfill
relevance: '제품의 형태·비례·소재·마감·오브젝트성을 평가·해설하는 콘텐츠. 제품 맥락 없는 일반 미학/인테리어-only 제외. 면도기/브랜드 언급은 관련성 근거가 아님.'
```

```yaml
query_type: Topic
query_name: AD3_ConsumerTech_EarlyAdoption
keywords:
- 테크 리뷰
- 신제품 언박싱
- 얼리어답터
- 스마트 가젯
- 테크 비교
- 신기술 체험
- tech review
- gadget unboxing
- early adopter
- smart gadget
- tech comparison
- new tech hands-on
accounts_to_track: []
exclude_keywords: []
exclude_accounts: []
platforms:
- TikTok
- Instagram Reels
- Instagram Post
- YouTube Shorts
- X
- Facebook
history_rule: UI가 허용하는 가장 긴 backfill
relevance: '소비자 기술·신제품·고급/스마트 기능·기술 비교를 사용자 관점에서 다루는 콘텐츠. B2B·투자·일반 기술뉴스 제외. 특정 브랜드 언급은 관련성 근거가 아님.'
```

```yaml
query_type: Topic
query_name: AD4_MensStyle_Grooming_Selfcare
keywords:
- 남성 패션
- 남성 스타일
- 남성 그루밍
- 남성 셀프케어
- 데일리 룩
- 남성 스킨케어
- 헤어 스타일링
- menswear
- mens fashion
- mens style
- mens grooming
- mens self-care
- daily outfit
- mens skincare
- hair styling
accounts_to_track: []
exclude_keywords: []
exclude_accounts: []
platforms:
- TikTok
- Instagram Reels
- Instagram Post
- YouTube Shorts
- X
- Facebook
history_rule: UI가 허용하는 가장 긴 backfill
relevance: '면도에 한정되지 않는 남성 패션·뷰티·셀프케어·외모관리 콘텐츠. shaving/shaver/면도 및 Braun/Philips는 relevance basis로 쓰지 않음 — 면도 콘텐츠가 잡히더라도 별도 타깃 친화 신호가 있어야 포함.'
```

```yaml
query_type: Topic
query_name: AD5_Routine_Mobility_Optimization
keywords:
- 모닝 루틴
- 데일리 루틴
- 출장 필수템
- 여행 필수템
- EDC
- 미니멀 라이프
- 시간 절약 루틴
- morning routine
- daily routine
- everyday carry
- edc
- travel essentials
- business trip essentials
- minimalist routine
- time-saving routine
accounts_to_track: []
exclude_keywords: []
exclude_accounts: []
platforms:
- TikTok
- Instagram Reels
- Instagram Post
- YouTube Shorts
- X
- Facebook
history_rule: UI가 허용하는 가장 긴 backfill
relevance: '일상의 시간·준비·관리 부담을 줄이는 루틴/이동/최적화 콘텐츠. generic productivity-only 제외. 면도기/브랜드 언급은 관련성 근거가 아님.'
```

---
키워드 수: AD1 16 · AD2 14 · AD3 12 · AD4 15 · AD5 15 (ko+en). 금지 seed(Braun·NEVO·네보·Philips·필립스·shaver·shaving·면도·면도기·전기면도기) 0건, 포맷 토큰(shorts·viral·fyp·reels) 0건 — C 재확인.
