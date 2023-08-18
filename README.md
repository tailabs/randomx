# RandomX - Random String Generator

[![license](https://img.shields.io/github/license/tailabs/randomx.svg)](https://github.com/tailabs/randomx/blob/main/LICENSE)
[![Go Report Card](https://goreportcard.com/badge/github.com/tailabs/randomx)](https://goreportcard.com/report/github.com/tailabs/randomx)
[![release](https://img.shields.io/github/release/tailabs/randomx/all.svg)](https://github.com/tailabs/randomx/releases)

RandomX is a Go package that provides a user-friendly tool for generating random strings. It enables you to generate random strings of specified lengths with various character sets, including lowercase letters, uppercase letters, digits, and symbols.

This package was developed with the assistance of [ChatGPT 3.5](https://openai.com/), an advanced language model created by OpenAI.

## Installation

To incorporate RandomX into your Go project, you can easily install it with the following command:

```shell
go get -u github.com/tailabs/randomx
```

## Usage

Here's an example demonstrating how to use the RandomX package to generate random strings:

```go
package main

import (
	"fmt"
	"github.com/tailabs/randomx"
)

func main() {
	rx := randomx.New()

	randomChars := rx.GenerateRandomString(10, randomx.LowercaseLetters+randomx.UppercaseLetters)
	fmt.Println("Random Characters:", randomChars)

	randomOptions := randomx.GenerateOptions{
		UseLowercase: true,
		UseUppercase: true,
		UseDigits:    true,
		UseSymbols:   false,
	}
	randomCustom := rx.GenerateRandomStringFromBuiltin(12, randomOptions)
	fmt.Println("Random Custom:", randomCustom)
}
```

## Credits

RandomX is developed and maintained by [TAILabs](https://github.com/tailabs).

This package was made possible with the assistance of [ChatGPT 3.5](https://openai.com/), a state-of-the-art language model developed by OpenAI.

## License

This project is licensed under the MIT License - see the LICENSE file for details.