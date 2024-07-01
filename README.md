# README

This repository contains a centralized Prettier configuration that can be used across multiple projects. The configuration is defined in `config/index.json`.

## Getting Started

To use this configuration in your project, first install it as a dev dependency:

```bash
npm install --save-dev @manuelstolze/prettier-config
```

Then, reference it in your `package.json`:

```json
{
  "prettier": "@manuelstolze/prettier-config"
}
```

Or, if you prefer, you can create a `.prettierrc.js` file in the root of your project and export the configuration:

```javascript
module.exports = require("@manuelstolze/prettier-config");
```

## Configuration

The current configuration is as follows:

```json
{
  "singleQuote": false,
  "jsxSingleQuote": false,
  "printWidth": 100,
  "proseWrap": "always",
  "tabWidth": 2,
  "useTabs": false,
  "trailingComma": "none",
  "semi": true,
  "arrowParens": "always"
}
```

This configuration can be overridden by adding a `.prettierrc.js` file in your project and merging it with the base configuration:

```javascript
const baseConfig = require("@manuelstolze/prettier-config");

module.exports = {
  ...baseConfig,
  // your overrides here
};
```
