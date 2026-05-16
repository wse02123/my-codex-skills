# UT Report Format

Use this structure for the decision-making report. Keep it concise enough for a planner to share with product, design, or stakeholder partners.

## 1. 검증 대상 요약

- 서비스/기능:
- 테스트 사용자 맥락: 신규 사용자 / 기존 사용자
- 입력 자료:
- 화면 순서:
- 기능 진입점:
- 사용자가 완료해야 하는 핵심 행동:
- 예상 타겟:
- 주요 가정:

## 2. 시뮬레이션 전제

State that the 100 personas are simulated contexts, not a demographic sample or real UT result.

Include:

- 이 결과는 실제 사용자 조사 결과가 아니라 사전 검증용 시뮬레이션이다.
- 100인의 페르소나는 실제 인구통계 표본이 아니다.
- 발견사항은 실제 UT와 인터뷰에서 확인해야 할 가설이다.

## 3. 핵심 발견 요약

Summarize the most important findings in 3 to 5 bullets:

- 기능이 잘 작동한 상황
- 가치 이해가 약했던 상황
- 반복적으로 드러난 사용 허들
- 반복적으로 드러난 미사용 허들
- 예상 타겟과 어긋난 지점

Each bullet should include an evidence label:

- 화면 관찰
- 페르소나 맥락 추론
- 실제 UT 확인 필요

## 4. 사용 맥락 분석

Describe when and why the service/feature becomes relevant:

- 사용이 자연스러웠던 상황:
- 사용 직전 트리거:
- 사용자가 기대한 이점:
- 맥락상 가치가 약했던 상황:

Do not claim that a demographic group is the main target. Prefer context-based language such as "시간 압박이 높고 즉시 결정을 해야 하는 사용자 맥락".

## 5. 예상 타겟 검증

Compare the user's expected target with simulated sub-contexts:

- 사용자가 예상한 타겟:
- 예상 타겟 안에서 잘 맞았던 하위 맥락:
- 예상 타겟 안에서 잘 맞지 않았던 하위 맥락:
- 예상과 달랐던 이유:
- 실제 UT에서 검증할 타겟 가설:

Avoid saying the target has been redefined by the simulation alone.

## 6. 사용으로 이어진 시뮬레이션 맥락의 허들

Use a table:

| 허들 | 발생 맥락 | 사용자 영향 | 개선 방향 |
|---|---|---|---|

Focus on discovery, comprehension, trust, input burden, flow continuity, information architecture, CTA clarity, and next-action clarity.

## 7. 미사용으로 이어진 시뮬레이션 맥락의 허들

Use a table:

| 미사용 이유 | 해당 맥락 | 대표 페르소나 예시 | 개선 또는 제외 판단 |
|---|---|---|---|

Include cases where non-usage is acceptable because the feature is not for that context.

## 8. 오류/실패 복구성 분석

Include this section when the flow has failure, error, validation, rejection, or exception screens.

- 사용자가 무엇이 실패했는지 이해할 수 있는가:
- 사용자가 어디를 고쳐야 하는지 알 수 있는가:
- 사용자가 어떻게 다시 시도해야 하는지 알 수 있는가:
- 부분 성공/전체 실패/중복 제외 같은 결과 상태가 명확한가:
- 복구 흐름에서 가장 큰 이탈 위험:

## 9. 개선 제안

Group suggestions by planning action:

- 진입점:
- 문구/정보 구조:
- 화면 흐름:
- 신뢰/안심 장치:
- 실제 UT에서 확인할 타겟 가설:
- 후순위 또는 제외할 요소:

End this section with the top 3 priority improvements.

## 10. 실제 UT에서 확인할 질문

Include:

- 관찰 과제:
- 인터뷰 질문:
- 확인해야 할 행동:
- 성공 기준:
- 실패 기준:

Avoid long survey-style lists. Prioritize questions that validate the riskiest assumptions.

End with "실제 UT에서 반드시 볼 관찰 포인트 5개".
