# OSS Contribution #60 — ChatCops PR #565: fix: expand lint package paths on Windows

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#560](https://github.com/codercops/chatcops/issues/560) (closed)
- **Pull request:** [#565 — fix: expand lint package paths on Windows](https://github.com/codercops/chatcops/pull/565)
- **Status:** Merged
- **Date merged:** 2026-10-31

## Problem and implementation

Replace shell-dependent workspace globs in pnpm lint with a Node script that enumerates packages and passes explicit paths to Biome, consistently across Windows and Linux.

## Validation

Windows run checked 417 files with no errors. Existing warnings and informational diagnostics were noted in the PR.

## What I learned

This contribution strengthened my practice in defining edge-case behavior, adding focused regression coverage, and documenting changes in the package’s established workflow.

## Result

The change was merged into ChatCops. See the linked PR for the full diff, review discussion, and checks.
