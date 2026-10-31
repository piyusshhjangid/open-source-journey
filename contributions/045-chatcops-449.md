# OSS Contribution #45 — chatcops PR #449: feat(widget): translate disclosure in 11 locales

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open).
- **Pull request:** [#449 — feat(widget): translate disclosure in 11 locales](https://github.com/codercops/chatcops/pull/449)
- **Target branch:** `dev`
- **Merge commit:** `75903b4ae1dbd4c4a5c3d74e43bdf98a2b1f5eda`
- **Status:** Merged
- **Date merged:** 2026-10-29 (UTC)

## 1. Problem and requirements

Part of #55

Adds the `sourcesLabel`, `disclosure`, and `disclosureLearnMore` translations to 11 widget locales: Arabic, German, Spanish, French, Hindi, Italian, Japanese, Korean, Dutch, Portuguese, and Chinese. Urdu is unchanged.

Adds a patch changeset for `@chatcops/widget`.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- Widget build, panel build, and loader build passed.
- Type declaration generation passed.
- `tsc --noEmit` passed.
- `git diff --check` passed.
- The automated test suite was not run.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Preserving interpolation placeholders and checking the emitted locale bundle are key parts of a localization change.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#55](https://github.com/codercops/chatcops/issues/55) (open) |
| Pull request | [#449](https://github.com/codercops/chatcops/pull/449), merged |
| Merge target | `dev` |
| Merge date | 2026-10-29 |
| Validation | PR-reported results summarized above |

**Contribution #45 complete.**
