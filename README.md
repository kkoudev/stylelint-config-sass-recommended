# stylelint-config-sass-recommended

> The recommended shareable config of indent-based Sass for stylelint.

It turns on all the [_possible errors_](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/rules.md#possible-errors) rules within stylelint.

Use it as is or as a foundation for your own config.

## Installation

### npm

```bash
npm install stylelint-config-sass-recommended --save-dev
```

### yarn

```bash
yarn add stylelint-config-sass-recommended --dev
```


## Usage

If you've installed `stylelint-config-sass-recommended` locally within your project, just set your `stylelint` config to:

```json
{
  "extends": "stylelint-config-sass-recommended"
}
```

If you've globally installed `stylelint-config-sass-recommended` using the `-g` flag, then you'll need to use the absolute path to `stylelint-config-sass-recommended` in your config e.g.

```json
{
  "extends": "/absolute/path/to/stylelint-config-sass-recommended"
}
```

### Extending the config

Simply add a `"rules"` key to your config, then add your overrides and additions there.

For example, to change the `at-rule-no-unknown` rule to use its `ignoreAtRules` option, turn off the `block-no-empty` rule, and add the `unit-whitelist` rule:

```json
{
  "extends": "stylelint-config-sass-recommended",
  "rules": {
    "at-rule-no-unknown": [ true, {
      "ignoreAtRules": [
        "extends"
      ]
    }],
    "block-no-empty": null,
    "unit-whitelist": ["em", "rem", "s"]
  }
}
```

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
