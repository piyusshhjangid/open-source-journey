# Contribution #9 — ChatCops: CORS Headers for Error Responses

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#158](https://github.com/codercops/chatcops/issues/158)
- **Pull request:** [#166](https://github.com/codercops/chatcops/pull/166)
- **Status:** Merged into `dev`

## Problem

Browser clients need the appropriate CORS headers on error responses as well as successful responses. If an adapter returns an applicable error without those headers, the browser may prevent the client from reading the response, obscuring the useful error details.

## Work completed

The contribution made CORS headers consistent for applicable `400` and `405` error responses across the Cloudflare, Vercel, and Express adapters. It supports the default wildcard origin (`*`) or a configured origin.

The objective was consistent browser-facing behavior without changing the intended error status and response semantics.

## Validation

The PR's reported checks included tests, workspace build, typecheck, and changeset validation. For the exact final diff, review discussion, and CI status, see [PR #166](https://github.com/codercops/chatcops/pull/166).

## Skills practised

- Cross-adapter API behavior
- CORS and browser error handling
- Regression testing for HTTP error paths
- Following project changeset and validation conventions

## Reflection

Error paths are part of an API's public contract. When middleware or adapters behave differently on failures, browser clients can lose access to diagnostic information even if the server generated a useful response. Testing both success and error responses helps keep behavior predictable.
