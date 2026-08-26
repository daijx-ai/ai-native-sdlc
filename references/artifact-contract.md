# Artifact and transition contract

Treat these as semantic roles. Map them to existing project files or systems before creating anything.

| Role | Minimum content | Typical existing homes | Transition decision |
| --- | --- | --- | --- |
| Intent | problem, outcome, constraints, non-goals, owner | current request, issue, brief, intent doc | product owner accepts/rejects |
| Spec/design | behavior, actors/state/data, impact, acceptance | PRD, Spec, Contract, design doc | product/technical owner accepts |
| Build plan | files/layers, order, risk, rollback, proof | task plan, Task Brief, implementation plan | implementer/lead accepts |
| Change | exact diff/build output | working tree, commit, package | Test gate passes |
| Test evidence | commands/actions, outputs, negative cases, unknowns | tests, report, CI/check run | reviewer accepts |
| Release evidence | target, version, approval, rollback, health | PR, release record, delivery receipt | release/customer owner accepts |
| Incident/feedback | signal, evidence, impact, triage decision | ticket, postmortem, support/feedback record | re-enter the correct stage |

## Rules

- One authoritative home per semantic role; copies link back with an ID, path, or immutable revision.
- A commit/file name is not itself an approval. Record the human decision or project-defined gate.
- Do not create a global `SDLC_STATE.md` or duplicate status ledger. Use the project's current status surface.
- Do not force a full chain for a bounded fix. The current instruction plus code/test evidence may legitimately cover several roles.
- Preserve these states separately: `studied`, `designed`, `implemented`, `running`, `verified`, `delivered`, `paid`.
- When an accepted artifact changes, invalidate only downstream evidence affected by that change.
