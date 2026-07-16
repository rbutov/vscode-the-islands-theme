# Islands Dark Theme for VS Code

The **Islands Dark Theme** brings the soft, layered look of [JetBrains Islands](https://blog.jetbrains.com/platform/2025/12/meet-the-islands-theme-the-new-default-look-for-jetbrains-ides/) — the new default appearance across JetBrains IDEs — to Visual Studio Code and Cursor.

Dark chrome frames darker editor and tool-window islands, with clearer active tabs and syntax colors taken from the official Islands Dark editor scheme.

## Features

- **Islands Dark only** — faithful dark port of the JetBrains Islands palette
- **Layered UI** — lighter main-window chrome (`#26282C`) around darker editor / sidebar / panel islands (`#191A1C`)
- **Clear active tabs** — blue-tinted selection (`#233558`) so the focused file stands out
- **JetBrains syntax** — keywords, strings, functions, and comments matching Islands Dark
- **Modern workbench** — sticky scroll, terminal, chat / inline chat, testing, notebook, and SCM graph colors
- **Broad language coverage** — JavaScript, TypeScript, PHP, Go, Ruby, GraphQL, and more

## Color Palette

Mapped from JetBrains `ManyIslandsDark.theme.json` and `IslandSchemeDark.xml`:

| Role | Color |
| --- | --- |
| Editor / tool windows | `#191A1C` |
| Main window chrome | `#26282C` |
| Popups / lookups | `#27282B` |
| Foreground | `#BCBEC4` |
| Selection | `#2A4371` |
| Active tab | `#233558` / border `#2E4D89` |
| Keywords | `#CF8E6D` |
| Strings | `#6AAB73` |
| Numbers | `#2AACB8` |
| Functions | `#56A8F5` |
| Fields / properties | `#C77DBB` |
| Comments | `#7A7E85` |
| Accent | `#3871E1` |

## Installation

1. Open **Extensions** in VS Code (or Cursor).
2. Search for `Islands Dark Theme`.
3. Click **Install**.
4. Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`), choose **Preferences: Color Theme**, and select **Islands Dark**.

### From VSIX

```bash
npm install
npm run vsce-package
code --install-extension ./bin/theme.vsix
```

## Recommended Editor Settings

```json
{
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontLigatures": true,
  "editor.bracketPairColorization.enabled": false,
  "workbench.iconTheme": "vscode-jetbrains-icon-theme-2023-dark"
}
```

## Development

1. Clone this repository.
2. Run `npm install`.
3. Press `F5` (or use **Launch Theme**) to open an Extension Development Host.

## Issues and Feedback

Report bugs or ideas in the [GitHub repository](https://github.com/rbutov/vscode-islands-dark-theme).

## License

Released under the [MIT License](LICENSE).

---

Inspired by the JetBrains Islands theme. Not affiliated with JetBrains.
