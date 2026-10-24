# OSS Contribution #3 --- ChatCops Inline Panel Visibility

## Repository

-   **Repository:**
    [`codercops/chatcops`](https://github.com/codercops/chatcops)
-   **Technology:** CSS / TypeScript widget / DOM / accessibility
-   **Issue:** [#92 --- Hide the inline chat panel when `close()` is
    called](https://github.com/codercops/chatcops/issues/92)
-   **Pull Request:**
    [#120](https://github.com/codercops/chatcops/pull/120)
-   **Branch:** `fix/inline-close-panel`
-   **Commits:** `8da2d3f` ---
    `fix(widget): hide inline panel when closed`; `ce8564a` ---
    `fix(widget): hide closed inline panel from focus`
-   **Status:** PR #120 is merged into `codercops:dev` and issue #92 is closed as completed.
-   **Date completed:** 12 October 2026

------------------------------------------------------------------------

## 1. Problem

In inline mode, calling `close()` left the panel visually present or not
fully hidden. Removing opacity and pointer-event overrides allowed the
`cc-visible` class to control its visible state, but the closed panel
could still remain in the keyboard tab order and be exposed to screen
readers.

## 2. Requirements

The issue asked for the inline panel to hide when `close()` is called,
while preserving existing layout and popup open/close animations. The
maintainer also requested screenshots or a short before/after recording
from inline mode and completion of the PR template's AI-assistance
section.

## 3. Implementation

### CSS behavior

Removed the forced `opacity: 1` and `pointer-events: auto` declarations
from the inline panel CSS so the `cc-visible` class could control
visibility.

Added this closed-state rule in `packages/widget/src/styles/widget.css`:

``` css
.cc-panel.cc-inline:not(.cc-visible) {
  visibility: hidden;
}
```

This makes the closed inline panel invisible and prevents its hidden
controls from being focused. The popup animation behavior and inline
layout were preserved.

### Changeset

Added a patch changeset for `@chatcops/widget`, as requested by the
issue.

## 4. Validation

The following checks passed:

``` bash
pnpm -r build
pnpm test
pnpm -r typecheck
git show --check --oneline HEAD
```

-   Workspace build --- passed.
-   Full test suite --- **190 tests passed across 26 test files**.
-   Type checking --- passed.
-   Git whitespace/diff checks --- passed.
-   Manual verification: inline panel visible on initial load, hidden
    after clicking **Close panel**, and restored after clicking **Open
    panel**.
-   Popup open/close animations were manually checked and remained
    unchanged.

The maintainer independently tested inline mode and confirmed that the
panel was hidden after `close()`, could not be focused, and returned
after `open()`.

## 5. Screenshots

-   **Open state:** [View
    screenshot](https://github.com/user-attachments/assets/6da7350b-b2b4-449a-bdb9-58729cccd019)
-   **Closed state:** [View
    screenshot](https://github.com/user-attachments/assets/de6fc56a-c1a5-47b3-ab6c-b1cdb680d886)

These screenshots were added to the PR description as manual
verification evidence.

## 6. Review Feedback

The maintainer agreed that removing the CSS overrides was the correct
first step, but pointed out that `opacity: 0` and `pointer-events: none`
do not remove the hidden panel from keyboard navigation or screen-reader
exposure. I added `visibility: hidden` for the closed inline state and
asked the maintainer to review again.

The maintainer confirmed that the fix worked. After the requested
AI-assistance section was added to the PR description, issue #92 was
closed as completed via PR #120.

## 7. AI Assistance Disclosure

I used ChatGPT for debugging guidance, understanding CSS visibility and
focus behavior, and planning validation. I reviewed and applied the code
changes, ran the build, tests, and type checks, and manually verified
the widget behavior.

## 8. What I Learned

### CSS and accessibility

-   `opacity: 0` makes an element transparent but does not remove it
    from keyboard focus order.
-   `pointer-events: none` affects pointer interaction, not keyboard
    focus by itself.
-   A visually hidden component must be evaluated for keyboard
    navigation and assistive-technology exposure as well as appearance.

### Testing and review

-   Manual verification should cover initial state, close state, and
    reopen state.
-   Screenshots make visual behavior easier for maintainers to verify.
-   Reviewer feedback can expose accessibility requirements that aren't
    obvious from a visual check alone.
-   PR descriptions should include every required section and accurately
    disclose AI assistance.

### Contribution workflow

-   Read the issue's contribution instructions before starting.
-   Comment on an issue and wait for assignment before opening a PR.
-   Follow the repository's one-issue-at-a-time guidance.
-   Keep validation results and manual testing claims specific and
    reproducible.

## 9. Final Result

  Item                       Result
  -------------------------- --------------------------------
  Issue                      #92
  PR                         #120
  Maintainer verification    Confirmed fix works
  PR                         #120 merged into `dev`
  Issue                      #92 closed as completed
  Build                      Passed
  Full test suite            190/190 passed across 26 files
  Typecheck                  Passed
  Git checks                 Passed
  Open/closed screenshots    Added to PR description
  AI assistance disclosure   Added

**Contribution #3 complete; PR #120 merged and issue #92 closed.**
