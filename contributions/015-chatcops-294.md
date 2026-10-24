# OSS Contribution #15 — ChatCops Cross-Origin Request E2E Coverage

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#233 — Run a browser test with the chat API on a different origin than the page](https://github.com/codercops/chatcops/issues/233) (closed as completed)
- **Pull Request:** [#294 — test(e2e): cover cross-origin chat requests](https://github.com/codercops/chatcops/pull/294)
- **Branch:** `feat/233-cross-origin-e2e`
- **Commit:** `ed44fa6`
- **Merge commit:** `d5a3995`
- **Status:** Merged into `dev`; issue #233 closed as completed
- **Label:** Not recorded in the PR summary.
- **Date:** 22 October 2026

## 1. Problem and requirements

The widget needed browser-level coverage for communicating with a chat API served from a different origin, including the browser-generated CORS preflight.

## 2. Implementation

Added a separately configurable mock API server, cross-origin HTML fixture using the built widget, and Playwright coverage for preflight headers, request order, and streamed assistant output. Updated Playwright to run both servers and preserved same-origin fixtures.

## 3. Validation

PR-reported: widget and workspace builds, typecheck, Biome checks, and `git diff --check` passed; `pnpm e2e` passed 10/10 tests. Deliberately removing `Access-Control-Allow-Headers` made the browser block the POST and fail the test. The full `pnpm test` report was 932 passed, 28 skipped, and 5 provider-test timeouts; those failures were disclosed and were outside the E2E change.

## 4. Maintainer review

Anurag629 requested changes to isolate request recording to the API server and remove redundant or flaky assertions. The contributor fixed all three items. The maintainer then confirmed the E2E job and Biome passed and approved the corrected tests.

## 5. What I learned

- Browser security behavior needs a real browser test. Keep test-server state isolated so parallel same-origin specs cannot contaminate cross-origin assertions.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#233](https://github.com/codercops/chatcops/issues/233), closed |
| Pull request | [#294](https://github.com/codercops/chatcops/pull/294), merged |
| Contribution | ChatCops Cross-Origin Request E2E Coverage |
| Merge target | `chatcops`:`dev` |
| Merge date | 22 October 2026 |
| Validation | PR and maintainer-reported results summarized above |

**Contribution #15 complete.**
