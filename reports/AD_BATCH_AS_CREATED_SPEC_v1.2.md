# AD Batch (Batch 1) — AS-CREATED spec v1.2 (Human UI, 2026-09-02) — C 등록본
출처: Human 덤프 `Braun_NEVO_Syncly_v2.2_Regional_Delta_Bundle_20260902/ad1_5_query.text` (sha b0d18fb40209f210ac28943f47cc3b679d889446922c9d9c0c105f5352a61591, main a0681b2). UI 'Review query details' 화면 그대로 옮김. **이 파일이 AD1~AD5의 운영 정본**(Human-only mutation; Human이 직접 생성). A-0053 spec v1.1(exact 시트)과의 차이는 C-0097에 사실로 기록되며, v1.1은 legacy로 보존한다.
query_id·tracking_since: 서버 미노출(수집 10% 진행 중) — list_data_queries에 나타나는 즉시 C가 추가.

## AD1 — `AD1_PremiumConsumption_HighInvolvementObjects`
- type: Topic · platforms: Facebook · Instagram Post · Instagram Reels · X · YouTube Shorts · TikTok · backfill: 1 month · include/exclude accounts: — · exclude keywords: — · dump occurrences: 1
- keywords (20): 프리미엄 라이프스타일 · 프리미엄 제품 · 고급 제품 · 프리미엄 가전 · 하이엔드 오디오 · 명품 시계 · 프리미엄 자동차 · 제품 품질 · 장인정신 · 소유 경험 · premium lifestyle · premium products · high-end products · premium appliances · high-end audio · luxury watches · premium automotive · product quality · craftsmanship · ownership experience
- definition:

  > 가격 자체가 아니라 제품의 품질, 소재, 제작 완성도, 브랜드 신뢰, 사용경험과 소유가치 때문에 높은 관여를 보이는 한국어 및 영어 공개 소셜 콘텐츠와 이를 반복적으로 생산하는 정보원·미디어·리뷰어·큐레이터·크리에이터를 발견하기 위한 Query입니다.
  > 
  > 시계, 오디오, 자동차, 프리미엄 가전, 고관여 소비재 등에서 제품을 단순 구매대상이 아니라 성능·품질·완성도·내구성·브랜드·소유경험을 종합적으로 평가하는 콘텐츠를 포함합니다. 제품 간 비교, 장기 사용, 구매 고민, 업그레이드, 프리미엄 가격의 정당화 또는 비판도 포함합니다.
  > 
  > 단순히 가격이 비싸다는 이유만으로 포함하지 않습니다. 할인정보만 존재하는 콘텐츠, 명품 로고나 사치 소비만을 보여주고 제품 품질·경험·관여가 드러나지 않는 콘텐츠, 금융투자·자산가격 중심 콘텐츠는 제외합니다.
  > 
  > Braun, NEVO, Philips, Series 9, S9000, shaver, shaving, 면도기, 전기면도기 자체를 이 Query의 relevance basis로 사용하지 않습니다. 이러한 제품이 우연히 등장하더라도 Premium Consumption / High-Involvement Objects라는 독립적인 의미맥락이 존재할 때만 포함합니다.

## AD2 — `AD2_Design_Material_Object`
- type: Topic · platforms: Facebook · Instagram Post · Instagram Reels · X · YouTube Shorts · TikTok · backfill: 1 month · include/exclude accounts: — · exclude keywords: — · dump occurrences: 1
- keywords (20): 제품 디자인 · 산업 디자인 · 산업디자인 · 디자인 오브젝트 · 제품 미학 · 소재와 마감 · 제품 소재 · 제품 마감 · 제품 형태 · 디자인 리뷰 · product design · industrial design · design objects · product aesthetics · material and finish · product materials · product finish · product form · object design · design review
- definition:

  > 물리적 제품의 형태, 비례, 소재, 표면, 마감, 구조, 조작성, 제작 완성도와 오브젝트로서의 미감을 중요하게 평가하는 한국어 및 영어 공개 소셜 콘텐츠와 이를 반복적으로 생산하는 디자인 정보원·에디터·매체·리뷰어·큐레이터·크리에이터를 발견하기 위한 Query입니다.
  > 
  > 산업디자인, 제품디자인, 소재 선택, 표면처리, 금속·플라스틱·유리 등 물성, 조립 완성도, 촉감, 형태, 디테일, 제품 오브젝트성, 디자인 품질에 대한 실제 제품맥락의 관찰·리뷰·비교를 포함합니다.
  > 
  > 그래픽디자인 튜토리얼, UI/UX만을 다루는 콘텐츠, 디자인 채용·포트폴리오 홍보, 순수미술 일반론처럼 물리적 제품과 연결되지 않는 일반 미학 콘텐츠는 제외합니다.
  > 
  > Braun, NEVO, Philips, Series 9, S9000, shaver, shaving, 면도기, 전기면도기 자체를 relevance seed로 사용하지 않습니다. 면도제품이 등장하더라도 독립적인 Design / Material / Object 관여가 확인되는 경우만 포함합니다.

## AD3 — `AD3_ConsumerTech_EarlyAdoption`
- type: Topic · platforms: Facebook · Instagram Post · Instagram Reels · X · YouTube Shorts · TikTok · backfill: 1 month · include/exclude accounts: — · exclude keywords: — · dump occurrences: 2
- keywords (20): 테크 리뷰 · 신제품 리뷰 · 소비자 기술 · 스마트 기기 · 스마트 디바이스 · 얼리어답터 · 신기술 제품 · 프리미엄 기기 · EDC · 전자기기 리뷰 · tech review · new product review · consumer tech · smart devices · smart gadgets · early adopter · new gadgets · premium gadgets · everyday carry · consumer electronics
- definition:

  > 일반 소비자가 실제로 구매·사용하는 새로운 기술제품, 스마트기기, 전자기기, 고급 기능, 신제품과 초기 수용 경험을 다루는 한국어 및 영어 공개 소셜 콘텐츠와 이를 반복적으로 생산하는 테크 매체·리뷰어·전문가·얼리어답터·크리에이터를 발견하기 위한 Query입니다.
  > 
  > 스마트기기, 소비자 전자제품, 신제품 리뷰, 제품 비교, 실제 사용성, 새로운 기능, 센서·자동화·적응 기능, EDC와 휴대기기, 초기구매 경험, 업그레이드 판단을 포함합니다.
  > 
  > B2B 기술, 기업용 SaaS, 개발자 인프라, 주식·투자 관점의 기술뉴스, 일반적인 AI/반도체 산업뉴스처럼 소비자 제품의 실제 선택·사용과 연결되지 않는 콘텐츠는 제외합니다.
  > 
  > Braun, NEVO, Philips, Series 9, S9000, shaver, shaving, 면도기, 전기면도기 자체는 relevance seed로 사용하지 않습니다. 제품군과 무관하게 Consumer Tech / Early Adoption 정보환경을 독립적으로 발견하는 것이 목적입니다.

## AD4 — `D4_MensStyle_Grooming_SelfCare`
- type: Topic · platforms: Facebook · Instagram Post · Instagram Reels · X · YouTube Shorts · TikTok · backfill: 1 month · include/exclude accounts: — · exclude keywords: — · dump occurrences: 1
- keywords (20): 남성 패션 · 남성 스타일 · 남성 스킨케어 · 남성 헤어 · 남성 향수 · 자기관리 · 퍼스널 스타일 · 남성 뷰티 · 셀프케어 · 그루밍 라이프스타일 · menswear · mens style · mens skincare · hair care · mens fragrance · personal style · self-care · grooming lifestyle · beauty routine · wellness routine
- definition:

  > 남성 패션, 스킨케어, 헤어 및 향수 등을 아우르며 외모와 웰빙을 가꾸는 남성 그루밍 및 자기관리 라이프스타일 전반을 의미한다.

## AD5 — `AD5_Routine_Mobility_EverydayOptimization`
- type: Topic · platforms: Facebook · Instagram Post · Instagram Reels · X · YouTube Shorts · TikTok · backfill: 1 month · include/exclude accounts: — · exclude keywords: — · dump occurrences: 1
- keywords (20): 모닝 루틴 · 루틴 최적화 · 시간 절약 · 관리 편의 · 관리 부담 감소 · 일상 효율 · 자동화 · 휴대성 · 출장 준비 · 여행 루틴 · morning routine · streamlined routine · time saving · low maintenance · automation · everyday carry · travel convenience · reliable routine · reduce steps · effortless upkeep
- definition:

  > 반복적인 일상 행동에서 시간, 단계 수, 준비 부담, 유지관리 부담, 휴대·이동 부담과 인지적 부담을 줄이고 일관된 루틴을 만드는 데 관심을 보이는 한국어 및 영어 공개 소셜 콘텐츠와 이를 반복적으로 생산하는 정보원·리뷰어·라이프스타일 크리에이터를 발견하기 위한 Query입니다.
  > 
  > 모닝루틴, 반복사용, 시간절약, low-maintenance 제품과 서비스, 자동화, everyday carry, 출장·여행의 휴대성과 편의, 단계 감소, 관리부담 감소, 안정적인 반복루틴, effortless upkeep을 포함합니다.
  > 
  > 기업 생산성, 업무관리 SaaS, 프로젝트 관리, 공부법처럼 생활제품·개인 일상과 연결되지 않는 generic productivity 콘텐츠는 제외합니다. 단순히 ‘효율’이라는 단어가 등장하는 것만으로 포함하지 않고 실제 생활루틴 최적화 맥락을 요구합니다.
  > 
  > Braun, NEVO, Philips, Series 9, S9000, shaver, shaving, 면도, 면도기, 전기면도기 자체를 relevance basis로 사용하지 않습니다. 면도시간 단축만으로 이 affinity domain을 정의하지 않습니다.
