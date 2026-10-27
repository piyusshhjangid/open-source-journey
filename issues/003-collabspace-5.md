# CollabSpace Issue #5 — [Security] Hash refresh tokens at rest and handle token reuse

## GitHub record

- **Repository:** [piyusshhjangid/CollabSpace](https://github.com/piyusshhjangid/CollabSpace)
- **Issue:** [#5 — [Security] Hash refresh tokens at rest and handle token reuse](https://github.com/piyusshhjangid/CollabSpace/issues/5)
- **Status:** open (checked 27 October 2026)
- **Created:** 2026-10-26
- **Last updated:** 2026-10-26
- **Labels:** `enhancement`
- **Linked pull request:** None found in the issue body or comments at the time of review.

## Goal

Reduce the impact of a database read or a replayed refresh token.

## Scope described in the issue

- Store a one-way digest of refresh tokens rather than the bearer token itself.
- Define token-family or session behavior for rotation and detected reuse.
- Revoke the affected session or family when reuse is detected.
- Design a migration that handles existing active tokens safely.
- Preserve logout and session revocation behavior.

## Acceptance criteria

- [ ] Raw refresh tokens are never persisted or logged.
- [ ] A rotated token cannot be used twice.
- [ ] Reuse follows a documented revocation policy.
- [ ] Existing sessions transition safely during deployment.
- [ ] Tests cover rotation, logout, expiry, and reuse.

## Current state

This is an open roadmap issue in the now-public CollabSpace repository. Its acceptance criteria remain unchecked on GitHub. No implementation or completion is claimed in this journal entry.

## Contribution notes

- **Work category:** Security
- **Issue theme:** Hash refresh tokens at rest and handle token reuse
- **Next step:** Review the current code and repository guidance, confirm the scope still matches the project, then implement through a focused pull request linked to this issue.
- **Record policy:** Update this file after work begins, after review feedback, and when the issue closes. Keep implementation and test results tied to the actual PR.

## Learning focus

Refresh-token rotation, digest storage, replay handling, and safe migration of active sessions.
