# 07 · 다음 validation은 무엇이어야 하나
> **Braun NEVO × Syncly** — Social Intelligence → Product Positioning → Message Strategy
> Author: Claude C (single writer, harness control plane) · Date: 2026-09-02 · Run: `RUN-20260902-V24-RECOVERY-001` (prior `RUN-20260902-V24-LOCAL-001`, `RUN-20260902-V23-001` = lineage) · Authority: business `PRESENTATION_FIRST_NEVO_V2.4` (main 8e8c74d) · method `MCP_FIRST_DPDD_v2.3` hypothesis-loop harness · Dataset: frozen 3,435 posts, sha256 `f8d130c217a570cccd295c35a21ad16a0f6ccae275c1c80a4cb9f5cad1153594`, cutoff 2026-08-31T00:00:00Z · Tier A(verbatim) 182 (5.3%)

## 원칙
이번 Run의 병목은 분석이 아니라 **텍스트 취득 설계**였다(전문 182건, 전부 M01 회원, 제품별 층화 없음). 따라서 다음 단계의 우선순위는 모델을 바꾸는 것이 아니라 분모를 채우는 것이다. 모든 항목은 신규 취득을 요구하며(현재 Syncly CLOSED), 사전등록된 코드북·문턱은 그대로 둔다.

| # | 항목 | 왜(어느 NO_DECISION을 푸는가) | 최소 설계 | 성공 기준 |
|---|---|---|---|---|
| 1 | **제품별 층화 verbatim 텍스트 취득** | R2 근본 원인; S9 Tier A 3 → L3/L5; NEVO Tier A 41/225 | NEVO·Series 9 각각 entity-detected 게시물에서 전문 회수(read-only details), 유료/비유료·Brand/외부·플랫폼 층화; 목표 셀당 ≥20 | Series 9 Tier A ≥ 50, Brand 저작 NEVO ≥ 10, 비유료 NEVO ≥ 20 |
| 2 | NEVO 음차 lexicon (내비/내보 등) | entity 재현율; 01M1EQR7Z9…류 재분류 | ENTITY_DET v2.5에 한국어 음차 변형 추가, 회귀 테스트 확장; CJK 인접 Latin `\b` 규칙(prefix `\b` + suffix `(?![a-z0-9])`) | 회귀 PASS, FN 후보 0 |
| 3 | 사람 gold 라벨링 | gold 0 → 모든 CH/PG가 CONDITIONAL; CH6 구성개념 경계 | 기존 frame(182행, 35 strata)에서 층화 최소 100; Human 최종, A blind 2차; D 배제 | κ ≥ .75; CH6 loose/tight 경계 판정 |
| 4 | 비유료·비Brand NEVO 텍스트 | robustness rung 5; L4 product/usage 분모(6) | 1과 병행, ORGANIC/SUSPECTED 우선 | N1 ≥ 20 |
| 5 | Brand 저작 NEVO 전문 | L5 β3 유일 blocker | braun_korea/us/global 게시물 7건 + 추가 | Brand cell ≥ 10 |
| 6 | 리뷰어 검증 질문(외부 취득) | RQ2 독립 외부 증거(Hey N2a=0) | "Series 9 사용자라면 어디서 차이를 느끼는가 / 턱밑을 몇 번 지나가는가" 브리프 | independent external Tier A ≥ 20 |
| 7 | problem-ownership 코딩 확대 | L2 near-zero 재현 여부 | 1의 표본에 PMO 코딩 | PMO_COMPLETE 방향 재현 |
| 8 | US 동일일자 street price | 가격 overlay US 공백 | featured offer 존재 시 캡처 | 동일일자·동일 세제·동일 번들 |
| 9 | 소비자 VOC | reception NO-DECISION | 댓글/리뷰 취득 경로 확보 | attribute-level 평가 ≥ 50 |

## 게이트
1) 취득 전 사전등록 갱신(셀 크기·family·threshold 동일) 2) 취득 후 Gate V0 재조정(분모 확장은 새 epoch) 3) B/D 독립 lineage 재수렴 4) 그 뒤에만 L1–L5 재판정. GUARD-V24R-001은 S9 Tier A ≥ 20이 되기 전까지 유지된다.
