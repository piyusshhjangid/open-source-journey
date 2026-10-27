# PR History — piyusshhjangid/chatcops #2

## GitHub record

- **Pull request:** [#2 — feat(widget): add French locale](https://github.com/piyusshhjangid/chatcops/pull/2)
- **Status:** Closed without merge
- **Current outcome:** Not counted as a merged contribution

## Purpose

Part of #55

Adds a complete French (fr) widget locale with French accents and punctuation, preserving all placeholders. Adds French to the widget's Available Locales table and includes a patch changeset for @chatcops/widget.

## Validation recorded in the PR

- vite build
- vite build -c vite.panel.config.ts — builds dist/locales/fr.js
- vite build -c vite.loader.config.ts
- tsc --emitDeclarationOnly
- vitest run — 379 tests passed
- tsc --noEmit
- node scripts/check-doc-samples.mjs — 111 checked, 1 skipped
- git diff --check

## Follow-up

The fork-side PR was closed without merging. The French locale was submitted to the upstream repository and merged as PR #371. Count the upstream merge once.

This history record preserves the attempt and avoids double-counting work that was later merged through the upstream PR.
