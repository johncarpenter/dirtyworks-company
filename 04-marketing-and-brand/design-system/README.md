# Design system

## Scope

- `guidelines/` — approved visual and interaction rules.
- `tokens/` — reusable machine-readable color, typography, spacing, surface and motion values.
- `assets/source/` — approved editable masters suitable for Git; large binaries may instead be indexed in controlled asset storage.
- `assets/exports/` — approved reusable web, print and presentation derivatives.
- `components/` — reusable component specifications and reference implementations that are not application runtime code.
- `templates/` — reusable brand production templates.
- `licenses/` — font, stock, icon and other usage/provenance records.
- `releases/` — immutable release manifests and migration notes.

## Consumption rule

Every application records the design-system release or commit it consumes. A copied snapshot must be labelled as derived and must not silently become a competing source of truth.

