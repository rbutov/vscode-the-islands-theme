# AGENTS.md

## Cursor Cloud specific instructions

### What this project is

This repo is **The Islands Theme**, a static VS Code / Cursor **color theme extension**
(a single product, not a monorepo). The whole "product" is three JSON theme files in
`src/` (`islands-dark.json`, `islands-light.json`, `islands-darcula.json`) registered via
`contributes.themes` in `package.json`. There is **no runtime code, server, API, database,
or background service** — nothing long-running to start.

### Commands

Standard commands live in `package.json` `scripts` and `.github/CONTRIBUTING.md`; use those.

- Lint/format: `npm run lint` (`prettier src --write`).
- Package/build: `npm run vsce-package` (produces `./bin/theme.vsix`).
- Publish: `npm run vsce-publish` (CI only; needs `VSCE_PUBLISHER_TOKEN`).

### Non-obvious caveats

- `npm run lint` runs `prettier --write`, so it **mutates the files in `src/`** in place.
  The committed theme JSON is not fully prettier-formatted, so a fresh `npm run lint`
  produces diffs. Revert those (`git checkout -- src/`) unless reformatting is the intent.
- `npm run vsce-package` does **not** create its output directory. If `bin/` is missing it
  fails with `ENOENT ... bin/theme.vsix`. Run `mkdir -p bin` first (`bin/` is gitignored).
- There is **no automated test suite**. Verification is manual/visual in an editor plus a
  successful `vsce package`.

### Running / testing the theme (GUI)

The only way to "run" this is to load it in a VS Code–family editor and pick a theme; there
is no headless run. No `code`/`cursor` CLI is preinstalled in the cloud VM, so to do a GUI
test you must install an editor (e.g. VS Code), then launch:

```
code --extensionDevelopmentPath=<repo-root> --user-data-dir=/tmp/vscode-user --no-sandbox <somefile>
```

Then Command Palette → `Preferences: Color Theme` → select `Islands Dark` / `Islands Light`
/ `Islands Darcula`.
