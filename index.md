# 目录

[TOC]

# 第1章 基础数据类型

## 1.1 布尔类型(bool)

Golang语言中布尔类型使用bool关键字定义，定义格式: `var typename bool = false

/test/bls.go

```go
package main

import (
    "fmt"
    "math/cmplx"
)

var (
    ToBe bool = false
)

func main() {
    fmt.Printf("Type: %T Value: %v\n", ToBe, ToBe)
}
```

## 1.2 字符串(string)

/test/strings.go

```go
 定义字符串 var s string
 
 
 package main

import "fmt"


func main() {
   
    var s string
    fmt.Printf("%v\n" s)
}
