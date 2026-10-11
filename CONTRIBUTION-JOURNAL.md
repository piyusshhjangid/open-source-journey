# OSS Contribution Journal

This journal records my open-source contributions, what I worked on, how I approached each repository, review feedback, maintainer interactions, and what I learned.

## Contribution Index

| # | Repository | Issue | PR | Status | Main Skill |
|---|---|---|---|---|---|
| 1 | [`pacocartones/free-llm-api-hub`](https://github.com/pacocartones/free-llm-api-hub) | [#67](https://github.com/pacocartones/free-llm-api-hub/issues/67) | [#198](https://github.com/pacocartones/free-llm-api-hub/pull/198) | Merged | Data verification + validation + generated artifacts + review |
| 2 | [`codercops/chatcops`](https://github.com/codercops/chatcops) | [#94](https://github.com/codercops/chatcops/issues/94) | [#104](https://github.com/codercops/chatcops/pull/104) | Merged into `dev` | TypeScript/DOM + tests + changesets + review |

## Latest Milestone: ChatCops #94

**Result:** PR #104 was approved by Anurag Verma and merged into `dev`.

The change aligns the widget's client-side input limits with the server's `chatRequestSchema` limits:

- Pre-chat text inputs and textareas: 500 characters.
- Chat message textarea: 10,000 characters.
- Added tests for the two limits and a patch changeset for `@chatcops/widget`.

Validation completed successfully:

- `pnpm -r build`
- `pnpm test` — 170 tests passed across 25 test files.
- `pnpm -r typecheck`
- Focused widget tests — 17 tests passed across 2 files.
- `git diff --check`

I also tested the widget's message flow with a temporary local mock SSE backend because I did not have, and did not want to use, a paid AI-provider API key. The mock confirmed that the widget could receive a simulated response for a normal message and for a 10,000-character message. This was a mock-backend test, not a live AI-provider integration test.

## How I Will Use This Journal

For every contribution, record:

1. Repository and issue
2. Problem and requirements
3. My understanding
4. Files changed
5. Implementation/solution
6. Tests and validation
7. Git workflow
8. PR and review feedback
9. Maintainer interaction
10. What I learned
11. What I could improve
12. Final result

The goal is not to maximize PR count. The goal is to become capable of making meaningful contributions independently.
