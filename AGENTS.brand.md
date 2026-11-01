<!-- semi-brand:start -->
## Brand: 3dnoobs (`@3dnoobs/brand`)

This product belongs to the **3dnoobs** brand. Its colours, fonts and allowed styles come only from `@3dnoobs/brand`
(`node_modules/@3dnoobs/brand/BRAND.md`).

- Never define brand colours or override Semi tokens in this app (`--color-primary-*`, `--semi-*`, `@theme` colours,
  hex values): `semi-lint` blocks it (`brand-override`). Use the semantic tokens (`bg-accent`, `text-accent-fg`,
  `bg-panel` …).
- Style: `flat`, `soft` only (`data-style` on `<html>`, `"style"` in `semi-lint.json`, switch with `/semi-style`).
- Fonts: Geist + Montserrat Alternates, loaded with `next/font` in the root layout (`--font-geist`, `--font-montserrat-alternates`).
- A change to the brand happens in the brand repo (`/semi-brand`), then `/semi-update` here.
<!-- semi-brand:end -->
