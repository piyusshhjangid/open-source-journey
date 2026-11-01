# OSS Contribution #59 — ChatCops PR #562: fix(server): block trailing-dot local webhook hosts

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#559](https://github.com/codercops/chatcops/issues/559) (closed)
- **Pull request:** [#562 — fix(server): block trailing-dot local webhook hosts](https://github.com/codercops/chatcops/pull/562)
- **Status:** Merged
- **Date merged:** 2026-10-31

## Problem and implementation

Normalize trailing DNS root dots for webhook host safety checks and reject trailing-dot localhost and blocked internal hostnames while preserving allowed public URLs.

## Validation

Webhook delivery tests (52), server build and typecheck, Biome, and diff check were reported passing.

## What I learned

This contribution strengthened my practice in defining edge-case behavior, adding focused regression coverage, and documenting changes in the package’s established workflow.

## Result

The change was merged into ChatCops. See the linked PR for the full diff, review discussion, and checks.
