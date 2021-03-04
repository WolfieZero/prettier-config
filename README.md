# @wolfiezero/prettier-config [![current version](https://img.shields.io/npm/v/@wolfiezero/prettier-config.svg?style=flat-square)][projectnpm]

Sharable config for [Prettier][prettier]

## Installation

Install this config then run [install-peerdeps][ipeerdeps] to get dependencies
as development dependencies.

```
npm install @wolfiezero/prettier-config -D
npx install-peerdeps @wolfiezero/prettier-config --D
```

Then add the following line to your package.json file.

```json
{
  "prettier": "@wolfiezero/prettier-config"
}
```

## Extending

If you wish to customise [options][prettieroptions] further, remove the `pettier`
config from package.json and create a prettier file (`/.prettierrc.js`) with the
following.

```js
module.exports = {
  ...require('@wolfiezero/prettier-config'),
  tabs: true,
  tabWidth: 4,
};
```

## VSCode User?

Make sure you have [Prettier extention][prettiervscode] installed and add the
following into the project's settings file (`/.vscode/settings.json`) (deleting
as appropriate).

```json
{
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "typescript.format.enable": false,
  "editor.formatOnSave": true
}
```

[projectnpm]: https://www.npmjs.com/package/@wolfiezero/prettier-config
[prettier]: https://prettier.io/
[prettieroptions]: https://prettier.io/docs/en/options.html
[prettiervscode]: https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
[ipeerdeps]: https://www.npmjs.com/package/install-peerdeps
