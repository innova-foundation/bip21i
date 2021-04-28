# bip21

[![build status](https://secure.travis-ci.org/carsenk/bip21d.png)](http://travis-ci.org/bitcoinjs/bip21)
[![Version](http://img.shields.io/npm/v/bip21d.svg)](https://www.npmjs.org/package/bip21)

A [BIP21](https://github.com/bitcoin/bips/blob/master/bip-0021.mediawiki) compatible URL encoding library for Innova.


## Example

``` javascript
var bip21 = require('bip21d')

var decoded = bip21.decode('innova:iJU9QDQ3a1ZVevp5tv4xW4c8xVVXV5QwEW?amount=20.3&label=Foobar')

console.log(decoded)
// { address: 'iJU9QDQ3a1ZVevp5tv4xW4c8xVVXV5QwEW',
//   options: {
//     amount: 20.3,
//     label: 'Foobar' }
// }
//
// WARNING: Remember to error check the `.address`!

console.log(bip21.encode('iJU9QDQ3a1ZVevp5tv4xW4c8xVVXV5QwEW'))
// => innova:iJU9QDQ3a1ZVevp5tv4xW4c8xVVXV5QwEW

console.log(bip21.encode('Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR', {
	amount: 20.3,
	label: 'Foobar'
}))
// => innova:Ffqz14cyvZYJavD76t6oHNDJnGiWcZMVxR?amount=20.3&label=Foobar
```


## License [MIT](LICENSE)
