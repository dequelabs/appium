# @appium/schema

> JSON schema for [Appium](https://github.com/appium/appium) configuration files

## Description

This package is used internally by Appium, but can also be used to validate Appium configuration files in other contexts.

## Install

```bash
npm i @appium/schema
```

## Usage

The schema is exported as a JS object:

```js
const { AppiumConfigJsonSchema } = require('@appium/schema');
```

It is also provided as a JSON file (since this is a JSON schema, after all):

```js
const schema = require('@appium/schema/lib/appium-config.schema.json');
```

## See Also

[@appium/types](https://npm.im/@appium/types) exports a TypeScript type `AppiumConfig` (generated from this package) for typesafe configuration objects; this may be useful if your Appium configuration is written in JS (e.g., `.appiumrc.js`). Example:

```js
// @ts-check
/** @type {import('@appium/types').AppiumConfig} */
module.exports = {
  server: {
    port: 1234,
    host: '127.0.0.1'
  }
}
```

## Notes

`lib/appium-config.schema.json` is generated by this package from `lib/appium-config-schema.js` (the single source of truth), but is under version control to avoid chicken-or-egg build problems.

## License

Apache-2.0