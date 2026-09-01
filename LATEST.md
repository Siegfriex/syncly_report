# Syncly 연구 현황 — LATEST

갱신: 2026-09-01T23:51Z (KST 2026-09-02 08:51) — 세션 종료 시점 · Epoch `RE-20260901-001` · Run `RUN-20260902-FULL-001` · 작성: Claude C (단독 writer)

## 한 줄 현황 (세션 종료 시점)
**Gate 0 PASS · 분모 3,435 확정 · 발견 10/10 VERIFIED · PILOT_GO 발행.** C/A 세션은 핸드오프를 남기고 정상 종료, B/D는 사전승인 하 계속. 상세는 reports/30min/20260902/0900_session_close.md.

### (이하는 07:30 시점 스냅샷)
Phase 0 마무리 단계 — Human의 SSOT 중간보고(20260902)로 **QUERY_SOURCE_LOCK=TRUE**와 **ANALYSIS_CUTOFF=2026-08-31T00:00:00Z**가 확정되었고, B의 cutoff 재물질화와 C의 Gate 0 독립검증만 남았다. 이후 Phase 1(소스 패널·T_S/T_C·full-details·video pilot) 진입.

## 방금 일어난 일
- Human이 Q1~Q4 쿼리 설정을 UI에서 직접 검증 — 4/4 원명세 일치(MATCH). C가 서버측 대조로 정확 일치 확인 → HUR-001 CONFIRMED.
- 측정모형 개편: 단일 T 폐기 → **T_S**(소스 기반 카테고리 진입)와 **T_C**(콘텐츠 기반 타깃 친화)로 분리. A01은 post corpus에서 **계정 패널(A_SOURCE_PANEL)**로 전환.
- 승인: 절단 caption 복구용 full-details 조회(~857건), promotion/language 열거, 60건 비디오 특징 파일럿.
- A가 PRF-0005(비교 격자 희소성)에 RECONCILE 판정 — Phase 2 정량 제품비교 클레임은 Gate 4 재평가(파일럿 이후)까지 보류.

## 다음 단계
1. A: LOCK/CUTOFF 비준 티켓 + B/C/D 작업 티켓 발행
2. B: cutoff 기준 재물질화 + 정확한 데이터 해시 공표
3. C: Gate 0 독립검증(카운트·해시·소스 튜플·쿼리 멤버십·무drift)
4. Phase 1 착수 (소스 패널 → T_S census → full-details → T_C → video pilot → Gate 1~5 재평가)

## 열린 인간 확인 항목 (연구 전체는 계속 진행)
HUMAN_ACTIONS.md 참조 — 소스 패널 육안 검토(HUI-002~004), 바이럴 outlier 적합성(HUI-005), 비디오 파일럿 spot-check(HUI-006), promotion/language 표본 검증(HUI-007/008), views 부재 판별(HUR-007).

## 핵심 수치 (야간 동결 기준)
| 코퍼스 | 동결 | 라이브 UI(9/2) |
|---|---|---|
| A01 (프리미엄 타깃 소스) | 1,849 | 1,892 |
| M01 (면도 카테고리 분모) | 1,271 | 1,292 |
| P02 (Philips S9000) | 64 | 69 |
| P03 (Braun Series 9) | 179 | 186 |

라이브 증가는 쿼리 변형이 아니라 수집 성장 — cutoff 동결의 근거.
