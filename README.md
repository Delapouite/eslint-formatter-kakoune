# ESLint formatter for kakoune

[ESLint](http://eslint.org) formatter that follows [kakoune](https://github.com/mawww/kakoune/blob/master/rc/base/lint.kak) format:

```
{filename}:{line}:{column}: {kind}: {message}
```

## Install

```sh
$ npm install --save-dev eslint-formatter-kakoune
```

## Usage

### ESLint CLI

```
$ eslint --format=node_modules/eslint-formatter-kakoune file.js
```

In your `kakrc`:

```
hook global WinSetOption filetype=javascript %{
  set buffer lintcmd 'eslint --config .eslintrc.js --format=node_modules/eslint-formatter-kakoune'
  lint-enable
  lint
}
```

You may add more hooks to trigger the lint command on save.

## See also

- [kakoune-flow](https://github.com/Delapouite/kakoune-flow)
- [kakoune-ecmascript](https://github.com/Delapouite/kakoune-ecmascript)

## Licence

MIT
