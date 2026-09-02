# reports/hdsvc/ — HD-SVC 레인 제출물

**본 repo의 단일 작성자는 Claude C다.** 이 디렉터리는 예외가 아니라 **제출 큐**다.

`HD_SUPPLIER_VS_CONSUMER`(HD-SVC)는 Human 직접 지시로 2026-09-03에 개설된 레인으로,
공개 웹의 소비자 발화를 수집해 데스크리서치 문서의 커뮤니티 장을 마감하는 것이 임무다.
A/B/C/D 4-agent harness 밖에 있으며, Lane E와도 분리돼 있다(E는 `6ea7648` 동결 유지).

## 규약

- 이 디렉터리의 문서는 전부 라벨 **`LANE_SUBMITTED`** — C 미검증이다.
- C가 독립 재현·검증한 뒤에야 `FINDINGS.md`로 승격될 수 있다.
- HD-SVC는 `STATE.json` · `LATEST.md` · `AGENTS.md` · `GATES.md` · `DECISIONS.md` ·
  `FINDINGS.md` · `TIMELINE.md` · `HUMAN_ACTIONS.md` 를 **수정하지 않는다.** C의 단일 작성자 파일이다.
- PUBLIC-SAFE 원칙 동일 적용: 집계 수치·방법만. raw 코퍼스, 개별 포스트·계정 식별자,
  URL, 자격증명 미포함. 상세 근거는 운영 repo에 있다.

## 문서

| 문서 | 내용 | 운영 repo 근거 |
|---|---|---|
| [HDSVC_COMMUNITY_GROUNDING_v1.md](HDSVC_COMMUNITY_GROUNDING_v1.md) | 620발화 동결 코퍼스 · 2축 코드북 · MEANING_FATE · dense embedding 재검정 | `syncly_demo` `claude-hdsvc/community-grounding` @ `dc91c8a` |

## C 우선 검토 요청

1. 대상 데스크리서치 문서 정정 2건 — 경쟁 모델 설계수명 기재 `UNVERIFIED`, 시장별 t=0 오류 2개
   (한 시장은 30일 차이로, 정정 전 해당 시장 시계열 전량 무효였다)
2. P축 코드 건수를 문제 보고 건수로 읽으면 안 된다는 해석 규칙 — 기존 코드북 운용에도 적용 가능한지
3. 전략 가설 "고장나지 않음을 소유하라"의 판정 변경
   (`CONSUMER_NEED_CONFIRMED` / `PRODUCT_RTB_UNRESOLVED`)
