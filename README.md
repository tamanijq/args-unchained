# args-unchained
[![npm version](https://img.shields.io/npm/v/args-unchained.svg)](https://npmjs.org/package/args-unchained)

Args parser/parser wrapper with alternative syntax

- [commander](https://github.com/tj/commander.js) - Chaining syntax :(
- [yargs](https://github.com/yargs/yargs) - Chaining syntax :(
- [mri](https://github.com/lukeed/mri) - No dynamic help :(

## Install

```sh
npm install --save args-unchained
```

## Usage

### Module

```js
const commander = require('commander')
const unchain = require('args-unchained')

const args = unchain(commander, {
  options: {
    debug: {
      description: 'output extra debugging',
      alias: 'd'
    },
    small: {
      description: 'small pizza size',
      alias: 's'
    },
    ['pizza-type']: {
      description: 'flavour of pizza',
      alias: 'p'
    },
  }
})
```

mycli --hello --happy --k

```js
{
  hello: true,
  happy: true,
  k: true,
}
````
