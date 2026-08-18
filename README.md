# workflow-design — the BIA-Workflow method

The method behind the BIA-Workflow agent (`https://agent.ai4bcm.org`): a Business Impact
Analysis run as a guided journey where the AI prepares every step and a human decides,
approves and owns the result. This repository holds the method as data — no code.

| file | what it is |
|---|---|
| `run-bia.yaml` | the BIA journey: 5 stages (+ the 3a owner loop), each with goal, prompt, tools, approval gate, reviewer checklist, expected output |
| `bia-template.json` | the standardised BIA record a Stage 3 conversion fills (impact over time, resources, dependencies, recovery targets) |
| `personas.json` | the facilitator personas a journey runs under |
| `draft-plan.yaml` | a deferred journey (continuity plan from an approved PP4 decision) — loaded, not advertised |
| `design.md` | the design in prose: stages, gates, artifacts, principles |

Used as the `design/` git submodule of the private `bia-workflow` server repository; the
server loads the journeys from here at startup. Method aligned with the BCI Good Practice
Guidelines (PP3 Analysis) as read through the BCI AI Addendum.

## Licence and attribution

`© 2026 AI4BCM - BIA-Workflow method, CC BY 4.0.`

Licensed under [Creative Commons Attribution 4.0 International](LICENSE). You may share
and adapt the method, including commercially, as long as you keep that attribution line.
