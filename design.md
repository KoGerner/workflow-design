# BIA-Workflow — design

`© 2026 AI4BCM - BIA-Workflow method, CC BY 4.0.`

## Principle

AI prepares each step; the human decides, approves and owns the result. Every stage ends
at an approval gate. Nothing is written back to the company's records without a human
saying so, and the method never drafts a continuity plan — it stops at the requirements
handover (BCI GPG PP4 solution design).

## The journey (`run-bia.yaml`)

| stage | name | ends with |
|---|---|---|
| 1 | Identification of scope | department/process in scope, key activities, AI-risk check, interview guide |
| 2 | Structured interview (conversational) | the complete structured capture, taken with consent in the approved environment |
| 3 | Convert the interview to the standardised template | the filled `bia-template.json` record: impact over time, resource requirements, dependencies |
| 3a | Missing-owner loop | only when a dependency has no owner: the asset owner captured and written back, human-approved |
| 4 | List the requirements (RTO, MTPD, RPO) | the drafted, consistency-checked BIA report routed for sign-off |
| 5 | Consolidate requirements + sanity check → handover | requirements for humans, never a plan |

Each stage in the YAML carries the same fields: `goal`, `copy_paste_prompt` (what the
facilitator hands the AI), `tools_to_use`, `connector_guidance`, `do_not_paste` (what must
not leave the approved environment), `approval_gate`, `reviewer_checklist`,
`expected_output`, `cites` (the knowledge chunks the stage rests on) and `next_moves`
(the offers the AI may end its turn with).

## Artifacts

A run produces a fixed set of files in the company's workspace — scope note and interview
guide, structured capture, the template-shaped record, the register update, the report,
the PP4 requirements handover. `run-bia.yaml` declares each artifact's path, markers and
minimum size, and the server enforces them before a stage may advance.

## Personas (`personas.json`)

`bia-facilitator` runs `run-bia`. (`plan-reviewer` and the deferred `draft-plan` journey were
retired 2026-08-24 — never advertised, never run; git history holds both.)
