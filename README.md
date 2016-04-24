# CryptoKitten

[![Build Status](https://travis-ci.org/CryptoKitten/HMAC.svg?branch=master)](https://travis-ci.org/CryptoKitten/HMAC)
[![Swift Version](https://img.shields.io/badge/swift-3.0-orange.svg)](https://swift.org)
![License](https://img.shields.io/github/license/CryptoKitten/HMAC.svg)
[![Slack Status](http://orlandos.nl:3000/badge.svg)](http://orlandos.nl:3000/)

A set of crypto libraries for Swift, written in Swift.
 
## HMAC
 
HMAC is a library that provides HMAC message authentication support on top of CryptoEssentials.

## Usage

```swift
var messageBytes = [UInt8](), passwordBytes = [UInt8]()
messageBytes.append(contentsOf: "MyMessage".utf8)
passwordBytes.append(contentsOf: "hunter2".utf8)

let passwordHash = SHA2<SHA512>.calculate(passwordBytes)
   
let authenticatedMessage = HMAC<MD5>.authenticate(message, withkey: passwordHash)
```

## License

**CryptoKitten uses parts of [CryptoSwift](https://github.com/krzyzanowskim/CryptoSwift) whose license is included below.
Parts where CryptoSwift code is used have this license included in the file**

Copyright (C) 2014 Marcin Krzyżanowski marcin.krzyzanowski@gmail.com This software is provided 'as-is', without any express or implied warranty.

In no event will the authors be held liable for any damages arising from the use of this software.

Permission is granted to anyone to use this software for any purpose, including commercial applications, and to alter it and redistribute it freely, subject to the following restrictions:

    The origin of this software must not be misrepresented; you must not claim that you wrote the original software. If you use this software in a product, an acknowledgment in the product documentation is required.
    Altered source versions must be plainly marked as such, and must not be misrepresented as being the original software.
    This notice may not be removed or altered from any source or binary distribution.
