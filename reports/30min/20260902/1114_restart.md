# 재시작 보고 — 2026-09-02 11:14 KST (2026-09-02T02:14:32Z)

Epoch `RE-20260901-001` · Run `RUN-20260902-FULL-001` · **Method revision `MCP_FIRST_DPDD_v2.1`** · 작성: Claude C (단독 writer)

## 한 줄
**C control plane 복원 완료 → `RUN_RESUME_BASELINE_MCP_FIRST` 발행 (C-0062).** 세션은 종료됐었지만 Run은 종료되지 않음. 다음: A가 방법론 개정 비준 + `GO_MCP_REBASELINE` → B/D 착수 (D pilot은 즉시 가능).

## 무엇이 바뀌었나 (방법론)
- Human이 배치한 **MCP-First Restart Bundle v2.1**이 현재 권위 (SHA256SUMS 25/25; main 4ccbd94 정본화). 기존 Final(09-01)/Interim SSOT(09-02)는 legacy 계보.
- 판정: **SOURCE_CORPUS_INVALIDATION = FALSE**. 잘못된 것은 Query 모집단이 아니라 enrichment/preprocessing route.
- 폐기/강등: 203자 preview를 decision-grade text로 사용(→ INDEX_TEXT), get_post_details 전수(835) 호출을 기본 route로 사용(→ SUSPENDED_AS_DEFAULT), MCP tool family 소진 전 "Syncly limitation" 선언.
- 보존: Query lock, cutoff 2026-08-31, 분모 3,435, 소스 패널 1,574, T_S 6/12, 10/10 VERIFIED, Gate 0 PASS, video pilot v3 설계 + C-0061 GO.

## 복원 검증 (Git 판독)
| 항목 | 값 |
|---|---|
| root main | 4ccbd94 CLEAN |
| A / B / C / D | aeb1f6e / a46c878 / 0365f13 / a501738 (모두 origin 동기) |
| BUS | 55a6840 · ledger 141행 · tickets 173 (미정본 outbox 1건 B-0026 정본화) |
| C-0061 PILOT_GO | BUS canonical 확인 · get_post_features 실제 호출 **0** (D-0030 명시, C도 0 유지) |
| 서버 교차(cutoff 필터) | A01/P02/P03 EXACT · M01 +1(기지) · D00 261 vs 184 listable(기지) → Gate 0 substrate 오늘도 정합 |
| 신규 gate | **Gate M0 (MCP Capability Exhaustion) OPEN**, Gate M1 (Baseline Enrichment) NOT_STARTED |

## Runtime MCP inventory (C probe 13회, read-only)
14 tools 재발견(historical 14와 이름 일치). 판정: PRODUCTION_READY 10 · CONDITIONAL 2 (details targeted-only; top_influencers 정렬 이상) · EXPLORATORY_ONLY 1 (search_voc 단일 probe 공백 — **limitation 선언 아님**, D exhaustion 필요) · PENDING_PILOT 1 (get_post_features).
MATERIAL 관측: (1) video-feature 검색이 hit마다 분석기 전체 서술문을 반환 → per-post feature 호출 없이 시각 증거 route; (2) ID batch 조회(≤100)가 author/metrics/sentiment/다중 Query 소속을 반환 → 3,435 metadata ≈ 35 call; (3) 주간 시계열 정상(과거 오류 미재현); (4) 어떤 route도 per-post promotion 필드 없음.

## 청결/drift
- B worktree dirty 1 file(outbox id 정정 미커밋) — B fix-forward. legacy SSOT는 FINAL 폴더 하위에 중첩 배치(byte-동일, as-is). 번들은 이중 중첩 경로(as-is).
- report repo: 세션 종료~재시작 사이 34 commit의 event 파일 1:1 백로그 생성 완료 + 금일 3건.

## Human 큐
변경 없음(전부 비블로킹). **본 재시작이 Human에게 요청하는 UI 행동 없음.** Query 생성/수정 금지 유지.

## 다음 30분 예상
A: 비준 + GO_MCP_REBASELINE + ticket DAG. D: pilot 60-call 실행(EXPERIMENTAL) + semantic/video/VOC exhaustion 착수. B: MCP_ROUTE_PROBE(by_ids 100-batch 등). C: 라우팅·독립검증·Gate M0 입력 수집.
