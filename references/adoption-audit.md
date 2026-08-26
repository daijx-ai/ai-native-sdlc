# Adoption audit

Use this mode when asked whether a project or local system has adopted the AI-native SDLC.

## Method

1. Define the project, time window, authoritative files, live runtime, and evidence boundary.
2. For each stage, label every relevant play with one of:
   - `studied`: source understood, no local design;
   - `designed`: local contract/plan exists;
   - `implemented`: code/config/artifact exists;
   - `running`: observed in the intended runtime;
   - `verified`: a falsifying acceptance check passed.
   These labels align with the `Framework/course-derived system` row in `$HOME/.agents/sop/programming-collaboration-workflow-details.md` §4. This reference applies them to the six SDLC stages; it does not redefine the vocabulary.
3. Report the first unpassed gate and the user-visible consequence. Do not average incomparable stages into one maturity score unless the user supplies a scoring contract.
4. Distinguish project delivery from framework adoption. A well-documented workflow can still have no deployed product; a small shipped fix can be valid without the full framework.

## Stage questions

- **Plan:** Is intent captured from the real requester with outcome, constraints, and an owner?
- **Design:** Is there one accepted behavior/contract and are conflicts resolved before implementation?
- **Build:** Does work follow the accepted slice with bounded ownership and plan/diff reconciliation?
- **Test:** Can the agent detect its own likely failures, including relevant rejection and regression paths?
- **Deploy:** Are review, authorization, environment, rollback, and live readback real rather than described?
- **Maintain:** Does real feedback or monitoring re-enter the lifecycle with evidence and a triage owner?

## Delivery

Return coverage, per-stage state/evidence, already-strong capabilities, missing gates, the smallest next adoption step, and material unknowns. Never report the entire framework as landed from a partial implementation.
