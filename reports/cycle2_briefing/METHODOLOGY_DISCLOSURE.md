# METHODOLOGY DISCLOSURE — RUN-20260903-V25-AD-SIGNAL-ALIGNMENT-001 (C, 2026-09-03T00:19:00Z)

## METH-01 — Implementation independence
독립 구현 복제 검증은 성립하지 않았으며, blind result audit와 C의 독립 수치 재계산으로 대체하였다.

Facts: C wrote the reference coder (qa/c_coder/c_adsig_coder.py) for cross-checking; at CP1 rev 2 lane D imported that module verbatim (D-ADSIG-001 CP1R2, D cfee77e) instead of keeping its own implementation. From that point the two marts cannot diverge by construction, so "two independent pipelines agree" is not a valid claim. What stands instead: (a) two C blind 40-unit label audits against the frozen codebook (audit-3 content PASS_WITH_NOTES: every D claim positive a genuine lexicon instance; tier rule 0 violations); (b) C's independent numeric recomputation of every matrix cell (398/398 identical) and of both BH families (K2 11/11; K1 10/11 + one boundary case); (c) C ownership of the reference code with its sha in the ledger. The report must not use the words "independent pipeline" for this run.

## METH-02 — Pre-registration amendments (status: POST-DATA / PRE-VERDICT AMENDMENT)
| id | timestamp | old sha | new sha | changed field | reason | outcome values inspected before amendment? | verdict assigned before amendment? |
|---|---|---|---|---|---|---|---|
| AM-1 | 2026-09-02T23:30:08Z | bc841bacb99826ea… | c1f261e1d35a96f2… | N-2 state→Q4 list mapping | §N-2: alignment state → Q4 list mapping had no rule in the prereg; fixed before any X02 value could exist | NO — no matrix, share or verdict existed at that time (D-ADSIG-002 not yet released) | NO — no verdict has been assigned in this run |
| AM-2 | 2026-09-02T23:43:56Z | e405a1ce77218b5c… | 6ab6b652e9df1fa9… | lexicon v1.1 currency regex fix (3 patterns) | three MR-PROMOTION currency regexes were dead (\\b before $/€/£ never matches after a space) — repaired to a lookbehind; no token added/removed | NO — no matrix, share or verdict existed at that time (D-ADSIG-002 not yet released) | NO — no verdict has been assigned in this run |

Both amendments were made after the post mart existed (data seen at row-count/missingness level only) and before any share, matrix, test or verdict existed. They are logged in RUN_STATE.AD0_FREEZE.amendments and TICKET_LEDGER (AD0-AMEND-1/2). Post-hoc rule: no further amendment after D-ADSIG-002 (first outcome table, 2026-09-02T23:53Z); any later change requires a new run id.

## Sequencing note (v2.5 comparator lane)
D-V25-004 Stage 2 statistics were computed before the label audit closed (C decision to parallelise); the audit then failed and Stage 2 was superseded (D-V25-005/006). Disclosed in control/v25_comparator_universe/DECISION_LOG.md.

## Conclusion-strength vocabulary (binding for all current-run text)
Allowed: HIGH · MEDIUM · DIRECTIONAL · INSUFFICIENT · NOT_MEASURED. Where a code carries a recorded lexicon gap (AS-06, AS-W2, AS-W3, MR-PROMOTION, MR-CONVENIENCE) or a THIN grounding flag, a low/zero supply is written as **NOT_MEASURED** (no evaluable evidence) or **LOW_OBSERVED_WITH_COVERAGE_CAVEAT** (evaluable but lexicon-limited) — never "광고에 없다" / "absent from advertising". Applies to H9 and every T-test reading.
