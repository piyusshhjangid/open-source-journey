# In-progress Contribution — OGCops Podcast Top Episodes Template

- **Repository:** [codercops/ogcops](https://github.com/codercops/ogcops)
- **Issue:** [#226](https://github.com/codercops/ogcops/issues/226)
- **Pull request:** [#239 — feat(templates): add podcast top episodes card](https://github.com/codercops/ogcops/pull/239)
- **Branch:** `codex/226-podcast-top-episodes`
- **Commit:** `2e9a775` — `feat(templates): add podcast top episodes card`
- **Status:** Open; awaiting an approving review. Three checks are passing.
- **Last status supplied:** 24 October 2026

## Change summary

Adds a `podcast-top-episodes` template with a ranked list of up to three episodes. Blank titles are skipped and ranks remain consecutive. Long titles truncate to one line; durations stay in a fixed right-hand column and blank durations are hidden. Light backgrounds use a darkened accent for readable rank numbers.

## Validation reported in the PR

- `npm run check` — 0 errors, 0 warnings, 10 hints.
- Focused template test — 5 passed.
- Full suite — 1,011 passed; the unrelated agenda PNG/SVG rendering test timed out after 5 seconds, including when run alone.
- `npm run build` — passed.
- `git diff --check` — passed.

## Review and remaining work

- GitHub reports all three checks passing and requires at least one approving review; no review had been submitted in the supplied status snapshot.
- The PR description still has placeholders for local visual checks and the attached screenshot description. Replace those with the actual verification notes before review.
- The PR mentions [Toolbelt #302](https://github.com/codercops/toolbelt/pull/302), an unrelated Markdown Live Preview PR; it is not counted as the contributor's PR.

Update this file when the PR receives review, changes state, or merges. Move it into `contributions/` and assign the next contribution number only after merge.
