# Local routing map

Use installed assets as the implementation layer. This Skill coordinates them; it does not replace them.

| Need | Existing authority/capability |
| --- | --- |
| task tiering, plan, implementation discipline, technical evidence | `$HOME/.agents/sop/programming-collaboration-workflow.md` |
| delegated lanes, model roles, Task Brief, approval staging | `$HOME/.agents/protocols/agent-collaboration-protocol.md` |
| implementation scope/artifact discipline | `$tospec`; task tier still comes from the canonical workflow §0 |
| independent frozen review | `$cross-agent-review` |
| ordinary-user black-box acceptance | `$HOME/.agents/sop/black-box-user-acceptance.md` |
| reusable Agent goal/task packet | `$leader` or `$qiaomu-goal-meta-skill`, according to the requested format |
| frontend/UI implementation and browser verification | the currently installed frontend and web-testing Skills that match the task |
| security scan/fix | the matching Codex Security Skill only when explicitly requested or risk-triggered |
| end-of-task project truth cleanup | `$project-neat` when its trigger applies |

## Cross-runtime placement

- Long-lived personal Skills belong in `$HOME/.agents/skills/`, the shared authority on a compatible host.
- Global `AGENTS.md` / `CLAUDE.md` should contain only a short trigger-to-Skill pointer and hard invariants.
- Project-specific commands, architecture, artifact mapping, release routes, and monitoring stay in the nearest project authority or project-scoped Skill.
- Hooks, CI, deployment, rollback, and monitors are deterministic project mechanisms. Never emulate them with prose in this shared Skill.
