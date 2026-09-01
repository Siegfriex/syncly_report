# Human 확인 큐

갱신: 2026-09-01T22:30Z · 원칙: human 응답 부재가 전체 run을 정지시키지 않음 — 각 항목에 blocks_scope 명시

## 완료
| ID | 내용 | 결과 |
|---|---|---|
| HUI-001 (=HUR-001) | Q1~Q4 쿼리 설정 UI 검증 | **DONE — 4/4 MATCH, C 서버 대조 정확 일치 → LOCK=TRUE 승격** |
| HUR-006 (부분) | Promotion/Language 필터 존재·의미론 | 부분 확인 (3분류 존재, 서비스 파생) — 표본 검증은 HUI-007/008로 승계 |

## 열림 (우선순위순)
| ID | 우선 | 내용 | blocks_scope (이것만 막힘) |
|---|---|---|---|
| HUR-007 | P0 | IG Post/Facebook의 views 부재가 상류 부재인지 MCP 미노출인지 UI 판별 | 해당 플랫폼 views 기반 클레임 문구 확정 |
| HUI-002 | P1 | A01 상위 20~50 소스 계정 육안 검토 (프리미엄 타깃 지향 생태 확인) | Core A 패널 확정 (패널 구축 자체는 진행 가능) |
| HUI-003 | P1 | M01 상위 20~50 소스 계정 특성화 | T_S 교집합 해석 확정 |
| HUI-004 | P1 | 공유 소스 6곳 + 매칭 포스트 전건 검토 | category-entry 사례 연구 확정 |
| HUI-005 | P1 | 3.7M 바이럴 outlier의 카테고리 적합성 판정 | Gate 2/5 최종 판정 (robust variants로 분석은 계속) |
| HUI-006 | P1 | 비디오 파일럿 ~60건 중 일부 human gold spot-check | 비디오 분석 확장 결정 |
| HUI-007 | P1 | Paid/Organic/Suspected 분류 표본 검증 | message salience vs consumer concern 구분 문구 |
| HUI-008 | P2 | Language 필터 KO 라벨 정밀도 수동 검증 | 한국 시장 headline 허용 범위 |
| HUR-004 | P2↓ | D00 UI 목록 건수 확인 — 서버측 상한 해소 확인됨, confirmatory | D00 증거 코퍼스 각주 |
| HUR-005 | P2 | YouTube 동명 handle 실채널 동일성 확인 | YT 소스 정체성 CONDITIONAL 해제 |

| HUR-008 | P1 | 12개 계정의 8월(01~31) 창 내 면도 카테고리 포스트 유무 + 각 PostID/URL (Dashboard Author 차원 또는 Quick Search; 진입 6곳은 양성 대조) | 저진입(0.38%) 인과 해석만 — 다른 작업 전부 계속 |

각 항목의 정확한 UI 경로·확인 대상·가설 A/B·다운스트림은 운영 repo의 HUR 티켓(16필드)에 기재 — 필요 시 C가 요청 시점에 제공.
