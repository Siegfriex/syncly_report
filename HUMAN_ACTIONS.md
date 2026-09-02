# Human 확인 큐

갱신: 2026-09-02T03:57:40Z

## 완료
| ID | 내용 | 결과 |
|---|---|---|
| HUI-001 (=HUR-001) | Q1~Q4 쿼리 설정 UI 검증 | **DONE — 4/4 MATCH, C 서버 대조 정확 일치 → LOCK=TRUE 승격** |
| HUR-006 (부분) | Promotion/Language 필터 존재·의미론 | 부분 확인 (3분류 존재, 서비스 파생) — 표본 검증은 HUI-007/008로 승계 |

## 열림 (우선순위순)
| ID | 우선 | 내용 | blocks_scope (이것만 막힘) |
|---|---|---|---|
| **HUR-009** | **P0** | **UI_MUTATION_REQUIRED (C-0084 개정)** — **지금 순서**: ① HUR-007·HUR-008·HUI-005·HUI-007 UI 확인(Baseline Query 존재 중; 설정 변경 금지) → ② AD1~AD5를 (A-0053 비준·AD3=옵션 A) claude-c `control/rotation/AD_BATCH_QUERY_SPEC_SHEET_v1.md`대로 생성 (3) query_id·tracking_since·keyword 캡처 → C. (참고: UI가 6번째 이후 Query 생성을 거부하면 변경 없이 중단하고 C에 알려주세요 — 그 경우 P02 Archive→canary 후 생성으로 순서가 바뀝니다.) (4) **Archive는 단계적(C-0085)**: P02 하나만 먼저 Archive → C가 접근성 canary 검정 → 결과 통보 후 나머지 4개 Archive(또는 중단). Delete 금지, 스크린샷. 요청서 `control/human_review/HUR-009_baseline_rotation_ui_mutation.md` | Batch 1 수집 시작만 |

### 기존 열림
| ID | 우선 | 내용 | blocks_scope (이것만 막힘) |
|---|---|---|---|
| HUR-007 | P0 | IG Post/Facebook의 views 부재가 상류 부재인지 MCP 미노출인지 UI 판별 | 해당 플랫폼 views 기반 클레임 문구 확정 |
| HUI-002 | P1 | A01 상위 20~50 소스 계정 육안 검토 (프리미엄 타깃 지향 생태 확인) | Core A 패널 확정 (패널 구축 자체는 진행 가능) |
| HUI-003 | P1 | M01 상위 20~50 소스 계정 특성화 | T_S 교집합 해석 확정 |
| HUI-004 | P1 | 공유 소스 6곳 + 매칭 포스트 전건 검토 | category-entry 사례 연구 확정 |
| HUI-005 | P1 | 3.7M 바이럴 outlier의 카테고리 적합성 판정 | Gate 2/5 최종 판정 (robust variants로 분석은 계속) |
| HUI-006 | P1 | **준비 완료** — pilot 층1 V_POS 20건 gold spot-check (운영 repo claude-c control/human_review/HUI-006_video_pilot_gold_spotcheck_20260902.csv : URL 열고 영상에 면도 제품 엔티티가 보이는지/말하는지 Y/N + 무엇인지 기입). 불일치 >4/20 → PRF-0010 HOLD | PRF-0010의 EXPERIMENTAL 이상 승격·ALT-2 확대 판단만 — 나머지 전부 계속 |
| HUI-007 | P1 | Paid/Organic/Suspected 분류 표본 검증 | message salience vs consumer concern 구분 문구 |
| HUI-008 | P2 | Language 필터 KO 라벨 정밀도 수동 검증 | 한국 시장 headline 허용 범위 |
| HUR-004 | P2↓ | D00 UI 목록 건수 확인 — 서버측 상한 해소 확인됨, confirmatory | D00 증거 코퍼스 각주 |
| HUR-005 | P2 | YouTube 동명 handle 실채널 동일성 확인 | YT 소스 정체성 CONDITIONAL 해제 |

| HUI-007 | P2 | **신규** — Syncly UI에서 이 workspace의 댓글/리플라이/VOC 수집 옵션이 (a) 존재하는지 (b) 켜져 있는지 (c) 어느 패널에 댓글 내용이 보이는지 확인만(설정 변경 금지). 요청서: claude-c `control/human_review/HUI-007_comment_ingestion_ui_read.md` | OBS-0003 라벨·CIT-07 문구만 — 나머지 전부 계속 |
| HUR-008 | P1 | 12개 계정의 8월(01~31) 창 내 면도 카테고리 포스트 유무 + 각 PostID/URL (Dashboard Author 차원 또는 Quick Search; 진입 6곳은 양성 대조) | 저진입(0.38%) 인과 해석만 — 다른 작업 전부 계속 |

각 항목의 정확한 UI 경로·확인 대상·가설 A/B·다운스트림은 운영 repo의 HUR 티켓(16필드)에 기재 — 필요 시 C가 요청 시점에 제공.
