# bip21-smart
[![Version](http://img.shields.io/npm/v/bip21-smart.svg)](https://www.npmjs.org/package/bip21-smart)

A [BIP21](https://github.com/bitcoin/bips/blob/master/bip-0021.mediawiki) compatible URL encoding library.


## Example

``` javascript
var bip21 = require('bip21-smart')

var decoded = bip21.decode('smartcash:Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5?amount=20.3&label=Foobar')

console.log(decoded)
// { address: 'Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5',
//   options: {
//     amount: 20.3,
//     label: 'Foobar' }
// }
//
// WARNING: Remember to error check the `.address`!

console.log(bip21.encode('Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5'))
// => smartcash:Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5

console.log(bip21.encode('Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5', {
	amount: 20.3,
	label: 'Foobar'
}))
// => smartcash:Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5?amount=20.3&label=Foobar
```


## License [MIT](LICENSE)
