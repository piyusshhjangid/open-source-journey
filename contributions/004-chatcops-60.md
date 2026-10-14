# OSS Contribution #4 — ChatCops Widget Accessibility and Reduced Motion

## Repository

- **Repository:** [`codercops/chatcops`](https://github.com/codercops/chatcops)
- **Issue:** [#60 — Add focus-visible styles and respect `prefers-reduced-motion`](https://github.com/codercops/chatcops/issues/60)
- **Pull Request:** [#131 — fix(widget): improve accessibility and reduced motion](https://github.com/codercops/chatcops/pull/131)
- **Branch:** `fix/widget-accessibility-motion`
- **Commit:** `e6ad46f` — `fix(widget): improve accessibility and reduced motion`
- **Merge commit:** `19d4d7a`
- **Status:** Approved and merged into `dev`; issue addressed
- **Label:** `hacktoberfest-accepted`
- **Date:** October 2026

## 1. Problem and requirements

The widget needed clearer keyboard-focus indicators and better support for users who request reduced motion. The issue called for visible `:focus-visible` styles and honoring `prefers-reduced-motion: reduce`.

## 2. Implementation

### Keyboard focus

Added consistent accent-colored `:focus-visible` outlines using `var(--cc-accent)` to the launcher/FAB, header close button, send button, retry/regenerate controls, bubble close control, and pre-chat submit control.

### Keyboard and touch behavior

Kept the regenerate action visible when its message receives keyboard focus and on devices without hover support, so the action is not dependent on mouse hover alone.

### Reduced motion

Added reduced-motion behavior to disable the FAB pulse, typing-dot animation, and panel/bubble transitions when `prefers-reduced-motion: reduce` is active.

### Release metadata

Added a patch changeset for `@chatcops/widget`.

## 3. Validation

The PR record reports:

- `pnpm --filter @chatcops/widget build` — passed.
- `pnpm --filter @chatcops/widget exec vitest run` — 115 tests passed across 10 test files.
- `pnpm -r typecheck` — passed for core, widget, and server.
- `git diff --check` — passed.
- Manually checked keyboard focus indicators in the development widget.
- Enabled `prefers-reduced-motion: reduce` in Chrome DevTools and verified the media query matched and the relevant animations/transitions were disabled.
- Three GitHub checks passed before merge.

**Testing limitation:** The development widget's chat backend was unavailable (`ERR_CONNECTION_REFUSED`) during visual testing. This blocked successful chat requests but did not prevent checking focus styles or reduced-motion behavior. The PR description also explicitly noted that `pnpm -r build` and `pnpm test` were not run in the final validation for this PR; do not claim those commands passed for this contribution.

## 4. Maintainer review

Anurag629 approved the changes and reported independently testing the widget with the keyboard in Chrome alongside a build of `dev`. The maintainer confirmed that the original launcher had no visible focus ring and Regenerate stayed invisible when focused; the branch added accent outlines to all seven buttons, exposed Regenerate on focus and touch devices, and disabled the specified animations/transitions under reduced motion. The maintainer stated that the change covered every point in the issue and merged it.

## 5. What I learned

- Keyboard accessibility requires visible focus indicators, not just clickable controls.
- Hover-only controls can be difficult or impossible to discover on touch devices and with keyboard navigation.
- Reduced-motion preferences should be applied to all relevant motion, not only one animation.
- Manual browser verification can validate CSS behavior even when a backend is unavailable, but backend-dependent behavior must be reported as untested.
- PR descriptions should distinguish checks that passed from checks that were not run.

## 6. Final result

| Item | Result |
|---|---|
| Issue | #60 |
| PR | #131 |
| Maintainer approval | Yes |
| Merged into | `dev` |
| Build | Widget build passed |
| Widget tests | 115/115 passed across 10 files |
| Typecheck | Passed |
| Full `pnpm test` / workspace build in final validation | Not run for this PR |
| Manual accessibility/reduced-motion checks | Completed |
| Changeset | `@chatcops/widget`: patch |
| GitHub checks | 3 passed |

**Contribution #4 complete.**
