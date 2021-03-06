# Application

## Overview

Generates new Angular app with better defaults/tools

More info can be found in [my blogpost](https://medium.com/@martin_hotell/use-react-tools-for-better-angular-apps-b0f14f3f8114)

**TL;DR:**

* ditches Karma/Jasmine in favour of Jest
* ditches Protractor/Selenium in favour of TestCafe
* ditches TSLint for formatting in favour of Prettier
* uses tslint:recommended and tslint-config-standard rules for better linting defaults
* adds husky and lint-staged for formatting/linting execution during commit

## Command

```sh
ng new --collection @martin_hotell/schematics my-app [options]
# or
ng new -c @martin_hotell/schematics my-app [options]
```

### General Options

`Angular CLI` [new options](https://github.com/angular/angular-cli/wiki/new).

> **general `ng new` differences:**
>
> * inline templates turned on by default
> * lintFix turned on by default

### Options

Adds Angular material

* `--material`

  * Type: `boolean`
  * Default: `false`

Select Angular material theme

* `--matTheme`
  * Type: `'deeppurple-amber' | 'indigo-pink' | 'pink-bluegrey' | 'purple-green'`
  * Default: `indigo-pink`

Setup default Change Detection for Components

* `--changeDetection`
  * Alias: `-cd`
  * Type: `'Default' | 'OnPush'`
  * Default: `Default`

#### Examples

Generate new app with angular material and default theme

```sh
ng new my-app --material -c @martin_hotell/schematics
```

Generate new app with angular material and different theme

```sh
ng new my-app --material --matTheme pink-bluegrey -c @martin_hotell/schematics
```

Generate new app with OnPush change detection

```sh
ng new my-app --changeDetection OnPush -c @martin_hotell/schematics
# or
ng new my-app -cd OnPush -c @martin_hotell/schematics
```
