# my-codex-skills

Personal Codex skill collection for service planning, UX review, product thinking, and vibe-coding workflows.

## Skills

### service-ut-simulator

Pre-UT simulation skill for service planners, PM/POs, UX planners, and product designers.

Use it when you want to review a service flow, mockup, or feature idea before real usability testing. It helps identify likely usage contexts, friction points, non-usage reasons, recovery issues, and real UT questions.

Outputs:

- UT report for decision-making
- Persona-level 로우데이터 preview

It is not a replacement for real UT, interviews, analytics, or statistical research. It is designed to organize hypotheses and risks to validate with real users.

## Install a Skill

Copy a skill folder into your Codex skills directory.

Example for `service-ut-simulator`:

```powershell
Copy-Item -Recurse -Force `
  '.\service-ut-simulator' `
  "$env:USERPROFILE\.codex\skills\service-ut-simulator"
```

Then start a new Codex conversation and run:

```text
$service-ut-simulator 실행해줘
```

If Codex does not automatically detect the skill, ask it to open the skill file directly:

```text
service-ut-simulator\SKILL.md 파일을 읽고 그 지침대로 실행해줘.
```

## Repository Structure

```text
my-codex-skills/
├─ README.md
└─ service-ut-simulator/
   ├─ SKILL.md
   ├─ agents/
   │  └─ openai.yaml
   └─ references/
      ├─ report-format.md
      └─ raw-data-schema.md
```
