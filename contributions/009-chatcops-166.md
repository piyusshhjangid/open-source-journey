# OSS Contribution #9 — ChatCops CORS Headers for Error Responses

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#158](https://github.com/codercops/chatcops/issues/158)
- **Pull Request:** [#166 — fix(server): send CORS header with 400 and 405 error responses](https://github.com/codercops/chatcops/pull/166)
- **Branch:** `fix/158-cors-error-responses`
- **Commit:** `46b4d93`
- **Merge commit:** `66d0858`
- **Status:** Merged into `dev`; issue #158 closed as completed
- **Label:** Not captured
- **Date:** 19 October 2026

## 1. Problem and requirements

Browser clients need applicable CORS headers on error responses as well as successful responses. Without those headers, a browser can hide useful server error details.

## 2. Implementation

Made CORS headers consistent for applicable `400` and `405` responses across the Cloudflare, Vercel, and Express adapters. Supports the default wildcard origin (`*`) or a configured origin while preserving intended error status and response semantics.

## 3. Validation

PR-reported: adapter tests passed (23); workspace build and typecheck passed; `pnpm test` passed 284 tests; `pnpm changeset status` and `git diff --check` passed. Regression tests cover default and custom CORS origins across applicable 400 and 405 responses.

## 4. Maintainer review

Review discussion details are not captured here. See [PR #166](https://github.com/codercops/chatcops/pull/166) for the full review record.

## 5. What I learned

- Error paths are part of an API public contract. Test success and error responses across adapters so browser clients can read diagnostics consistently.

## 6. Final result

| Item | Result |
|---|---|
| Repository | codercops/chatcops |
| Issue | #158 |
| Pull request | #166 |
| Contribution | ChatCops CORS Headers for Error Responses |
| Status | Merged into `dev` |
| Outcome | Standardized applicable CORS headers on `400` and `405` responses across three adapters; merged into `dev`. |
| Validation | PR-reported: adapter tests passed (23); workspace build and typecheck passed; `pnpm test` passed 284 tests; `pnpm changeset status` and `git diff --check` passed. Regression tests cover default and custom CORS origins across applicable 400 and 405 responses. |

**Contribution #9 complete.**
