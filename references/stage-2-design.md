# Stage 2 — Design

Use this stage when the outcome is accepted but requirements, UX, data, state, permissions, or acceptance remain ambiguous.

## Required outcome

Produce or update the project's authoritative Spec/PRD/Contract. Use `$HOME/.agents/sop/programming-collaboration-workflow-details.md` §2.1 as the canonical feature/actor, state, authorization, impact, and acceptance baseline. This stage adds only the Design-specific dimensions that exist:

- UI/interaction behavior and important content;
- policy conflicts, unresolved decisions, and named owners;
- explicit non-goals and compatibility constraints.

Existing project design files remain the source of truth. Do not create a second `spec.md` merely to match this playbook.

## Gate

The product owner accepts that the design solves the intent. A technical owner accepts high-risk architecture or security boundaries. Scope tradeoffs and contradictory policies must be resolved or explicitly blocked before Build.

## Useful measures

- intent-to-accepted-spec time;
- spec changes after Build starts;
- number of design conflicts discovered only during implementation or acceptance.
