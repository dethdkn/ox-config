<h1 align="center">@dethdkn/ox-config</h1>
<p align="center">⚓️ My Opinionated OX Config</p>

<p align="center">
   <a href="https://rosa.dev.br">
      <img src="https://img.shields.io/badge/check me!-👻-F28AA9" alt="rosa.dev.br"/>
   </a>
   <a href="https://github.com/dethdkn/ox-config/blob/main/LICENSE">
      <img src="https://img.shields.io/github/license/dethdkn/ox-config?color=%233da639&logo=open%20source%20initiative" alt="License"/>
  </a>
   <a href="https://gitmoji.dev">
      <img src="https://img.shields.io/badge/gitmoji-%20😜%20😍-FFDD67" alt="Gitmoji"/>
   </a>
</p>

## 🚀 Setup

1. Install with your favorite package manager:
   - **bun** : `bun add -D @dethdkn/ox-config`
   - npm : `npm i -D @dethdkn/ox-config`
   - pnpm : `pnpm add -D @dethdkn/ox-config`
   - yarn : `yarn add -D @dethdkn/ox-config`

2. Create a `.oxfmtrc.json` file in the project root and copy the configuration from [github.com/dethdkn/ox-config/.oxfmtrc.json](https://github.com/dethdkn/ox-config/blob/main/.oxfmtrc.json).

3. Create a `.oxlintrc.json` in the project root:

```json
{
  "extends": ["./node_modules/@dethdkn/ox-config/.oxlintrc.json"]
}
```

4. Add lint scripts to `package.json`:

```json
{
  "scripts": {
    "fmt": "oxfmt --check",
    "fmt:fix": "oxfmt",
    "lint": "oxlint --type-aware",
    "lint:fix": "oxlint --type-aware --fix"
  }
}
```

4. Install the [OXC VS Code extension](https://marketplace.visualstudio.com/items?itemName=oxc.oxc-vscode).

5. Add the following configuration to `.vscode/settings.json`:

```json
{
  // Use OXC as the default code formatter in VSCode
  "editor.defaultFormatter": "oxc.oxc-vscode",

  // Automatically format files whenever you save them
  "editor.formatOnSave": true,

  // Apply OXC auto-fix actions on save (only when explicitly configured)
  "editor.codeActionsOnSave": {
    "source.fixAll.oxc": "explicit"
  },

  // Enable type-aware linting
  "oxc.typeAware": true,

  // Run OXC linter automatically on type
  "oxc.lint.run": "onType"
}
```

## 📝 License

Copyright © 2026 [Gabriel 'DethDKN' Rosa](https://github.com/dethdkn)\
This project is under [MIT license](https://github.com/dethdkn/ox-config/blob/main/LICENSE)
