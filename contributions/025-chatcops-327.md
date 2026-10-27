# OSS Contribution #25 — chatcops PR #327: ci(docs): type-check TypeScript samples

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Closes #201](https://github.com/codercops/chatcops/issues/201) (closed when checked).
- **Pull request:** [#327 — ci(docs): type-check TypeScript samples](https://github.com/codercops/chatcops/pull/327)
- **Target branch:** `dev`
- **Merge commit:** `c6605fc32bc349f4b46afc447f1145f44d86f601`
- **Status:** Merged
- **Date merged:** 2026-10-26 (UTC)

## 1. Problem and requirements

Closes #201

Adds a `docs:check` script that extracts TypeScript samples from MDX files and type-checks them against the built workspace packages. CI runs the check after the build.

Fixed samples that were incomplete or no longer matched the current package APIs. One reference-only `WidgetConfig` interface fragment is skipped because it uses private widget types.

## 2. Implementation

The contribution was merged into `dev`. The scope and implementation details recorded in the PR description are summarized above. The complete diff and file list remain available on GitHub.

## 3. Validation

- `pnpm -r build` — passed
- `pnpm docs:check` — passed; 107 samples checked and 1 skipped
- Temporarily introduced a type error in a docs sample and confirmed the checker failed with the correct file and line; removed the probe afterward
- `git diff --cached --check` — passed
- `pnpm lint` — reported a warning in unchanged `website/src/components/react/CodeTabs.tsx` and Windows path errors for the `packages/*` globs

## 4. Maintainer review

GitHub reports this pull request as merged. This record does not infer approval details beyond that status; use the linked PR for the review discussion and checks.

## 5. What I learned

- Documentation examples need an automated check against the actual built package APIs.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Pull request | [#327](https://github.com/codercops/chatcops/pull/327), merged |
| Linked issue | #201 (closed) |
| Merge target | `dev` |
| Merge date | 2026-10-26 |
| Validation | See the PR-reported results above |

**Contribution #25 complete.**
