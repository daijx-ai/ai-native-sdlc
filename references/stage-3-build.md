# Stage 3 — Build

Use this stage when an accepted requirement exists and code/configuration must change.

## Workflow

1. Read the accepted requirement, current project authority, actual target code, and nearby tests.
2. Classify, plan, execute, isolate parallel work, and verify through `$HOME/.agents/sop/programming-collaboration-workflow.md`; do not define a second Build procedure here.
3. For implementation work, follow `$tospec` for scope and artifact discipline. Only use a Light/fast path when `$tospec` and the canonical workflow §0 both permit it; an accepted-Spec feature slice may still be Heavy. Do not create lifecycle artifacts for ceremony.
4. If implementation reveals a requirement, permission, security, or Contract conflict, stop Build. Return to [Stage 2 — Design](stage-2-design.md), apply [Artifact and transition contract](artifact-contract.md), and invalidate affected downstream evidence. Do not edit the Spec in place and continue building.
5. Report implementation, integration, and system verification as separate states.

## Gate

The canonical workflow's applicable Build checks pass, the task-owned diff is reconciled with the accepted plan/Spec, and no governing artifact conflict remains. Build completion does not authorize release or prove customer delivery.

## Useful measures

- first implementation pass success;
- rework rounds;
- accepted-plan versus final-diff drift;
- time spent steering versus waiting, only when measured reliably.
