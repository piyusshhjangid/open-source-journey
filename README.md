# Open Source Journey

My journey from first-time contributor to independent open-source contributor. I use this repository to document what I contribute, how I work through unfamiliar codebases, the feedback I receive, and what I learn along the way.

## Contributions

| # | Project | Issue | PR | Type | Result |
|---|---|---|---|---|---|
| 1 | [free-llm-api-hub](https://github.com/pacocartones/free-llm-api-hub) | [#67](https://github.com/pacocartones/free-llm-api-hub/issues/67) | [#198](https://github.com/pacocartones/free-llm-api-hub/pull/198) | Data verification and generated artifacts | Merged |
| 2 | [ChatCops](https://github.com/codercops/chatcops) | [#94](https://github.com/codercops/chatcops/issues/94) | [#104](https://github.com/codercops/chatcops/pull/104) | TypeScript/DOM change, tests, changeset | Merged into `dev` |

## Latest Milestone

My second contribution was a code change to ChatCops. I added client-side maximum lengths for pre-chat fields and chat messages to match the server-side validation limits, wrote tests for both limits, and added a patch changeset for `@chatcops/widget`.

The maintainer approved and merged PR [#104](https://github.com/codercops/chatcops/pull/104). The review specifically praised the named constants, comments pointing to `chatRequestSchema`, and tests covering both limits.

## Current Focus

- Independent implementation and debugging in unfamiliar codebases
- Writing and understanding unit tests, not only running them
- Git/GitHub workflow and responding to code review
- CI/CD, build checks, and type checking
- Understanding source-of-truth files and generated artifacts
- Communicating clearly with maintainers
- Building a consistent contribution record while preparing for GSoC 2027

## Goals

- Make meaningful open-source contributions
- Become comfortable working in unfamiliar codebases
- Improve testing and debugging skills through real code changes
- Participate in SWoC, where suitable
- Prepare for GSoC 2027 while remembering that 2027 participation depends on the official accepted-organization list

## Contribution Journal

Detailed contribution records are stored in the `contributions/` directory.

- [Contribution #1 — free-llm-api-hub #67](contributions/001-free-llm-api-hub-67.md)
- [Contribution #2 — ChatCops #94](contributions/002-chatcops-94.md)
