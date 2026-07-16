# Change Log

All notable changes to the "islands-dark-theme" extension will be documented in this file.

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
