# AI-Native SDLC

An evidence-gated lifecycle router Skill for AI-assisted software work.

`v0.1.3` is the current DJX personal main version. It keeps lifecycle receipts evidence-backed, treats one-gate-at-a-time as dependency order rather than an automatic turn end, and preserves explicit approval gates for Deploy and other external actions. The immutable `v0.1.0`–`v0.1.2` tags remain preserved. It has not yet completed a real-project pilot.

## What it does

- identifies the current lifecycle stage and the first unpassed gate;
- reuses accepted project evidence instead of replaying completed stages;
- continues to the next already-authorized gate without treating every accepted gate as a task endpoint;
- routes Plan, Design, Build, Test, Deploy, and Maintain work to on-demand references;
- keeps accepted-Spec Build and bounded fixes on the direct `tospec` + canonical-workflow path;
- stops releases, deployments, credentials, permissions, and external writes at explicit authorization gates.

It is one router Skill with references, not six competing child Skills or a second project-status system.

## Install

```bash
npx skills add daijx-ai/ai-native-sdlc
```

The Skill may also be installed by copying this repository into a host's supported Skill directory.

## Portability boundary

This release expects companion workflow authorities such as:

- `$HOME/.agents/sop/programming-collaboration-workflow.md`
- `$HOME/.agents/protocols/agent-collaboration-protocol.md`
- `$tospec`
- `$cross-agent-review`

The repository is portable across home directories, but it is not a standalone universal workflow. Other users must provide equivalent authority files or adapt the routing references, then verify positive and negative trigger cases in fresh sessions before enabling implicit invocation. File presence alone does not prove runtime discovery or correct routing.

## Release evidence

- Skill structure validation: passed
- Repository-root `SKILL.md`: present and validated
- Public-package secret and private-context scan: passed
- Real-project pilot: not yet run

## Origin

Inspired by Anthropic's [AI-Native SDLC Playbook](https://claude.com/blog/the-ai-native-sdlc-playbook) and adapted to DJX's existing local workflow, authorization, verification, and cross-agent authorities.
