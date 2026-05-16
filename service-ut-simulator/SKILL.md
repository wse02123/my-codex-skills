---
name: service-ut-simulator
description: Service usability test simulation for planners. Use when Codex needs to review a service, feature, mockup, screen-flow image, or prototype description and produce a UT-style validation report plus persona-level raw data. The skill supports both new-user and existing-user contexts, identifies usage situations, usage hurdles, non-usage hurdles, target-fit issues, and improvement ideas without treating simulated personas as statistically representative users.
---

# Service UT Simulator

## Purpose

Use this skill to simulate a planner-style usability test from screen-process images and the user's feature/service explanation.

Do not present the simulation as real user research. Treat it as a structured pre-UT thinking tool that reveals likely usage contexts, friction points, non-usage reasons, and questions to verify in real UT or interviews.

## User Onboarding

When the user invokes this skill for the first time in a conversation, start with a short Korean onboarding message before asking for inputs. The message must help non-technical service planners understand what the skill is, when to use it, what it can produce, and what it cannot prove.

Use this structure:

1. Who this skill is for
   - Explain that it is for service planners, PMs, PO/UX planners, and product designers who want to review a service flow, mockup, or feature idea before real UT.

2. What this skill can do
   - It can inspect screen-flow material and service explanations.
   - It can simulate varied persona contexts.
   - It can identify where users may notice, understand, use, hesitate, fail, or ignore the service/feature.
   - It can produce two outputs: a UT report and persona-level 로우데이터 preview.

3. What this skill cannot do
   - It cannot replace real UT, interviews, analytics, or statistically valid research.
   - It must not claim demographic usage rates or market demand.

4. How to use it
   - Tell the user to provide the required information first.
   - Show both required information and optional information in the first onboarding message.
   - Tell the user optional information can be provided partially and improves accuracy.
   - If information is missing, ask only for the missing required items.

Keep onboarding concise, but do not omit the optional-information guide. Do not over-explain the methodology before the user provides inputs.

## Core Rule

The 100 personas are not a real population sample and are not based on Korean demographic statistics. Never produce statistical conclusions such as "30s men use this most" or "42% of users will use it."

Instead, report patterns as simulated context findings:

- "Several simulated contexts exposed this hurdle."
- "The feature seemed stronger when the user had this situation."
- "The expected target split into sub-contexts that behaved differently."
- "This is a hypothesis to verify in real UT."

## Required Input

Ask only for missing required inputs. If the user provides partial information, proceed after clarifying the smallest number of blocking gaps.

1. Screen process image, mockup, or flow material
2. Screen order
3. Test user context: new user or existing user
4. Feature/service being tested and the user's desired core action
5. Expected target

## Initial Request Template

When the user invokes the skill without enough information, ask in Korean with this onboarding plus input-request template. Include the optional-information section every time the first onboarding message is shown, even if the user did not ask for it:

```markdown
이 스킬은 서비스 기획자, PM/PO, UX 기획자가 화면 flow나 목업을 바탕으로 실제 UT 전에 사용성 가설을 점검할 때 쓰는 도구예요.

제가 할 수 있는 일은 다음과 같아요.
- 화면 흐름을 보고 사용자가 어디서 이해하고, 망설이고, 실패하거나 이탈할 수 있는지 점검합니다.
- 신규 사용자/기존 사용자 맥락에 맞춰 100개의 가상 페르소나 맥락을 시뮬레이션합니다.
- 결과는 UT 보고서와 로우데이터 미리보기로 정리합니다.

단, 이 결과는 실제 UT나 통계 조사를 대체하지 않습니다. "50대 남성이 많이 쓴다" 같은 인구통계 결론이 아니라, 실제 UT에서 확인해야 할 사용 맥락과 허들을 찾는 용도입니다.

먼저 아래 필수정보를 주세요.

## 필수정보
1. 화면 프로세스 이미지, 목업, 또는 화면 flow 자료
2. 화면 순서
3. 테스트 사용자 맥락: 신규 사용자 / 기존 사용자
4. 검증할 기능과 사용자가 완료해야 하는 핵심 행동
5. 현재 예상 타겟

## 선택정보
아래는 전부 채우지 않아도 됩니다. 아는 만큼만 주시면 가정이 줄고 결과가 더 날카로워져요.

### 서비스/기능 맥락
- 서비스명
- 이 기능을 만든 이유
- 사용자가 얻어야 하는 핵심 가치
- 검증하고 싶은 가설
- 내부에서 논쟁 중인 지점
- 특히 걱정되는 UX 지점

### 사용자 맥락
- 신규 사용자라면: 가입/로그인 포함 여부, 온보딩 포함 여부, 첫 사용자가 반드시 이해해야 하는 정보
- 기존 사용자라면: 기존에 같은 일을 처리하던 방식, 기존에 익숙한 화면/기능, 이번에 새로 보거나 바뀐 부분

### 성공 기준
- 성공으로 볼 행동
- 중간에 반드시 거쳐야 하는 단계
- 사용자가 이탈하면 안 되는 중요 지점
- 실패/오류가 났을 때 사용자가 복구해야 하는 행동

### 제약 조건
- 모바일/PC 기준
- 로그인, 결제, 예약, 신청, 업로드 등 민감 행동 포함 여부
- 테스트에서 제외할 행동
- 실제 서비스와 목업이 다른 부분
- 접근할 수 없는 화면이나 아직 개발되지 않은 화면
```

If the user already supplied some items, ask only for the missing items.

If an implementation summarizes the onboarding instead of copying the template exactly, it must still include these four optional-information groups: 서비스/기능 맥락, 사용자 맥락, 성공 기준, 제약 조건.

For existing-user tests, ask one additional question when it is not inferable:

```markdown
기존 사용자는 지금 같은 일을 어떤 방식으로 처리하고 있나요?
```

For new-user tests, ask one additional question when it is not inferable:

```markdown
가입/로그인 또는 온보딩까지 테스트 범위에 포함할까요?
```

## Optional Input

Use optional details when provided, but do not block the simulation if they are missing. State assumptions in the report.

Do not present optional input as homework the user must complete. Present it as accuracy boosters the user can provide partially.

Group optional input in Korean using these categories:

### 서비스/기능 맥락

- Service name
- Reason the feature/service exists
- Core user value
- Planning hypothesis
- Concerns or disputed internal points
- Specific UX risks the user wants checked

For new users, also use:

- Whether signup/login is included
- Whether onboarding is included
- What a first-time user must understand before using the feature

For existing users, also use:

- Existing feature or habit the user already has
- Existing way users solve the same job today
- What is newly added or changed
- Where the existing user should discover the feature/change

### 성공 기준

- Success behavior
- Required intermediate steps
- Drop-off points the user is most worried about
- Recovery behavior expected after failure, validation error, or upload rejection

### 제약 조건

- Login, onboarding, payment, reservation, application, upload, or other sensitive-action constraints
- Mobile or PC context
- Actions excluded from the test
- Differences between the mockup and the real service
- Screens that are inaccessible, under development, or intentionally omitted

## Workflow

1. Understand the input material.
   - Identify screens, screen order, visible entry points, CTA labels, required user actions, and unclear states.
   - If images are provided, inspect them directly before reasoning.

2. Classify the test context.
   - New user: evaluate first impression, value understanding, signup/onboarding burden, first successful action, and reasons to continue or leave.
   - Existing user: evaluate discoverability, fit with existing habits, comprehension of the change, perceived advantage over the old behavior, and confusion caused by the change.

3. Generate 100 personas using fixed attributes only.
   - Vary age band, gender, region type, job/role, household type, income/consumption tendency, digital familiarity, interests, knowledge background, lifestyle, primary device, app habits, time pressure, decision style, MBTI, personality keywords, information-search style, purchase/reservation/signup behavior, and general attitude toward new services/features.
   - Do not include service-specific need, likelihood to use this feature, usage reason, non-usage reason, or hurdles as persona attributes. These are test results.
   - Avoid making the persona set overly concentrated in one age, gender, job, lifestyle, or digital skill group unless the user explicitly constrains the target.
   - If the user gives an expected target such as "50s men", include varied sub-contexts inside that target and comparison contexts outside the target. Do not treat the mix as a population ratio.

4. Give each persona a 30-day lifestyle pattern.
   - Internally reason from repeated routines, irregular events, time pressure, work/leisure rhythm, and domain-relevant moments.
   - Use 10-minute granularity as a mental model for finding realistic touchpoints, but do not print a full 30-day 10-minute timetable unless the user explicitly asks.
   - For each persona, derive 1 to 3 relevant life touchpoints instead of inventing a full visible timetable.
   - Match touchpoints to the domain: exercise services around workout/health moments, food services around meal/planning moments, shopping around browsing/purchase moments, finance around money-management moments, education around study/career moments, etc.

5. Run the simulated UT.
   - Place the service/feature into each persona's plausible 30-day context.
   - Decide whether a touchpoint occurs, whether the persona notices the entry point, whether they understand the value, whether they try the flow, where they hesitate, and whether they complete the desired core action.
   - Record usage reasons, usage hurdles, non-usage reasons, and improvement hints as derived observations.
   - Classify each persona's reaction type without treating it as a statistic: immediate use, hesitant use, deferred use, non-use, failed recovery, or needs help from another person.
   - If the flow includes failure, error, rejection, validation, or exception screens, analyze recovery separately: whether the user understands what failed, what to fix, where to fix it, and how to try again.
   - Separate evidence labels: screen observation, persona-context inference, and real-UT validation needed.

6. Produce two outputs.
   - UT report: concise decision-making summary.
   - Raw data: persona-level evidence table.
   - Default output in chat: full UT report plus a 10-row raw-data preview.
   - If the user asks for the full 100-row raw data, provide it as a separate file-friendly table or in chunks.

Read `references/report-format.md` before writing the UT report. Read `references/raw-data-schema.md` before writing raw data.

## Output Rules

- Separate the UT report and raw data clearly.
- Use Korean unless the user asks for another language.
- Label all simulated findings as hypotheses, patterns, or observations from simulated contexts.
- Include assumptions when optional input is missing.
- Avoid fake precision. Do not use percentages, rankings by demographic group, or market-size language.
- Do not write "100명 중 n명" in the report. If counts are needed, keep them in raw data or phrase them as internal simulation signals.
- Highlight target-fit issues inside the user's expected target, especially sub-contexts that do not show the expected behavior.
- End with real UT questions that the planner should verify with actual users.
- Use "로우데이터" consistently in Korean output.
- Before finalizing, check: no demographic-statistical claims, assumptions are visible, screen observations and inferences are separated, expected-target weaknesses are included, recovery issues are covered when relevant, and the output ends with actual UT verification questions.
