# OSS Contribution Journal

This journal records my open-source contributions, what I worked on, how
I approached each repository, review feedback, maintainer interactions,
and what I learned.

## Contribution Index

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  \#          Repository                                                                            Issue                                                               PR                                                                  Status      Main Skill
  ----------- ------------------------------------------------------------------------------------- ------------------------------------------------------------------- ------------------------------------------------------------------- ----------- ------------------
  1           [`pacocartones/free-llm-api-hub`](https://github.com/pacocartones/free-llm-api-hub)   [#67](https://github.com/pacocartones/free-llm-api-hub/issues/67)   [#198](https://github.com/pacocartones/free-llm-api-hub/pull/198)   Merged      Data
                                                                                                                                                                                                                                                        verification +
                                                                                                                                                                                                                                                        validation +
                                                                                                                                                                                                                                                        generated
                                                                                                                                                                                                                                                        artifacts + review

  2           [`codercops/chatcops`](https://github.com/codercops/chatcops)                         [#94](https://github.com/codercops/chatcops/issues/94)              [#104](https://github.com/codercops/chatcops/pull/104)              Merged into TypeScript/DOM +
                                                                                                                                                                                                                                            `dev`       tests +
                                                                                                                                                                                                                                                        changesets +
                                                                                                                                                                                                                                                        review

  3           [`codercops/chatcops`](https://github.com/codercops/chatcops)                         [#92](https://github.com/codercops/chatcops/issues/92)              [#120](https://github.com/codercops/chatcops/pull/120)              Merged /    CSS visibility +
                                                                                                                                                                                                                                            issue       accessibility +
                                                                                                                                                                                                                                            closed      manual
                                                                                                                                                                                                                                                        verification +
                                                                                                                                                                                                                                                        review
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Latest Milestone: ChatCops #92

**Result:** Issue #92 was closed as completed via PR #120, as confirmed
by the maintainer's GitHub notification on 12 October 2026.

The fix ensures that the inline chat panel is genuinely hidden when
`close()` is called, rather than merely transparent and non-interactive
to pointer events.

-   Removed forced `opacity: 1` and `pointer-events: auto` declarations
    so the `cc-visible` class controls inline-panel visibility.

-   Added a rule for the closed inline state:

    ``` css
    .cc-panel.cc-inline:not(.cc-visible) {
      visibility: hidden;
    }
    ```

-   Preserved the inline panel's layout and popup open/close animations.

-   Added a patch changeset for `@chatcops/widget`.

### Validation

-   `pnpm -r build` --- passed.
-   `pnpm test` --- 190 tests passed across 26 test files.
-   `pnpm -r typecheck` --- passed.
-   `git diff --check` / Git whitespace checks --- passed.
-   Manually verified the inline panel is visible on initial load,
    hidden after **Close panel**, and restored after **Open panel**.
-   The maintainer independently confirmed that the closed panel was
    hidden and could not be focused.
-   Added screenshots of the open and closed states to the PR
    description.

### Review and lessons learned

The maintainer identified an accessibility issue in the initial
approach: `opacity: 0` and `pointer-events: none` alone do not remove
hidden controls from keyboard navigation or reliably hide them from
screen readers. I added `visibility: hidden` for the closed inline
state, then the maintainer verified the fix.

This contribution reinforced that UI behavior must be checked beyond
visual appearance, including keyboard focus and accessibility. It also
highlighted the importance of providing screenshots and completing all
required PR-template sections, including the AI-assistance disclosure.

**AI assistance disclosure:** I used ChatGPT for debugging guidance,
understanding CSS visibility and focus behavior, and planning
validation. I reviewed and applied the code changes, ran the build,
tests, and type checks, and manually verified the widget behavior.

Detailed record: [Contribution #3 --- ChatCops
#92](contributions/003-chatcops-92.md).

## Previous Milestone: ChatCops #94

**Result:** PR #104 was approved by Anurag Verma and merged into `dev`.

The change aligns the widget's client-side input limits with the
server's `chatRequestSchema` limits:

-   Pre-chat text inputs and textareas: 500 characters.
-   Chat message textarea: 10,000 characters.
-   Added tests for the two limits and a patch changeset for
    `@chatcops/widget`.

Validation completed successfully:

-   `pnpm -r build`
-   `pnpm test` --- 170 tests passed across 25 test files.
-   `pnpm -r typecheck`
-   Focused widget tests --- 17 tests passed across 2 files.
-   `git diff --check`

I also tested the widget's message flow with a temporary local mock SSE
backend because I did not have, and did not want to use, a paid
AI-provider API key. The mock confirmed that the widget could receive a
simulated response for a normal message and for a 10,000-character
message. This was a mock-backend test, not a live AI-provider
integration test.

## Programs & Community Milestones

### Social Winter of Code (SWoC) --- Season 7, Winter 2026--27

-   **Date:** 11 October 2026
-   **Milestone:** Received an email stating that I had been selected as
    a SWoC contributor.
-   **Record status:** Selection email received; official roster/badge
    confirmation still to be checked.
-   **Important distinction:** This is program participation, not a code
    contribution. Individual SWoC PRs should be added to the
    contribution index only when they are actually opened and merged.
-   **Next actions:** Verify my GitHub username on the [official SWoC
    badge page](https://www.swoc.in/badge), join the [official
    Discord](https://discord.com/invite/eHkSQYnamb) from the official
    website, review project rules, and track merged PRs.
-   **Official season:** Winter 2026--27; the official website lists
    registration closing on 31 December 2026 and the coding period as 1
    January--30 March 2027.
-   **Certificate target:** The official website states that at least
    two PRs must be merged during the coding period for a verified
    certificate.

Detailed checklist: [SWoC Season 7 participation
plan](programs/001-swoc-season-7-2026-27.md).

## How I Will Use This Journal

For every contribution, record:

1.  Repository and issue
2.  Problem and requirements
3.  My understanding
4.  Files changed
5.  Implementation/solution
6.  Tests and validation
7.  Git workflow
8.  PR and review feedback
9.  Maintainer interaction
10. What I learned
11. What I could improve
12. Final result

The goal is not to maximize PR count. The goal is to become capable of
making meaningful contributions independently.
