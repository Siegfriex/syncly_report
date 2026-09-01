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

## 프로세스 기록
- 야간 세션에서 10건의 정정이 모두 downstream 소비 전 포착 (correction rate ~9%, GREEN).
- 재현성 패스: zero drift.
- 검증 분류 체계: IMPLEMENTATION-VERIFIED(독립 재구현) vs CONSTRUCT-CHECKED(도구 결함 공유 가능) 구분 운용; lexicon 측정은 negative-control 게이트 의무.

상세 근거(포스트/계정 식별자 포함)는 비공개 운영 repo의 C 감사 기록에 있음 — 본 public repo에는 집계 수치만 기재.
