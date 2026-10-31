# codercops/chatcops Issue #460 — Widget: support CSP nonces for injected styles

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#460 — Widget: support CSP nonces for injected styles](https://github.com/codercops/chatcops/issues/460)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-29
- **Last updated:** 2026-10-30
- **Closed:** 2026-10-30
- **Labels:** `enhancement`, `hacktoberfest`
- **Linked pull request:** [#473 — feat(widget): support CSP nonces for styles](https://github.com/codercops/chatcops/pull/473) (merged)

## Problem

The widget injects `<style>` elements into its shadow roots for the launcher, chat panel, and pre-chat form. On sites with a strict Content Security Policy that blocks inline styles, those styles can be rejected, leaving the widget unstyled or unusable. This affects both the initial loader and styles added when the pre-chat form loads.

## Expected behavior and scope

Let the widget apply a host-provided CSP nonce to every style element it creates. For script-tag installs, it could use the nonce on the ChatCops script; ESM users should have a configuration option to provide one. Document the setup and add tests covering the loader, panel, and lazy pre-chat styles under a nonce-based policy. Keep the existing behavior unchanged when no nonce is configured.

## Tests or acceptance criteria

No explicit test checklist in the issue body.

## Discussion and current state

The maintainer assigned this issue to me and outlined nonce propagation through script-tag and ESM installs. It was completed by merged PR #473.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Widget
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
