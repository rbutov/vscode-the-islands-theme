# Change Log

All notable changes to "The Islands Theme" extension will be documented in this file.

## 1.2.0 (2026-08-09)

- Re-synced against current JetBrains Islands theme sources (`ManyIslandsDark` / `Light` / `Darcula`); core palette unchanged since June 2026
- **Islands Light** readability fixes:
  - Corrected near-invisible UI tokens (`activityBarTop`, badges, selected tabs)
  - Removed dark leftovers in merge editor, stack-frame highlight, and warning validation
  - Improved low-contrast syntax (HTML/CSS tags, Vue components, SCSS comments, CSS URLs)
  - Aligned bracket highlight colors with the Light editor scheme
- Expanded modern workbench coverage (widget border, chat bubbles, gauges, profiles sash)
- Restored marketplace README screenshot; fixed recommended settings JSON example
- Updated `prettier` to 3.9.6 and refreshed transitive packaging dependencies (npm audit clean)

## 1.1.0 (2026-07-16)

- Renamed extension to **The Islands Theme** (`the-islands-theme`)
- Added three JetBrains Islands variants in the theme picker:
  - **Islands Dark** — from `ManyIslandsDark.theme.json` + `IslandSchemeDark.xml`
  - **Islands Light** — from `ManyIslandsLight.theme.json` + Light editor scheme
  - **Islands Darcula** — from `ManyIslandsDarcula.theme.json` + classic Darcula scheme
- Repository moved to https://github.com/rbutov/vscode-the-islands-theme

## 1.0.0 (2026-07-15)

- Initial release: Islands Dark Theme for VS Code / Cursor
- UI colors mapped from JetBrains Islands Dark (`ManyIslandsDark.theme.json`)
  - Main window chrome `#26282C`, editor / tool islands `#191A1C`
  - Active tabs `#233558` with border `#2E4D89`, selection `#2A4371`
  - Transparent status / activity bar borders for Islands-style chrome
- Syntax highlighting aligned with `IslandSchemeDark.xml`
  - Keywords, strings, numbers, functions, fields, comments, HTML tags, etc.
  - Language leftovers from Darcula (PHP / Go / Ruby / SCSS) normalized to the Islands palette
- Modern workbench coverage for release
  - Sticky scroll, terminal selection / find, sash hover
  - Chat / inline chat, testing, notebook, SCM graph, comments
  - Diff unchanged regions, multi-diff, banners, ghost text
