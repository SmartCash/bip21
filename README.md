# bip21

[![build status](https://secure.travis-ci.org/dcousens/bip21.png)](http://travis-ci.org/dcousens/bip21)
[![Coverage Status](https://coveralls.io/repos/dcousens/bip21/badge.png)](https://coveralls.io/r/dcousens/bip21)
[![Version](http://img.shields.io/npm/v/bip21.svg)](https://www.npmjs.org/package/bip21)

A BIP21 compatible URL encoding utility library.


## Example

``` javascript
var bip21 = require('bip21')

var decoded = bip21.decode('bitcoin:1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH?amount=20.3&label=Foobar')

console.log(decoded)
// { address: '1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH',
//   amount: 20.3,
//   label: 'Foobar' }

console.log(bip21.encode("1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH"))
// => bitcoin:1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH

console.log(bip21.encode("1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH", {
	amount: 20.3,
	label: "Foobar"
}))
// => bitcoin:1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH?amount=20.3&label=Foobar
```


## License

This library is free and open-source software released under the MIT license.

