# react-native-cryptr
react-native-cryptr is a simple encrypt and decrypt module for react native

It is for doing simple encryption of values UTF-8 strings that need to be decrypted at a later time.

If you require anything more than that you probably want to use something more advanced or [react-native-crypto](https://www.npmjs.com/package/react-native-crypto) directly.

The Cryptr constructor takes 1 required and 1 optional argument.

	Cryptr(secret[, algorithm])

If an algorithm is not provided it defaults to `aes-256-ctr`.


**DO NOT USE THIS MODULE FOR ENCRYPTING PASSWORDS!**

Passwords should be a one way hash. Use [react-native-bcrypt](https://www.npmjs.com/package/react-native-bcrypt) for that.


## Install

	npm install react-native-cryptr

## Usage

``` javascript
var Cryptr = require('react-native-cryptr'),
    cryptr = new Cryptr('myTotalySecretKey');


var encryptedString = cryptr.encrypt('bacon'),
    decryptedString = cryptr.decrypt(encryptedString);

console.log(encryptedString);  // d7233809c0
console.log(decryptedString);  // bacon
```

