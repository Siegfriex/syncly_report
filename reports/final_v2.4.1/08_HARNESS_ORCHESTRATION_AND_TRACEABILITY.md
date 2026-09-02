# 08 · 하네스 오케스트레이션과 추적성 — 이것은 'AI 여러 명'이 아니다
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 1. 역할과 경계
| Lane | 역할 | 할 수 있는 것 | 할 수 없는 것 |
|---|---|---|---|
| **A** Principal Analyst | 가설 사다리 수락, 발표 claim strength, 결정 클래스 | sealed evidence만 보고 판정; delta review | 새 분석·새 RQ·threshold 변경 |
| **B** Syncly Interaction → Frozen-data lineage | v2.3: Hey/MCP read-only 발굴(41콜, 48 evidence rows) · recovery: 행 단위 데이터 계보(P03/NEVO/REF), actor 감사, alias 감사, 원문 물질화 | 서버 측 의미 검색, raw 보존 | 쿼리 생성/수정, 결과 수를 prevalence로, 통계 해석 |
| **C** Assurance / Control plane | 사전등록 동결, 티켓 라우팅, provenance·게이트, 독립 재계산, B/D 수렴 판정, 단독 writer | 모든 canonical state | 남의 결과를 '좋게' 해석, 연구 방향 결정 |
| **D** Local Data Science | mart, entity, dedup, 코드북 적용, 통계, 반례 생산 · recovery: 측정 파이프라인 감사, 표적 재계산 | Tier A 기반 측정 | MCP, gold 평정, threshold 변경 |
| **E** Desk Evidence | 공식 카피·스펙·가격·캠페인·에디토리얼 독립 수집(36 units, 20 price rows) | OFFICIAL_INTENT 코딩 | Syncly, 소셜 결과 열람, 소비자 수용 주장 |

## 2. 왜 이 구조인가 — parallel independent analysis + adversarial validation + central arbitration
- **병렬 독립:** B와 D는 같은 176행(P03)의 계보를 서로의 결과를 보지 않고 재구성했다(B는 자체 detector 재구현, D는 사전등록 규칙). Stage별 rowset sha를 C가 대조했다.
- **적대적 검증:** D의 임무는 A의 스토리를 증명하는 것이 아니라 깨는 것이었다(L2 반례, CH6 구성개념 감사). B는 자기 Loop-1 actor 라벨이 틀렸음을 스스로 재실행으로 확인했고(28/40 mart 정답), 자기 모니터가 D 수치를 먼저 노출한 독립성 누출을 자진 신고했다.
- **중앙 조정:** C는 3행 divergence를 규칙(spec regex)으로 판정하고, PF-R5(HIGH) 주장을 13/13 분해로 반박했으며, 산술 재현(11/11)과 실행 완결성(WP 6F/2P/1S)을 분리해 기록했다.
- **Human:** 권위 문서 비준, 세션 시작, gold 최종 평정, 발표 문장 비준(CORR-V24-SLIDE2)만 맡는다.

## 3. 타임라인 (UTC, 2026-09-02)
11:04 v2.3 RUN_START → 11:22 B/D/E release → 11:28–12:25 B MCP Loop 1(41콜) · 11:45–12:19 D Loop 1 · 11:46 E → 12:25 Human v2.4 override(발표 우선, Syncly CLOSED) → 12:26–12:36 D-V24-001 → 12:41 C 검증·LOCAL PAGE SEAL → 12:56 A 해석 → 13:05 FINAL SEAL → ~13:15 Human recovery override(seal 보류) → 13:19 B/D recovery 티켓 → 13:22/13:34 CP1 → 13:31 R1(3행) → 13:40/13:55 CP2 → 13:52 D-V24R-002 표적 재계산 → 13:59 A delta → 14:02 RECOVERY SEALED.
운영 교훈: v2.3 Loop 1 동안 C는 watchdog 없이 턴을 종료해 B의 57분 실행을 감시하지 못했다. recovery에서는 Monitor(90초 폴링) + 7/12/15분 정책으로 교정했다.

## 4. 추적 체인 (예: Slide 1 두 번째 beat)
Business claim "디자인·프리미엄 어휘가 조금 더 자주" → Claim ID **C3 (local: DIRECTIONAL_NON_SIGNIFICANT)** → Statistical result 21/41 vs 18/68, h=.514, p_BH=.054 → Analytical table `claude-d v24_recovery/D_V24R_002_RECOMPUTE.json` → Codebook `claude-d v24/specs/CODEBOOK_CH_PMO_PG_N_v2.4.md` (CB_v2.4.0, commit 9d504e9) → Source rows `TIER_A_LABELS_v2.4_RECOMPUTED.csv` (post_id, CH6, grp) → Artifact sha `5bc7862b…` → Agent ticket `D-V24R-002_TARGETED_RECOMPUTE` (claude-d 1ca0481) → C verification (recompute in `control/v24_recovery/DECISION_LOG.md` 13:58Z) → Dataset `posts_cutoff.jsonl` sha `f8d130c2…1594`.
같은 체인이 모든 headline에 대해 `09_SOURCE_AND_CLAIM_LEDGER.md`에 있다.

## 5. 산출물 위치 (절대경로 기준 root `/home/sieg/projects-wsl/syncly_demo/.agent_worktrees/`)
- C: `C_assurance/control/v24/` (LOCAL_PAGE_SEAL, VERIFICATION_D/A, CLAIM/ROBUSTNESS ledgers, B_EVIDENCE_MARKUP, final/), `C_assurance/control/v24_recovery/` (RUN_STATE, CHECKPOINT/COVERAGE/DIVERGENCE/ROOT_CAUSE/REMEDIATION ledgers, L_DISPOSITIONS_REISSUED, RECOVERY_SEAL, final_report/)
- D: `D_research/v24/` (specs, results, gold, viz), `D_research/v24_recovery/` (lineage, audits, recompute)
- B: `B_production/runs/v2.3_20260902/B/` (Hey/MCP), `B_production/runs/v24_recovery/B/` (lineage, actor, alias, materialized)
- E: `E_desk/runs/v2.3_20260902/E/` · A: `A_authority/harness/handoff/` · BUS: `BUS_ledger/harness/ledger/LEDGER.md` (+ tickets/, recovery/, final/)
