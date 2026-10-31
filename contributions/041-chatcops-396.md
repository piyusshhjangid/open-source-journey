# OSS Contribution #41 — chatcops PR #396: feat(widget): add Dutch locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open).
- **Pull request:** [#396 — feat(widget): add Dutch locale](https://github.com/codercops/chatcops/pull/396)
- **Target branch:** `dev`
- **Merge commit:** `095829b283bea8858a5c764dbbdbe043efbb7645`
- **Status:** Merged
- **Date merged:** 2026-10-28 (UTC)

## 1. Problem and requirements

Part of #55

Adds the Dutch (nl) widget locale, lists Dutch in the Available Locales documentation, and includes a patch changeset for @chatcops/widget. Placeholders are preserved so untranslated future keys can fall back to English.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- Widget build, panel build (emits dist/locales/nl.js), and loader build passed.
- Type declaration generation and tsc --noEmit passed.
- vitest run --project @chatcops/widget — 393 tests passed.
- git diff --check passed.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Preserving interpolation placeholders and checking the emitted locale bundle are key parts of a localization change.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#55](https://github.com/codercops/chatcops/issues/55) (open) |
| Pull request | [#396](https://github.com/codercops/chatcops/pull/396), merged |
| Merge target | `dev` |
| Merge date | 2026-10-28 |
| Validation | PR-reported results summarized above |

**Contribution #41 complete.**
