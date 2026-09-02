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
