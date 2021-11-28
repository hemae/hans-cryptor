# hans-cryptor
string cryptor for node.js

## Table of contents
* [Features](#features)
* [Installing](#installing)
* [Example](#example)
    + [encrypt](#encrypt)
    + [decrypt](#decrypt)
    + [compare](#compare)
    

<a name="features"><h2>Features</h2></a>
* encrypring and decrypting strings by password using Vigenere method

<a name="installing"><h2>Installing</h2></a>
Add the package to your project
```
npm i hans-cryptor
```

<a name="example"><h2>Example</h2></a>

Export *encrypt*, *decrypt*, *compare* from *hans-cryptor*

```javascript
const {encrypt, decrypt, compare} = require('hans-cryptor')
```
using TypeScript
```typescript
import {encrypt, decrypt, compare} from 'hans-cryptor'
```

<a name="encrypt"><h3>encrypt</h3></a>        

```typescript
const str = 'string for encrypting'
const key = 'this is a key'
const encryptedStr = crypt.encrypt(str, key)
console.log(encryptedStr) // çÜÛÜÐÐÈëíØÝÜÐ
```

<a name="decrypt"><h3>decrypt</h3></a>        

```typescript
const decryptedStr = crypt.decrypt(encryptedStr, key)
console.log(decryptedStr) // string for encrypting
```

<a name="compare"><h3>compare</h3></a>        

```typescript
const isMatched = crypt.compare(str, encryptedStr, key)
console.log(isMatched) // true

const anotherKey = 'this is another key'
const anotherEncryptedStr = crypt.encrypt(str, anotherKey)
const isMatchForAnother = crypt.compare(str, anotherEncryptedStr, key)
console.log(isMatchForAnother) // false
```
