# Changelog

## [3.1.0] - 2026-11-18

### Changed
- `brand.json` `semi` is `">=0.26.0 <1.0.0"` (was `^0.20.0`): the range covers @semi/ui v0.26 and later 0.x minors. Plugins older than v0.27.0 do not parse this form and read it as uncapped; no 1.x tag exists, so that is safe. From v0.27.0 `satisfies` and the `semi-brand` validator accept it.
- Dev dependency @semi/ui is `github:hoanghuynh296/semi-nextjs-codebase#v0.27.0` (the first release that validates this range); `dist/` regenerated with `npm run build` (only the @semi/ui version stamps and the `semi` range change). v0.27.0 adds the runtime dependency `uqr`, now in the lock file.

### Checked
- @semi/ui 0.21.0 to 0.27.0 changelog: no change to token names, the `brand.json` schema or `semi-brand build` output. No colour, font, logo or voice change.

### Fixed
- Dev dependency `next` is `^16.4.6` (was resolved at 16.4.3, flagged by GHSA-mfr8-8qww-v76h and GHSA-vc7v-qv4w-wrv8, range 16.2.0-16.4.4), so `semi-brand site` (the `brand-pages` build) runs again.
