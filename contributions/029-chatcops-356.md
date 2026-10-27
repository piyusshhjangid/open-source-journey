# OSS Contribution #29 — chatcops PR #356: fix(widget): keep focus inside popup chat

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Closes #335](https://github.com/codercops/chatcops/issues/335) (closed when checked).
- **Pull request:** [#356 — fix(widget): keep focus inside popup chat](https://github.com/codercops/chatcops/pull/356)
- **Target branch:** `dev`
- **Merge commit:** `82822a652ad27e394a6669a35bd84c78306732e0`
- **Status:** Merged
- **Date merged:** 2026-10-26 (UTC)

## 1. Problem and requirements

Closes #335

Keeps keyboard focus inside the open popup chat. Tab from the last focusable element wraps to the first, and Shift+Tab from the first wraps to the last. The focusable elements are recalculated on each key press so controls that appear or disappear are handled.

Adds `aria-modal="true"` to the popup dialog. Inline mode remains unchanged. Includes a patch changeset for `@chatcops/widget`.

## 2. Implementation

The contribution was merged into `dev`. The scope and implementation details recorded in the PR description are summarized above. The complete diff and file list remain available on GitHub.

## 3. Validation

- Popup panel tests: 14 passed.
- Widget Vite builds completed; TypeScript declaration build passed.
- `npm run size`: passed; panel is 13.9 kB gzipped against the 14 kB limit.
- `git diff --check upstream/dev...HEAD`: passed.
- `npm run lint` exited successfully, with existing Windows Biome glob diagnostics and a CodeTabs warning.
- Full coverage could not be verified locally: the pinned pnpm version could not be downloaded, and the fallback run hit Windows temporary-file permission errors. CI should run the canonical checks.

## 4. Maintainer review

GitHub reports this pull request as merged. This record does not infer approval details beyond that status; use the linked PR for the review discussion and checks.

## 5. What I learned

- This contribution reinforced the value of testing the behavior at the boundary described by the issue and documenting the verification results.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Pull request | [#356](https://github.com/codercops/chatcops/pull/356), merged |
| Linked issue | #335 (closed) |
| Merge target | `dev` |
| Merge date | 2026-10-26 |
| Validation | See the PR-reported results above |

**Contribution #29 complete.**
