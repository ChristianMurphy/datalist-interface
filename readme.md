# datalist-interface

[![Build][build-badge]][build]
[![Coverage][coverage-badge]][coverage]
[![Downloads][downloads-badge]][downloads]
[![Size][size-badge]][size]

A simple interface for a list.

## Installation

[npm][]:

```bash
npm install datalist-interface
```

## Usage

```js
var DatalistInterface = require('datalist-interface')

var mammals = new DatalistInterface([
  'common vampire bat',
  'virginia opossum',
  'eastern grey kangaroo',
  'tasmanian devil',
  'human',
  'northern elephant seal',
  'fox squirrel',
  'tree pangolin',
  'african elephant',
  'platypus',
  'colugo',
  'reindeer',
  'humpback whale',
  'star-nosed mole',
  'giant panda',
  'giant armadillo',
  'plains zebra',
  'black and rufous elephant shrew'
])

mammals.is('human') // => true
mammals.is('unicorn') // => false

mammals.add('unicorn').is('unicorn') // => true

mammals.remove('unicorn').is('unicorn') // => false
```

## API

### `DatalistInterface([value...])`

Create a new instance.  Values are passed to [`#add()`][add].

###### Example

```js
var DatalistInterface = require('datalist-interface')

var fish = new DatalistInterface(['shark', 'tuna'])
```

### `DatalistInterface#is(value)`

### `DatalistInterface#has(value)`

Check if `value` is in the list.

###### Example

```js
fish.is('shark') // => true
fish.is('human') // => false
```

### `DatalistInterface#add([value...])`

Add each value to `list`.

###### Example

```js
fish.add('giant grouper', 'red lionfish')
```

### `DatalistInterface#remove([value...])`

Remove each value from `list`.

###### Example

```js
fish.remove('giant grouper', 'reindeer')
```

### `DatalistInterface#all()`

### `DatalistInterface#valueOf()`

### `DatalistInterface#toJSON()`

Return the list as an `Array`.

###### Example

```js
fish.all() // => ['shark', 'tuna', 'red lionfish']
```

### `DatalistInterface#toString()`

Return the list as a `string`.

###### Example

```js
fish.toString() // => 'shark,tuna,red lionfish'
```

## Related

*   [`datamap-interface`](https://github.com/wooorm/datamap-interface)
    — Simple interface for a map

## License

[MIT][license] © [Titus Wormer][author]

<!-- Definitions -->

[build-badge]: https://img.shields.io/travis/wooorm/datalist-interface.svg

[build]: https://travis-ci.org/wooorm/datalist-interface

[coverage-badge]: https://img.shields.io/codecov/c/github/wooorm/datalist-interface.svg

[coverage]: https://codecov.io/github/wooorm/datalist-interface

[downloads-badge]: https://img.shields.io/npm/dm/datalist-interface.svg

[downloads]: https://www.npmjs.com/package/datalist-interface

[size-badge]: https://img.shields.io/bundlephobia/minzip/datalist-interface.svg

[size]: https://bundlephobia.com/result?p=datalist-interface

[npm]: https://docs.npmjs.com/cli/install

[license]: license

[author]: https://wooorm.com

[add]: #datalistinterfaceaddvalue
