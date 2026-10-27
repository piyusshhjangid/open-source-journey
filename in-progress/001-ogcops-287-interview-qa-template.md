# In-Progress PR — OGCops #287: Interview Q&A quote card

## Repository

- **Repository:** [codercops/ogcops](https://github.com/codercops/ogcops)
- **Issue:** [#285 — Add the Interview Q&A quote template](https://github.com/codercops/ogcops/issues/285) (open)
- **Pull request:** [#287 — feat(templates): add interview Q&A quote card](https://github.com/codercops/ogcops/pull/287)
- **Target branch:** `dev`
- **Status:** Open; changes requested
- **Last checked:** 27 October 2026

## 1. Problem and requirements

The linked issue requests an interview template with a question and answer, optional speaker name and role, site attribution, and readable rendering across light and dark backgrounds.

## 2. Implementation

The PR adds the `quote-interview` template. The question uses an accent Q mark, the answer uses an A mark, and speaker details sit opposite the site name. Whitespace-only optional values are hidden; long text shrinks and truncates; light-background accent text is darkened. The template is exported and registered, with focused rendering and optional-field coverage.

## 3. Validation

The PR reports:

- `npm run check` — passed with 0 errors and 0 warnings.
- `npm run test -- --testTimeout 15000` — 1,427 tests passed across 69 files.
- `npm run build` — passed.
- `git diff --check` — passed.
- Local editor verification checked the default dark design and a white background with pale-yellow accent.

The maintainer also reports checks, all 1,427 tests, and build passing on top of `dev`.

## 4. Maintainer review

The latest review requests two changes:

1. Truncate or shrink a long site name so it stays inside the card when the author and role are also long.
2. Hide the answer's top divider when the question is empty.

The PR is not approved yet. The linked issue remains open.

## 5. What remains

Address both review comments, rerun relevant checks, update the PR, and request another review.

## 6. Current result

| Item | Result |
|---|---|
| Repository | `codercops/ogcops` |
| Linked issue | [#285](https://github.com/codercops/ogcops/issues/285), open |
| Pull request | [#287](https://github.com/codercops/ogcops/pull/287), open |
| Review state | Changes requested |
| Next action | Fix long site-name overflow and remove the divider when the question is absent |

This PR is not included in the merged contribution total.
