# Changelog

## [3.1.0] - 2026-11-18

### Changed
- `brand.json` `semi` is `^0.26.0` (was `^0.20.0`): apps of this brand can use @semi/ui v0.26.x and later 0.x minors. `^0.26.0` is the form `/semi-sync` parses in v0.26.1 (`satisfies` reads `^`, `~` or an exact version; `>=0.26.0 <1.0.0` would be treated as "no cap").
- Dev dependency @semi/ui is `github:hoanghuynh296/semi-nextjs-codebase#v0.26.1`; `dist/` regenerated with `npm run build` (only the @semi/ui version stamps and the `semi` range change).

### Checked
- @semi/ui 0.21.0 to 0.26.1 changelog: no change to token names, the `brand.json` schema or `semi-brand build` output. No colour, font, logo or voice change.
