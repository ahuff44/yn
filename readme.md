# yn [![Build Status](https://travis-ci.org/sindresorhus/yn.svg?branch=master)](https://travis-ci.org/sindresorhus/yn)

> Parse yes/no like values

Useful for validating answers of a CLI prompt.

-

The following case-insensitive values are recognized:

```js
'y', 'yes', 'true', true, 'n', 'no', 'false', false
```


## Install

```sh
$ npm install --save yn
```


## Usage

```js
var yn = require('yn');

yn('y');
//=> true

yn('NO');
//=> false

yn(true);
//=> true

yn('abomasum');
//=> null

/* optionally provide a second argument for options */
/* lenient mode will use a key distance-based score to leniently
 * accept typos of "yes" and "no"
 */
yn('mo', {lenient: true});
//=> false
```

Unrecognized values return `null`.


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
