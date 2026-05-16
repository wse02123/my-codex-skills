# Raw Data Schema

Create 로우데이터 as a persona-level evidence table. Use Markdown table by default. If the user asks for a file-friendly format, use CSV-style rows or JSON.

Default chat output should include the UT report and a 10-row 로우데이터 preview. Provide the full 100-row 로우데이터 only when the user asks for it, or split it into chunks when a single response would be too long.

## Required Columns

- persona_id
- persona_summary
- user_context
- relevant_life_moment
- touchpoint_occurred
- entry_point_noticed
- value_understood
- tried_flow
- completed_core_action
- reaction_type
- usage_scenario
- reason_used
- usage_hurdles
- reason_not_used
- improvement_hint
- evidence_label
- confidence_note

## Column Guidance

`persona_id`
: Use stable IDs such as P001 to P100.

`persona_summary`
: Summarize fixed persona attributes only. Include age band, gender, role, lifestyle, digital familiarity, decision style, and attitude toward new services/features.

`user_context`
: Mark whether the run is for a new user or existing user. Add any relevant assumption.

`relevant_life_moment`
: Describe the realistic moment in the persona's 30-day lifestyle pattern where the service could appear. Do not print every 10-minute slot.

`touchpoint_occurred`
: Yes, No, or Weak. This means the persona had a plausible moment to encounter or need the service.

`entry_point_noticed`
: Yes, No, or Unclear. Explain briefly if the entry point was missed.

`value_understood`
: Yes, Partial, or No. Explain whether the feature/service value was immediately clear.

`tried_flow`
: Yes, No, or Hesitated. Use this for whether the persona began the interaction.

`completed_core_action`
: Yes, No, or Not applicable. Do not imply real conversion.

`reaction_type`
: Use one of: immediate use, hesitant use, deferred use, non-use, failed recovery, needs help from another person.

`usage_scenario`
: Summarize when, where, and why the persona used or considered the service.

`reason_used`
: Derived result. Leave blank or write "N/A" if the persona did not use it.

`usage_hurdles`
: Derived result. Include concrete flow, copy, trust, input, timing, or next-action friction.

`reason_not_used`
: Derived result. Include lack of context, weak value, existing alternative, distrust, timing mismatch, burden, or habit mismatch.

`improvement_hint`
: Give one practical design or planning hint connected to the row.

`evidence_label`
: Mark screen observation, persona-context inference, or real-UT validation needed.

`confidence_note`
: Mark assumptions or evidence limits, especially when the input mockup lacks detail.

## Raw Data Rules

- Generate enough rows to support the report. For a full run, create 100 rows internally or as a separate output when requested.
- If the response would become too long, provide a representative 10-row 로우데이터 preview and ask whether to export the full 100 rows into a separate file or continue in chunks.
- Do not use counts as population statistics.
- Do not let generated persona attributes include feature-specific needs or expected behavior.
- Keep row language concrete. Avoid generic statements such as "UX was bad."
