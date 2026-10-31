# OSS Contribution #42 — chatcops PR #407: feat(widget): add Korean locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open).
- **Pull request:** [#407 — feat(widget): add Korean locale](https://github.com/codercops/chatcops/pull/407)
- **Target branch:** `dev`
- **Merge commit:** `3896eb00717c186e067e8827079381675d74dfce`
- **Status:** Merged
- **Date merged:** 2026-10-28 (UTC)

## 1. Problem and requirements

Part of #55

Adds the Korean (ko) widget locale in Hangul, lists Korean in the Available Locales documentation, and includes a patch changeset for @chatcops/widget. Placeholders are preserved so untranslated future keys can fall back to English.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- Widget build, panel build (emits dist/locales/ko.js), and loader build passed.
- Type declaration generation and tsc --noEmit passed.
- vitest run --project @chatcops/widget — 394 tests passed.
- git diff --check passed.
- node scripts/check-doc-samples.mjs — 119 snippets checked; the script exited with TS2688 because @types/node is missing from the local dependencies.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Preserving interpolation placeholders and checking the emitted locale bundle are key parts of a localization change.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#55](https://github.com/codercops/chatcops/issues/55) (open) |
| Pull request | [#407](https://github.com/codercops/chatcops/pull/407), merged |
| Merge target | `dev` |
| Merge date | 2026-10-28 |
| Validation | PR-reported results summarized above |

**Contribution #42 complete.**
