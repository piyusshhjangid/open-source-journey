# PR History — codercops/chatcops #353

## GitHub record

- **Pull request:** [#353 — fix(widget): keep focus inside popup chat](https://github.com/codercops/chatcops/pull/353)
- **Status:** Closed without merge
- **Current outcome:** Not counted as a merged contribution

## Purpose

Closes #335

Keeps keyboard focus inside the open popup chat. Tab from the last focusable element wraps to the first, and Shift+Tab from the first wraps to the last. Focusable elements are recalculated on each key press, so controls added or removed during the chat are handled.

Adds `aria-modal="true"` to the popup dialog and uses the shadow root’s active element for focus checks. Inline mode and closed popups remain unaffected. Includes a patch changeset for `@chatcops/widget`.

Also fixes Windows lint path handling, limits coverage inputs to TypeScript source files, and increases timeouts for slower provider imports and Miniflare tests.

## Validation recorded in the PR

- Full Vitest coverage run — passed: 1,224 tests passed, 28 skipped, no type errors.
- Popup panel tests — passed: 14 tests.
- Biome check — exited successfully; existing warnings and informational diagnostics remain.
- Size check — passed; panel is 13.34 kB gzipped against the 14 kB budget.
- `astro build` — passed.
- `git diff --check` — passed.

## Follow-up

PR #353 closed without merge. The updated implementation was merged upstream as PR #356; count the merged replacement once.

This history record preserves the attempt and avoids double-counting work that was later merged through the upstream PR.
