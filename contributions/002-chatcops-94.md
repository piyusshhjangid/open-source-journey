# OSS Contribution #2 — ChatCops

## Repository

**Repository:** [`codercops/chatcops`](https://github.com/codercops/chatcops)  
**Technology:** TypeScript / JavaScript / DOM APIs / Vitest / pnpm workspace / Changesets  
**Issue:** [#94 — Limit pre-chat and message length to what the server accepts](https://github.com/codercops/chatcops/issues/94)  
**Pull Request:** [#104 — fix(widget): enforce server input length limits](https://github.com/codercops/chatcops/pull/104)  
**Branch:** `fix/widget-input-maxlength`  
**Commit:** `24cfbd2` — `fix(widget): enforce server input length limits`  
**Status:** Approved and merged into `dev`  
**Date:** October 2026

---

## 1. Problem

The widget's pre-chat fields and chat message textarea did not set client-side maximum lengths to match the server's request validation. That meant users could enter more text than the server accepted and then encounter a rejected request.

The server's `chatRequestSchema` defined these limits:

- Each string value in `userData`: maximum 500 characters.
- The chat `message`: maximum 10,000 characters.

## 2. Implementation

I kept the change focused on the widget's input elements and added named constants with comments pointing back to the server validation schema.

### Pre-chat fields

In `packages/widget/src/dom/prechat-form.ts`:

- Added `MAX_PRECHAT_FIELD_LENGTH = 500`.
- Set `maxLength` to 500 for pre-chat text inputs and textareas.
- Added a comment pointing to the `userData` limit in `packages/server/src/config.ts` (`chatRequestSchema`).

### Chat input

In `packages/widget/src/dom/input.ts`:

- Added `MAX_MESSAGE_LENGTH = 10_000`.
- Set the chat textarea's `maxLength` to that constant.
- Added a comment pointing to the message limit in `chatRequestSchema`.

### Tests and release metadata

- Added a test to `packages/widget/tests/dom/prechat-form.test.ts` asserting that text, email, and textarea fields have `maxLength === 500`.
- Added `packages/widget/tests/dom/input.test.ts` to assert that the chat textarea has `maxLength === 10_000`.
- Added a patch changeset for `@chatcops/widget`.

## 3. Validation

The following commands passed:

```bash
pnpm -r build
pnpm test
pnpm -r typecheck
git diff --check
```

Full test result: **170 tests passed across 25 test files**.  
Focused widget result: **17 tests passed across 2 test files**.

## 4. Manual Testing

I manually confirmed that the pre-chat Message field stopped at 500 characters.

The demo's configured endpoint was `http://localhost:3001/chat`, but no server was listening on that port. I did not have an Anthropic API key and did not want to use a paid AI API. Instead, I used a temporary local mock HTTP/SSE server with no repository source changes or provider credentials.

The mock-backed widget flow returned simulated replies for a normal message and for a message containing 10,000 characters. The returned mock response reported `10000` characters. This validated the local widget request/response flow, **not** a live AI-provider integration.

## 5. Git Workflow

- Worked on branch `fix/widget-input-maxlength`.
- Reviewed the diff and staged only the intended five files.
- Ran the build, all tests, type checking, focused widget tests, and whitespace check.
- Added a Changesets patch entry for `@chatcops/widget`.
- Committed as `24cfbd2` and pushed the branch to my fork.
- Opened PR #104 against the upstream `dev` branch.

## 6. Maintainer Review

Anurag Verma approved and merged PR #104 into `dev`.

The maintainer's review said:

> “The constants with the comment pointing at `chatRequestSchema` are exactly what I had in mind, and the tests cover both limits.”

This feedback confirmed that the named constants, links to the validation schema, and tests matched the intended approach.

## 7. What I Learned

### Frontend and API consistency

- Client-side input limits should be consistent with the server's validation rules.
- Named constants make constraints visible and easier to maintain.
- Comments are more useful when they point to the authoritative source of the rule.

### Testing and validation

- Write targeted tests for each input limit.
- Run focused tests while developing, then run the full test suite, build, and typecheck before submission.
- A passing unit test does not replace a manual smoke test of the widget flow.

### Repository and contribution workflow

- Inspect package scripts before running development commands.
- A monorepo may have package-specific dependencies and workflows.
- Changesets are part of the release process for published packages.
- Keep a PR focused on the assigned issue and avoid unrelated setup changes.

### Debugging local demos

- A page being served by Vite does not mean its API backend is running.
- Check the configured API URL and whether the expected port is listening.
- A local mock can verify request/response handling without API credentials, but it must not be described as a live provider test.

## 8. What I Did Well

- Kept the implementation limited to the requested client-side constraints.
- Used named constants and referenced the server's schema.
- Added test coverage for both limits.
- Added the appropriate patch changeset.
- Ran the project's required validation commands.
- Investigated the demo connectivity issue and used a clearly identified local mock for smoke testing.
- Addressed formatting and staged-diff noise before committing.
- Received maintainer approval and got the PR merged.

## 9. What I Can Improve

- Become more independent at tracing data from the widget through the server validation path.
- Get more practice writing tests without relying heavily on step-by-step guidance.
- Learn to distinguish client-side validation, server-side validation, and provider/API failures quickly.
- Continue practising browser DevTools and network debugging.
- For future changes, test behavior at boundaries (499/500/501 and 9,999/10,000/10,001) where practical, while keeping validation aligned with the repository's requirements.

## 10. Final Result

| Item | Result |
|---|---|
| Issue | #94 |
| PR | #104 |
| Maintainer approval | Yes |
| Merged into | `dev` |
| Build | Passed |
| Full test suite | 170/170 passed |
| Typecheck | Passed |
| Focused widget tests | 17/17 passed |
| Changeset | `@chatcops/widget`: patch |
| Live AI-provider test | Not performed; local mock used instead |

**Contribution #2 complete.**
