# bip21

A [BIP21](https://github.com/bitcoin/bips/blob/master/bip-0021.mediawiki) compatible URL encoding library.


## Example

``` javascript
var bip21 = require('bip21')

var decoded = bip21.decode('ravencoin:1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH?amount=20.3&label=Foobar')

console.log(decoded)
// { address: '1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH',
//   options: {
//     amount: 20.3,
//     label: 'Foobar' }
// }
//
// WARNING: Remember to error check the `.address`!

console.log(bip21.encode('1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH'))
// => ravencoin:1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH

console.log(bip21.encode('1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH', {
	amount: 20.3,
	label: 'Foobar'
}))
// => ravencoin:1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH?amount=20.3&label=Foobar
```


## License [MIT](LICENSE)
