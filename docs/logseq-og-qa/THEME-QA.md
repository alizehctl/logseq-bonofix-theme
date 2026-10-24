# Logseq OG light table-header contrast fix

## Environment
- Logseq OG 1.0.0 (Electron 38.4.0), macOS
- Theme: Bonofix Theme, light palette, accent colour disabled for QA

## Problem
Table headers are `#9f9f9f` on white, about 2.65:1. They are hard to read in
the light palette.

## Fix
Use the theme's primary text colour for table headers:

```css
html[data-theme] .block-content table th {
  color: var(--ls-primary-text-color) !important;
}
```

## Verification
Before/after: `docs/logseq-og-qa/bonofix-table.png`.
