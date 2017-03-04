[![Build Status](https://travis-ci.org/kandros/micro-jwt-auth.svg?branch=master)](https://travis-ci.org/kandros/micro-jwt-auth)
[![npm](https://img.shields.io/npm/v/micro-jwt-auth.svg)](https://www.npmjs.com/package/micro-jwt-auth)
# micro-jwt-auth
jwt([json web token](https://jwt.io/introduction/)) authorization wrapper for [Micro](https://github.com/zeit/micro)

> An `Authorization` header with value `Bearer MY_TOKEN_HERE` is expected

## example
```javascript
'use strict'

const jwtAuth = require('micro-jwt-auth')

/*
    if Authorization Bearer is not present or not valid, return 401
*/

module.exports = jwtAuth('my_jwt_secret')(async(req, res) => {
  return "Ciaone!"
})
```
