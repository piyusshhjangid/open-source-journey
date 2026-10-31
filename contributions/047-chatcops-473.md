# OSS Contribution #47 — chatcops PR #473: feat(widget): support CSP nonces for styles

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Closes #460](https://github.com/codercops/chatcops/issues/460) (closed).
- **Pull request:** [#473 — feat(widget): support CSP nonces for styles](https://github.com/codercops/chatcops/pull/473)
- **Target branch:** `dev`
- **Merge commit:** `d2494daed93448153c8fd2add9c2d845ef472778`
- **Status:** Merged
- **Date merged:** 2026-10-30 (UTC)

## 1. Problem and requirements

Adds CSP nonce support for every widget-injected style. Script-tag installs read the nonce from their own script element; ESM and programmatic installs can set `nonce` in `WidgetConfig`. Documents the setup and adds unit and browser coverage under a nonce-only `style-src` policy.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- `pnpm --filter @chatcops/widget test` — 687 passed.
- `pnpm --filter @chatcops/widget typecheck` — passed.
- `pnpm e2e --grep "script nonce allows"` — passed.
- `pnpm size` — passed; panel is 16.65 kB gzipped against an 18 kB limit.
- Changed-file Biome check and `git diff --check` — passed.

The full docs sample check reports existing errors in unrelated workspace docs/packages. On Windows, the package build script’s final `rm -f` step is unsupported; the Vite builds and standalone widget declaration build passed.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Security policy support must cover every dynamically injected style and be verified in a browser under the actual policy.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#460](https://github.com/codercops/chatcops/issues/460) (closed) |
| Pull request | [#473](https://github.com/codercops/chatcops/pull/473), merged |
| Merge target | `dev` |
| Merge date | 2026-10-30 |
| Validation | PR-reported results summarized above |

**Contribution #47 complete.**
