# OSS Contribution #54 — ChatCops PR #539: fix(widget): ignore invalid consent attributes

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#536](https://github.com/codercops/chatcops/issues/536) (closed)
- **Pull request:** [#539 — fix(widget): ignore invalid consent attributes](https://github.com/codercops/chatcops/pull/539)
- **Status:** Merged
- **Date merged:** 2026-10-31

## Problem and implementation

Validate data-wait-for-consent values while preserving the consent-safe behavior requested in review. The merged change documents accepted values and adds tests and a widget patch changeset.

## Validation

Consent tests (45), widget typecheck, ESM/panel/loader builds, declaration build, docs sample check, Biome, size-limit, and diff check were reported passing.

## What I learned

This contribution strengthened my practice in defining edge-case behavior, adding focused regression coverage, and documenting changes in the package’s established workflow.

## Result

The change was merged into ChatCops. See the linked PR for the full diff, review discussion, and checks.
