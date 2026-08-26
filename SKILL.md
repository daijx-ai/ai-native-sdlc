---
name: ai-native-sdlc
description: Route stage-ambiguous or cross-stage software work through the next evidence-backed gate. Use for a new product or feature with no accepted Spec, an unresolved governing artifact conflict, project resumption, Test/Deploy/Maintain transitions, an incident whose cause, impact, or re-entry stage is unresolved, or an adoption audit. Do not invoke merely because accepted-Spec implementation or a bounded fix spans Build and Test; accepted-Spec Build, an already-reproduced scoped bug with accepted expected behavior, and a single already-scoped edit or fix go directly to tospec and the canonical workflow. Do not use for read-only explanations.
metadata:
  version: "0.1.1"
---

# AI-Native SDLC

Move software work through the next necessary gate without replaying accepted work or creating a second project-management system.

Primary consumers are the orchestrating agent at task entry and the user during adoption audits. This Skill produces routing decisions and gate evidence, not project status.

## Authority and boundaries

1. Follow the current user request, nearest project `AGENTS.md` / `CLAUDE.md`, declared source of truth, and live code/runtime evidence.
2. Treat existing project artifacts as authoritative for their semantic role. Names such as `intent.md`, `spec.md`, and `plan.md` are examples, not mandatory filenames.
3. Reuse `$HOME/.agents/sop/programming-collaboration-workflow.md` for task tiering, implementation, and verification. Reuse `$HOME/.agents/protocols/agent-collaboration-protocol.md` for delegation and independent review. Do not restate either protocol here.
4. A local prototype, client pilot, and production system need different gates. Choose from observed state and risk, not the project's ambition.
5. This Skill never authorizes push, merge, deploy, production access, credentials, permission changes, external messages, or other outside writes. Stop at the applicable approval gate.

## Route the current task

1. Confirm the real workspace, project instructions, source of truth, dirty state, and current runtime evidence.
2. Classify the task using the canonical workflow. An incident with unresolved cause, impact, or re-entry stage enters Maintain; an already-reproduced bug with accepted expected behavior and a scoped fix belongs directly in Build/Test. A task already scoped by an accepted Spec and any other bounded fix also belongs directly in the canonical Build/Test path; do not manufacture earlier artifacts.
3. Identify the latest accepted input and the first unpassed gate. Do not repeat a stage because a preferred filename is absent.
4. Read only the matching stage reference below. If new evidence contradicts an accepted intent, Spec, permission, security boundary, or other Contract, stop the current stage, read [Artifact and transition contract](references/artifact-contract.md), return to the governing earlier stage, and invalidate affected downstream evidence before continuing.
5. Multi-stage work advances one accepted gate at a time.
6. If this Skill discovers that the task is excluded by its description, hand off to `$tospec` and the canonical workflow without a receipt. Otherwise emit a compact lifecycle receipt only when this Skill actually selected or advanced a lifecycle gate. Read-only explanations do not use this Skill or a receipt; adoption audits use their own delivery format. The receipt replaces, never accompanies, free-form lifecycle status prose:

```text
entry_stage: <stage>
accepted_input: <artifact/evidence or current user instruction>
completed_gate: <gate or none>
evidence: <path/command/runtime observation>
next_gate: <stage + owner/approval>
unverified: <material unknowns>
```

| Current need | Read |
| --- | --- |
| Raw idea, customer request, unclear outcome, or incident intake | [Stage 1 — Plan](references/stage-1-plan.md) |
| Turn accepted intent into requirements/design/acceptance | [Stage 2 — Design](references/stage-2-design.md) |
| Implement or continue an accepted change | [Stage 3 — Build](references/stage-3-build.md) |
| Verify behavior, regression, or agent configuration | [Stage 4 — Test](references/stage-4-test.md) |
| Review, package, release, deploy, or rollback | [Stage 5 — Deploy](references/stage-5-deploy.md) |
| Operate, diagnose, learn from incidents, or close the loop | [Stage 6 — Maintain](references/stage-6-maintain.md) |
| Decide which existing file is authoritative or what can trigger the next stage | [Artifact and transition contract](references/artifact-contract.md) |
| Map this workflow onto the user's installed local assets | [Local routing map](references/local-routing.md) |
| Audit whether the playbook is merely studied or actually running | [Adoption audit](references/adoption-audit.md) |

## Scale the ceremony

- **Local/prototype:** current instruction or small intent, one acceptance target, smallest implementation plan, local falsifying check. No fake PR, CI, deployment, or monitoring artifacts.
- **Client/pilot:** accepted scope and non-goals, persisted spec/plan when handoff matters, real user-facing acceptance, independent review for Heavy work, explicit delivery status.
- **Production:** all relevant pilot gates plus protected review, environment-specific authorization, verified rollback, runtime observability, and an incident-to-intent loop.

Advance only on evidence. Preserve the canonical `studied / designed / implemented / running / verified / delivered / paid` states separately.
