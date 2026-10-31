# In-Progress PR — codercops/chatcops #539: fix(widget): ignore invalid consent attributes

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#536 — linked issue](https://github.com/codercops/chatcops/issues/536)
- **Pull request:** [#539 — fix(widget): ignore invalid consent attributes](https://github.com/codercops/chatcops/pull/539)
- **Target branch:** `dev`
- **Status:** Open
- **Last checked:** 1 November 2026
- **Review state:** CHANGES_REQUESTED

## 1. Problem and requirements

Closes #536

- Parse script-tag `data-wait-for-consent` as `"true"`, `"false"`, or the existing empty-attribute shorthand.
- Ignore other non-empty values so typos do not unexpectedly enable consent gating.
- Document the accepted values and add a patch changeset for `@chatcops/widget`.

## 2. Implementation

The PR description and current GitHub diff contain the detailed implementation. This record summarizes the authored PR and live review state without treating unmerged work as a completed contribution.

## 3. Validation

- Widget consent tests — 45 passed.
- Widget typecheck — passed.
- Widget ESM, panel, and loader Vite builds — passed.
- Widget declaration build — passed.
- Docs sample check — passed (190 TypeScript blocks checked, 4 skipped).
- Biome check for changed files — passed.
- `size-limit` — passed; loader 4.84/5 kB, panel 18.79/19 kB, single file 22.09/23 kB gzipped.
- `git diff --check` — passed.

Corepack could not download pnpm because network DNS was unavailable, so I ran the installed local tools directly.

## 4. Maintainer review

Changes requested. Maintainer says consent handling must fail closed: only `false` disables the wait; invalid values should continue to wait and produce a console warning. The maintainer also requested correcting the linked issue reference to #536. The PR body currently says `Closes #536`; verify this remains correct after revisions.

## 5. What remains

Preserve fail-closed consent behavior, warn on invalid values, align tests/docs with maintainer guidance, then request review again.

## 6. Current result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#536](https://github.com/codercops/chatcops/issues/536) |
| Pull request | [#539](https://github.com/codercops/chatcops/pull/539), open |
| Review state | CHANGES_REQUESTED |
| Next action | Preserve fail-closed consent behavior, warn on invalid values, align tests/docs with maintainer guidance, then request review again. |

This PR is not included in the merged contribution total.
