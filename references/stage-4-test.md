# Stage 4 — Test

Use this stage whenever behavior or an agent-facing rule/configuration must be proven.

## Feedback loop

1. Select and run the applicable evidence path from `$HOME/.agents/sop/programming-collaboration-workflow.md` §4; do not define a second test matrix here.
2. Protect the evidence surface from being weakened to make a result green. A changed test, fixture, threshold, or judge must be justified by the accepted Contract rather than the failing implementation.
3. Route ordinary-user UI acceptance to `$HOME/.agents/sop/black-box-user-acceptance.md`; screenshots alone are not an interaction pass.
4. Route Heavy/high-impact independent review through the canonical workflow and `$HOME/.agents/protocols/agent-collaboration-protocol.md`; do not define another reviewer threshold or response contract here.
5. List unverified dimensions instead of converting missing infrastructure into a pass.

For agent instructions, Skills, hooks, or model changes, test realistic prompts/tasks and the resulting behavior. When CI and enough real cases exist, maintain a regression eval suite; do not build a fake continuous-eval system for a local prototype.

## Gate

The canonical workflow's applicable Test evidence demonstrates the accepted behavior and relevant failures. A green command that cannot detect the likely failure is not evidence.

## Useful measures

- first-pass CI or local acceptance rate;
- review time and repeated finding classes;
- regressions caught before versus after release.
