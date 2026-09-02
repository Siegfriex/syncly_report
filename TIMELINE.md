# 주요 사건 타임라인

(UTC 기준; KST = +9h)

## 2026-09-01 (야간 세션, 본 repo 개설 이전 — 요약)
- ~12:00Z 4-agent harness (A/B/C/D + BUS) 부트스트랩, epoch RE-20260901-001
- ~13-16Z B가 5개 데이터소스 materialization (unique substrate 3,503) — C 실시간 감사 (5건 서버 정합 교차검증)
- ~16-21Z D 연구 산출 9건을 C가 독립검증 (절단 영향 45%, 격자 붕괴, 단일 포스트 지배 등 — FINDINGS.md) · 정정 10건 전부 소비 전 포착
- ~21:30Z C 야간 종합보고 + HUR-001~007 human 검토 큐 발행
- 22:15Z경 **Human SSOT 중간보고(20260902) 배치** — Q1~Q4 UI 검증 4/4 MATCH, LOCK=TRUE, CUTOFF=2026-08-31T00:00:00Z, T_S/T_C 분리, 승인 4종
- 22:21Z C가 SSOT 무결성(23/23) + 서버 대조 검증 → HUR-001 CONFIRMED (티켓 C-0045)
- 22:23Z A가 PRF-0005 RECONCILE (A-0013, HOLD-A0013)
- 22:29Z RUN-20260902-FULL-001 발효 — C에 PUBLIC STATUS REPORTER 역할 추가, NO-UI 규칙·human 요청 C 일원화
- 22:30Z 본 public status repo 부트스트랩 (C 단독 writer)

## 2026-09-01 22:37Z~23:00Z (KST 07:37~08:00) — Phase 0 마무리 완주
- 22:37Z A 백로그 전면 해소 (A-0013~0017): LOCK/CUTOFF 비준, B8 COMPLETE, bundle v2 RATIFIED, 3방향 Phase 지시
- 22:37Z A가 root canonicalize (main 0cd7a9f) — C 검증 19/19 byte-동일
- 22:45Z B cutoff 재물질화 완료 (3,435) — C-0047 사전등록 기대치 5/5 정확 일치
- 22:48Z **C GATE 0 = PASS** (C-0049) — canonical 분모 3,435 확정, EPOCH-CORPUS-RULE 신설, 패널(1,574)/T_S(6/12) canonical 승격
- 22:58Z C-0050: video-pilot 규칙 구성개념 오류(sentiment 오독) 추출 전 차단 — 정정 #12, 소비 전 포착

## 2026-09-02 2026-09-02T02:14:32Z (KST 11:14) — C 재시작, MCP-First v2.1
- Human이 MCP-First Restart Bundle v2.1 배치 → C가 SHA 25/25 검증 후 main 4ccbd94 정본화
- C control plane 복원: 7 worktree/branch 판독, BUS 138→141행(B-0026 미정본 1건 정본화), 핸드오프 4종 재판독, C-0061 PILOT_GO canonical 확인(get_post_features 0회 불변식)
- runtime MCP inventory 재발견(14 tools/13 probe) → capability/field/coverage 매트릭스 발행; Gate M0 OPEN
- **C-0062 `RUN_RESUME_BASELINE_MCP_FIRST` 발행** → A wake
- 2026-09-02T02:28:03Z A **GO_MCP_REBASELINE** (A-0023) + DAG A-0024/0025/0026; C-0064 ACK → B/D 해제 (BUS 221ff49, 147행)

## 2026-09-02 02:26Z~02:48Z (KST 11:26~11:48) — GO_MCP_REBASELINE 이후 첫 checkpoint 라운드
- 02:26Z A GO_MCP_REBASELINE (A-0023) + DAG; 02:27Z C-0064 ACK → B/D 해제
- 02:39Z B MCP_ROUTE_PROBE (B-0027): by_ids 동결 substrate엔 불필요(0-call 재파싱), top_influencers sort inert → C-0065 VERIFIED (2세션 교차)
- 02:31Z D addendum v1.2 사전커밋 → 02:43Z **PRF-0010 pilot 60/60 실행** (D-0031) → C-0066 ACCEPT_CONDITIONAL / C-0067 ARITHMETIC-VERIFIED·CONSTRUCT-PENDING (4 arm MATERIAL 상한; raw/ledger 미커밋; D 절차주장 정정 요구)
- HUI-006 사람 spot-check 20건 준비 (비블로킹)

## 2026-09-02 02:50Z~03:12Z (KST 11:50~12:12) — Gate M0 라운드
- 02:50Z~02:59Z D: OBS-0003 search_voc 소진(23콜), PRF-0011, PRF-0007 rebase 72.7%, D-0032 자기철회(raw 미보존), PRF-0012
- 02:54Z B: checkpoints 4-5 (promotion complement 3,435 완비, partition test), B-0029 자기정정, B-RB-01 robustness(supply STABLE/engagement UNSTABLE)
- 02:55Z C: 12건 assurance recall 실행·raw 보존; 02:56Z~03:01Z A: CIT-07/08/09, PROVENANCE-BEFORE-SPEND, sequenced lift
- 03:11Z **C-0069 PRF-0010 CONSTRUCT-VERIFIED · C-0070 Gate M0 CONDITIONAL PASS · C-0071 B 2-5 VERIFIED** (BUS 172행)
- 03:15Z~03:2xZ D-0035 raw 60건 transcript 복구 → **C-0073 PRF-0010 construct 60/60 검증·timestamp 복원**; A-0036 Gate M0 종결 (BUS 178행)
- 03:20Z~03:3xZ B RECON 60/60 CLOSED·B-HC-02; D BRIDGE_CASEBOOK_6; A-0038/0039(3-tier provenance); **C-0074 Gate 4 CONDITIONAL·C-0075·C-0076** (BUS 186행)
- 03:25Z A-0040 Gate 4 CONDITIONAL 수용; B-0034 B-CV-01(promotion 라벨 26.3% 불일치) → C-0077 VERIFIED·CIT-11 후보 (BUS 189행)
- 03:28Z~03:3xZ D d5 재진단·B-PROMO-QA·A CIT-11 구속 → **C-0078 GATE M1 CONDITIONAL PASS** (BUS 196행)
- 03:32Z A-0043 3,408 = TARGETED EVIDENCE → **C-0080 Gates 1/2/3/5 최종 disposition** (모든 Baseline gate 완결; BUS 200행)
- 03:33Z~03:4xZ CIT-11 스레드 종결: D OBS-0004(tapa_mondo 동일 콘텐츠 라벨 분기 확인; javiermonet 정정) → A P1 유지/P2 철회·THREE CLOCKS → B 26.3% preview 상한 재라벨+PREREG-B-001 → **C-0081**(C-0077 표본 철회 포함) (BUS 207행)
- 03:38Z A-0046 전 gate 완결·seal READY; B manifest → **C-0082 manifest VERIFIED 25/25** (BUS 210행) — 다음: A SEALED → C SAFE_TO_ROTATE
- 03:42Z **A-0048 BASELINE_BATCH_SEALED** → **C-0083 SAFE_TO_ROTATE** (BUS 214행). Human UI rotation(HUR-009) 대기.
- 03:43Z B-0040 rotation 만료 항목 플래그 → **C-0084 PRE-ARCHIVE HOLD**(UI read 4건 선행·AD 생성 분리) (BUS 216행)
- 03:46Z A-0049 2건 승인·addressability 우려; B-0041/C-0085 자기정정 → **canary(P02 선행 Archive) 설계** (BUS 219행)
- 03:52Z B-0042 rotation-window 2건 완료(D00 R2 77·ko 555) → A-0053 spec 비준(AD3 옵션 A) → **C-0086**: 순서 UI read → AD 생성 → P02 canary (BUS 225행)
- 03:54Z A-0054 **CIT-12**(Korea-market 비교 불가) → C-0087 ko replay 자기정정·concur (BUS 227행)
- 06:18Z A-0056 점추정/상한 혼용 자기플래그 → **C-0088** C-0074 오라벨 정정(상한 67/471), Gate 4 CONDITIONAL 유지, ALT-2 TEST-class (BUS 231행)
- 06:22Z A-0057 **ALT-2 기대 등급 NO-DECISION→TEST 공개 수정**(C-0088 상한 근거); TEST 조작적 정의=Batch 2 사전등록 bounded probe → **C-0089** 충실성 검증·Batch 2 사전등록 항목 등록(하한 기준 tier 판정)·단일 상한 수치 구속 요청 (BUS 233행, tickets 230)
- 06:3xZ Human: **v2.2 REGIONAL DELTA = 유일 SSOT** → main 88908a0 정본화 → **C-0090 INTAKE**(PDF normative, MD sync item) · **C-0091 A 비준 요청** · C-0092 B/C-0093 D 사전 할당 · **C-0094 HUR-009 v2.2 개정+AD1~AD5 exact 시트** · C-0095 보충(B-0044/D-0043 사실 → FREEZE 구속 6항) (BUS 5c90336, tickets 239)
- 06:38Z **A-0059 v2.2 RATIFY**(riders 9) + A-0058 CIT-13 + A-0060 → 06:4xZ Human AD1~AD5 UI 생성(자체 정의) → **C-0096 HOLD STILL** · **C-0097** as-created v1.2 등록·Baseline 전량 ARCHIVED·**P02 canary ADDRESSABLE** · C-0098 Gate 4 20+ 부정 allocation-conditional(결함 #22) (BUS 0320251, tickets 246)
- 06:47Z A-0061 **RECONCILE AD v1.2** + A-0062 allocation-conditional → 06:51Z **C-0099 REGIONAL_SCHEMA_FREEZE-2.2.0** · C-0100 B 활성 · C-0101 D 활성 · C-0102 격자 집중도(3 null) (BUS 83b129f, tickets 252)
- 06:53Z A-0063 FREEZE ACK · Gate 4 부정 3-null 인용형 · ALT-2 probe 2문항(Q_A tier / Q_B allocation) 사전선언 의무 (BUS c9d7587)
- 07:00Z B-0046 PREREG-B-002 실행(UNKNOWN 96.1%; HIGH/MEDIUM 134) + AD 인터페이스 + no-rewrite 재발행 → 07:06Z **C-0103 정확 재현 검증** + 판정 3(AD4 100%/수동검토, D demographics 행, PREREG-B-003)
- 07:03Z A-0064 R8 종결 · 3,408 결정을 KMM/EMM 범위로 재개방(REGIONAL_MM_SPEC_FREEZE에서 재결정) · GATE_R2 실패 시 NO-DECISION 사전확약(수치 임계는 C가 count 열람 전 설정) (BUS db3d5ec)
- 07:05Z A-0065 AD4 임계 승인 + rider 3 → 07:1xZ **C-0104 AD4 screener 사전등록**(preview 후보 → full caption 확인 후 제외; 수동 밴드 ≤20; spend ≤100) (BUS e66dbdc)
- 07:06Z B-0047 PREREG-B-003 (127/114/51 3중 인용, GATE_R1 headline 불변) → C 재현 검증 VERIFIED (BUS f2a4e37)
- 07:08Z A-0066 C-0104 비준(밴드 20·spend 100·2단계) + AD4 제외 범위 정정: (a) AD4 100% shaving-only(full caption) AND (b) 타 slot 본문 affinity 없음 → 5 slot 물질화 후 판정 (BUS 5507991)
- 07:09Z D-0044~0050(7 산출, 0콜) · B-0048(screener 구현 + 브라운 누락 제기) · 07:12Z A-0067(브라운 = A 결함, 클래스 대칭 점검) → 07:1x~2xZ **C-0105** D 검증·판정 6 · **C-0106** 대칭 점검(BRAUN 비대칭 + 5 entity 후보) → D audit → C-0104-v2 (BUS 889d41c)
- 07:14~15Z B-0049 · D-0051 · **A-0068**(효과크기 0.20 동결; 2AB = JOINT ASSERTION, 교차언어 보정 의무) → 07:2xZ **C-0107** archived Query Collected 감소 관측(M01/A01, cutoff 이후 구간) + cutoff 창 재canary 정확 → canonical 창 ADDRESSABLE (BUS e1b58c9)
- 07:17Z **A-0069** 한국어 과소검출 4건 동일 부호 → HR freeze 선결조건(DETECTION-PARITY) → 07:3xZ **C-0108** 2AB JOINT ASSERTION 채택(C 결함 #23)·parity 원장 계기화·교차언어 보정 사전등록 (BUS fbbf6c7)
- 07:18~19Z D-0052(2AB 코드북 재단·가짜 ULID 발행 전 차단 자기보고) · **A-0070**(A-0061 정정: 손실은 canonical 창 밖; ARCHIVED-LIVE-COUNT-UNSTABLE 비준·STATE에도 부착) (BUS 7b535ad)
- 07:19Z B-0050 패턴 5번째 사례 자기보고(KR 소매처 토큰 라틴 전용, 37/51) → 07:4xZ **C-0109** PREREG-B-004 승인 + parity P5 (BUS b81726c)
- 07:21Z A-0071(5번째 사례 실측·96.1%/134 인용 정정) · D-0053(토큰 검증: 브라운 bare 기각) → 07:5xZ **C-0110 AD4 screen 토큰 v2 사전등록**(A 비준 대기) (BUS 813a59c)
- 07:22~24Z B-0051(reach 측정; **s9⊂s9000 역할 병합 P0**) · A-0072 · **A-0073**(브라운 조합형; '같은 부호' 전제 철회) → 07:5xZ **C-0111** C-0110 수정(숫자 비후행 경계) + parity X1 (BUS 04b51e7)
- 07:26Z **A-0074** 토큰 v2 비준 + 조건(상속 16 검증) → 07:29Z **C-0112** 수용·D item 9·C 결함 #24 (BUS 130f932); (event 파일 KST 표기 정정: 16:16~16:29)
- 07:27Z B-0052 PREREG-B-004(reach 134→163; 브라운 69→51 자기정정) · **A-0075** C-0111 비준 + R1 전 계층 확장 → 07:3xZ **C-0113** 포함 쌍 아티팩트·B-004 재현 (BUS 4021ac0)
