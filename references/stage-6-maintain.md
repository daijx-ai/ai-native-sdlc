# Stage 6 — Maintain

Use this stage only for software that is running, delivered, or receiving real feedback. A static prototype has no production-monitoring stage yet.

## Close the loop

1. Name the real signal source: user feedback, support issue, CI history, deployment health, logs, or a stable metric.
2. Keep detection deterministic where possible. Version the threshold/baseline and test that the alarm can fire.
3. Tier responses: record, diagnose read-only, propose a change, or execute a pre-approved reversible runbook. Higher tiers require stronger gates.
4. Turn a material incident or repeated feedback into the Stage 1 intent contract with evidence, affected systems, desired outcome, and open questions.
5. Add a regression case for a fixed incident when the project has a suitable test/eval surface.
6. Track dismissal/noise so monitoring does not become another unattended output factory.

For local/pilot projects, maintenance may be a small feedback and open-loop ledger plus current project status. Do not claim autonomous operations because a schedule, config, or monitor file exists.

## Gate

The service owner triages the finding. Any change re-enters Plan/Design/Build/Test at the smallest correct stage.

## Useful measures

- signal breach to evidence-backed diagnosis;
- findings that become accepted fixes;
- repeat incidents and false-positive rate;
- continued use after delivery.
