# Stage 5 — Deploy

Use this stage for review, packaging, merge, release, deployment, production rollback, or a customer-facing handoff.

## Before any external write

1. Reconcile the final change with accepted intent/spec/plan and Test evidence.
2. State the exact target and current state: local demo, integration candidate, release candidate, staging, production, or delivered package.
3. Identify required human approvals and protected actions. Obtain explicit authorization for the exact merge, push, deploy, permission, credential, or external-message action.
   Follow the staged approval ladder in `$HOME/.agents/protocols/agent-collaboration-protocol.md` §5.
4. Use the project's existing review and release mechanisms. Do not invent a universal branch, PR, CI, or hosting route.
5. For production, rollback is always in scope: verify it before deployment and record the command/runbook, owner, and observed rehearsal. If no safe rollback exists, stop for explicit final approval with a recovery plan and the remaining risk.
6. After an authorized action, read back the live URL/package/version/status and relevant health signals.

An agent may prepare everything up to the production gate; it may not infer permission to cross it.

## Gate

The named release owner accepts risk and evidence. Delivery, deployment, customer acceptance, and payment remain separate facts.

## Useful measures

- time to first review and release lead time;
- rollback rehearsal success;
- change failure and recovery time;
- delivered artifacts actually accepted or used.
