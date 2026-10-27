# OSS Contribution #32 — chatcops PR #372: feat(store-postgres): add pgvector vector storage

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Closes #359](https://github.com/codercops/chatcops/issues/359) (closed when checked).
- **Pull request:** [#372 — feat(store-postgres): add pgvector vector storage](https://github.com/codercops/chatcops/pull/372)
- **Target branch:** `dev`
- **Merge commit:** `7e1e8cfa378407735142547f1627ebf689a9d3ab`
- **Status:** Merged
- **Date merged:** 2026-10-27 (UTC)

## 1. Problem and requirements

Closes #359

Adds optional pgvector-backed vector storage to `@chatcops/store-postgres`.

- Adds `migrateVectors(db, { dimensions, tablePrefix })`, separate from the existing `migrate`.
- Exposes the vector store through `postgresStorage({ db, dimensions })`.
- Implements cosine similarity search, metadata filters with exact JSON types, upserts, and deletion by source.
- Adds Postgres full-text keyword search using `segmentWords` for Japanese and Chinese text.
- Runs filtered HNSW searches with pgvector iterative scans inside a transaction.
- Adds Postgres vector conformance coverage, a pgvector-enabled CI service, storage documentation, and a minor changeset.

## 2. Implementation

The contribution was merged into `dev`. The scope and implementation details recorded in the PR description are summarized above. The complete diff and file list remain available on GitHub.

## 3. Validation

- Postgres package build and typecheck — passed.
- New vector unit tests — passed.
- Biome checks for changed source, tests, and docs — passed.
- `node scripts/check-doc-samples.mjs` — passed.
- `git diff --check` — passed.
- Full coverage locally — 1,324 passed, 136 skipped; 11 unrelated Cloudflare/Miniflare tests failed because the environment blocked local sockets.
- Postgres conformance requires `CHATCOPS_TEST_POSTGRES_URL` and pgvector; run it in an environment with the extension available.

## 4. Maintainer review

GitHub reports this pull request as merged. This record does not infer approval details beyond that status; use the linked PR for the review discussion and checks.

## 5. What I learned

- Designing a database-backed vector store requires explicit migration, filtering, and conformance-test decisions.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Pull request | [#372](https://github.com/codercops/chatcops/pull/372), merged |
| Linked issue | #359 (closed) |
| Merge target | `dev` |
| Merge date | 2026-10-27 |
| Validation | See the PR-reported results above |

**Contribution #32 complete.**
