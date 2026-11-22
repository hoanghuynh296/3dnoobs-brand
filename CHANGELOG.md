# Changelog

## [3.2.0] - 2026-11-22

### Changed
- Built on Semi v0.35.0: `brand.json` `semi` is `">=0.35.0 <1.0.0"` (was `">=0.26.0 <1.0.0"`); dev dependency @semi/ui is `github:hoanghuynh296/semi-nextjs-codebase#v0.35.0` (was v0.27.0); `dist/` and BRAND.md rebuilt.
- **Per-theme accent** (group decision C-024, ds#84): light theme uses shade 600 (`#008509`, on-accent `#ffffff`), dark theme shade 400-500 (`#539f50`, on-accent `#0c0d0e`, hover `#81b67d`). Before, both themes used `#008509`.
- **Flat light app step** `#ffffff` -> `#f9faf8` (panel stays `#ffffff`) (ds#88).
- Success status is turned 20 degrees away from the primary (`#28A25A` -> `#00a081`) so it no longer reads as the accent; `brand.css` overrides `--semi-success-*` in both themes.

### Visible changes
- Dark theme: the primary button is lighter green with dark text. Light theme accent is unchanged. Flat light pages get a faint green-grey background instead of pure white. Success badges and text shift towards teal. Readability table: 26/26 pairs pass AA.


## [3.1.0] - 2026-11-18

### Changed
- `brand.json` `semi` is `">=0.26.0 <1.0.0"` (was `^0.20.0`): the range covers @semi/ui v0.26 and later 0.x minors. Plugins older than v0.27.0 do not parse this form and read it as uncapped; no 1.x tag exists, so that is safe. From v0.27.0 `satisfies` and the `semi-brand` validator accept it.
- Dev dependency @semi/ui is `github:hoanghuynh296/semi-nextjs-codebase#v0.27.0` (the first release that validates this range); `dist/` regenerated with `npm run build` (only the @semi/ui version stamps and the `semi` range change). v0.27.0 adds the runtime dependency `uqr`, now in the lock file.

### Checked
- @semi/ui 0.21.0 to 0.27.0 changelog: no change to token names, the `brand.json` schema or `semi-brand build` output. No colour, font, logo or voice change.

### Fixed
- Dev dependency `next` is `^16.4.6` (was resolved at 16.4.3, flagged by GHSA-mfr8-8qww-v76h and GHSA-vc7v-qv4w-wrv8, range 16.2.0-16.4.4), so `semi-brand site` (the `brand-pages` build) runs again.
