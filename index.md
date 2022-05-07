<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [目录](#%E7%9B%AE%E5%BD%95)
- [第1章 基础数据类型](#%E7%AC%AC1%E7%AB%A0-%E5%9F%BA%E7%A1%80%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B)
  - [1.1 布尔类型(bool)](#11-%E5%B8%83%E5%B0%94%E7%B1%BB%E5%9E%8Bbool)
  - [1.2 字符串(string)](#12-%E5%AD%97%E7%AC%A6%E4%B8%B2string)
  - [1.3 整型(int int8 int16 int32 int64)](#13-%E6%95%B4%E5%9E%8Bint-int8-int16-int32-int64)
  - [1.4 byte类型(uint8)](#14-byte%E7%B1%BB%E5%9E%8Buint8)
  - [1.5 Unicode类型(rune ， int32 别名)](#15-unicode%E7%B1%BB%E5%9E%8Brune--int32-%E5%88%AB%E5%90%8D)
  - [1.6 浮点类型(float32 float64)](#16-%E6%B5%AE%E7%82%B9%E7%B1%BB%E5%9E%8Bfloat32-float64)
  - [1.7 复数类型 (complex64 complex128)](#17-%E5%A4%8D%E6%95%B0%E7%B1%BB%E5%9E%8B-complex64-complex128)
  - [1.8类型推断](#18%E7%B1%BB%E5%9E%8B%E6%8E%A8%E6%96%AD)
  - [1.9类型转换](#19%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2)
  - [1.10 零值](#110-%E9%9B%B6%E5%80%BC)
  - [1.11 包](#111-%E5%8C%85)
  - [1.12 import语句](#112-import%E8%AF%AD%E5%8F%A5)
  - [1.13 名字导出](#113-%E5%90%8D%E5%AD%97%E5%AF%BC%E5%87%BA)
  - [1.14 函数](#114-%E5%87%BD%E6%95%B0)
  - [1.15 返回多个值](#115-%E8%BF%94%E5%9B%9E%E5%A4%9A%E4%B8%AA%E5%80%BC)
  - [1.16 命名返回值](#116-%E5%91%BD%E5%90%8D%E8%BF%94%E5%9B%9E%E5%80%BC)
  - [1.17 变量](#117-%E5%8F%98%E9%87%8F)
  - [1.18 初始值](#118-%E5%88%9D%E5%A7%8B%E5%80%BC)
  - [1.19 简式申明](#119-%E7%AE%80%E5%BC%8F%E7%94%B3%E6%98%8E)
  - [1.20 常量](#120-%E5%B8%B8%E9%87%8F)
  - [1.21 数值常量](#121-%E6%95%B0%E5%80%BC%E5%B8%B8%E9%87%8F)
  - [1.22 小节](#122-%E5%B0%8F%E8%8A%82)
- [第2章 Golang复杂数据类型](#%E7%AC%AC2%E7%AB%A0-golang%E5%A4%8D%E6%9D%82%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B)
  - [2.1 map](#21-map)
  - [2.2 字面量](#22-%E5%AD%97%E9%9D%A2%E9%87%8F)
  - [2.3 操作](#23-%E6%93%8D%E4%BD%9C)
  - [2.4 struct](#24-struct)
  - [2.5 结构体字段](#25-%E7%BB%93%E6%9E%84%E4%BD%93%E5%AD%97%E6%AE%B5)
  - [2.5 结构体指针](#25-%E7%BB%93%E6%9E%84%E4%BD%93%E6%8C%87%E9%92%88)
  - [2.6 结构体字面量](#26-%E7%BB%93%E6%9E%84%E4%BD%93%E5%AD%97%E9%9D%A2%E9%87%8F)
  - [2.7 slice](#27-slice)
  - [2.8 数组引用](#28-%E6%95%B0%E7%BB%84%E5%BC%95%E7%94%A8)
  - [2.9 下标默认值](#29-%E4%B8%8B%E6%A0%87%E9%BB%98%E8%AE%A4%E5%80%BC)
  - [2.10 长度和容量](#210-%E9%95%BF%E5%BA%A6%E5%92%8C%E5%AE%B9%E9%87%8F)
  - [2.11 空切片](#211-%E7%A9%BA%E5%88%87%E7%89%87)
  - [2.12 make关键字](#212-make%E5%85%B3%E9%94%AE%E5%AD%97)
  - [2.13 切片的切片](#213-%E5%88%87%E7%89%87%E7%9A%84%E5%88%87%E7%89%87)
  - [2.14 元素追加](#214-%E5%85%83%E7%B4%A0%E8%BF%BD%E5%8A%A0)
  - [2.15 遍历](#215-%E9%81%8D%E5%8E%86)
  - [2.16 array](#216-array)
  - [2.17 pointer](#217-pointer)
  - [2.18 函数值](#218-%E5%87%BD%E6%95%B0%E5%80%BC)
  - [2.19 闭包](#219-%E9%97%AD%E5%8C%85)
  - [2.20 方法](#220-%E6%96%B9%E6%B3%95)
  - [2.21 非结构体方法](#221-%E9%9D%9E%E7%BB%93%E6%9E%84%E4%BD%93%E6%96%B9%E6%B3%95)
  - [2.22 指针接收者](#222-%E6%8C%87%E9%92%88%E6%8E%A5%E6%94%B6%E8%80%85)
  - [2.23 传值与传引用](#223-%E4%BC%A0%E5%80%BC%E4%B8%8E%E4%BC%A0%E5%BC%95%E7%94%A8)
  - [2.24 间接传指针](#224-%E9%97%B4%E6%8E%A5%E4%BC%A0%E6%8C%87%E9%92%88)
  - [2.25 间接传值](#225-%E9%97%B4%E6%8E%A5%E4%BC%A0%E5%80%BC)
  - [2.26 传值还是传指针](#226-%E4%BC%A0%E5%80%BC%E8%BF%98%E6%98%AF%E4%BC%A0%E6%8C%87%E9%92%88)
  - [2.27 小节](#227-%E5%B0%8F%E8%8A%82)
- [第3章 Golang分支开发](#%E7%AC%AC3%E7%AB%A0-golang%E5%88%86%E6%94%AF%E5%BC%80%E5%8F%91)
  - [3.1 if](#31-if)
  - [3.2 初始语句](#32-%E5%88%9D%E5%A7%8B%E8%AF%AD%E5%8F%A5)
  - [3.3 if-else 语句](#33-if-else-%E8%AF%AD%E5%8F%A5)
  - [3.4 for](#34-for)
  - [3.5 无限循环](#35-%E6%97%A0%E9%99%90%E5%BE%AA%E7%8E%AF)
  - [3.6 switch](#36-switch)
  - [3.7 检查顺序](#37%C2%A0%E6%A3%80%E6%9F%A5%E9%A1%BA%E5%BA%8F)
  - [3.8 省略条件](#38-%E7%9C%81%E7%95%A5%E6%9D%A1%E4%BB%B6)
  - [3.9 defer](#39-defer)
  - [3.10 defer栈](#310-defer%E6%A0%88)
  - [3.11 小节](#311-%E5%B0%8F%E8%8A%82)
- [第4章 Golang并发编程](#%E7%AC%AC4%E7%AB%A0-golang%E5%B9%B6%E5%8F%91%E7%BC%96%E7%A8%8B)
  - [4.1并发之道协程](#41%E5%B9%B6%E5%8F%91%E4%B9%8B%E9%81%93%E5%8D%8F%E7%A8%8B)
  - [4.2 并发之道channel](#42-%E5%B9%B6%E5%8F%91%E4%B9%8B%E9%81%93channel)
  - [4.3 管道缓存之Buffered Channels](#43-%E7%AE%A1%E9%81%93%E7%BC%93%E5%AD%98%E4%B9%8Bbuffered-channels)
  - [4.4 多路复用之select](#44-%E5%A4%9A%E8%B7%AF%E5%A4%8D%E7%94%A8%E4%B9%8Bselect)
  - [4.5 管道之Range和Close](#45-%E7%AE%A1%E9%81%93%E4%B9%8Brange%E5%92%8Cclose)
  - [4.6 管道Default Selection](#46-%E7%AE%A1%E9%81%93default-selection)
  - [4.7 Golang二叉树之一](#47-golang%E4%BA%8C%E5%8F%89%E6%A0%91%E4%B9%8B%E4%B8%80)
  - [4.8 Golang二叉树之二](#48-golang%E4%BA%8C%E5%8F%89%E6%A0%91%E4%B9%8B%E4%BA%8C)
  - [4.9 锁](#49-%E9%94%81)
  - [4.10 小节](#410-%E5%B0%8F%E8%8A%82)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



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
```

## 1.3 整型(int int8 int16 int32 int64)

一般来说，int 、 uint 以及 uintptr 类型在 `32` 位机器上是 `32` 位长； 在 `64` 位机器上则是 `64` 位长。 需要使用整数时， `int` 类型是首选， 除非你有特别的理由一定要用 **定长** 或者 **无符号** 类型。

/test/ints.go

```go
package main

import (
	"fmt"
	"math/cmplx"
)

var (
	ToBe   bool       = false
	MaxInt uint64     = 1<<64 - 1
	z      complex128 = cmplx.Sqrt(-5 + 12i)
)

func main() {
	fmt.Printf("Type: %T Value: %v\n", ToBe, ToBe)
	fmt.Printf("Type: %T Value: %v\n", MaxInt, MaxInt)
	fmt.Printf("Type: %T Value: %v\n", z, z)
}
```



## 1.4 byte类型(uint8)

```
byte 类型是 uint8 的别名，对于只占用 1 个字节的传统 ASCII 编码的字符来说，完全没有问题，例如 var ch byte = 'A'，字符使用单引号括起来。
```

/test/bytes.go

```go

package main

import (
	"fmt"
)

func main() {
	var bt = []byte{}
	fmt.Println("bt=", bt)
}
```



## 1.5 Unicode类型(rune ， int32 别名)

Go 语言采用的字符编码方案从属于 Unicode 编码规范。更确切地说，Go 语言的代码正是由 Unicode 字符组成的。Go 语言的所有源代码，都必须按照 Unicode 编码规范中的 UTF-8 编码格式进行编码。

/test/unicode.go

```go
func unicodeAndUtf8() {
    tmpStr := "hgfang的SRE人生."
    fmt.Printf("string:%q\n",tmpStr)
    fmt.Printf("rune(char):%q\n",[]rune(tmpStr))
    fmt.Printf("rune(hex):%x\n",[]rune(tmpStr))
    fmt.Printf("bytes(hex):% x\n",[]byte(tmpStr))
}
```

对应输出的效果如下:

```tex
string:"BGBiao 的SRE人生."
rune(char):['h' 'g' 'f' 'a' 'n' 'g' ' ' '的' 'S' 'R' 'E' '人' '生' '.']
rune(hex):[42 47 42 69 61 6f 20 7684 53 52 45 4eba 751f 2e]
bytes(hex):42 47 42 69 61 6f 20 e7 9a 84 53 52 45 e4 ba ba e7 94 9f 2e
```

## 1.6 浮点类型(float32 float64)

Golang语言中支持float32和float64两种类型浮点，具体使用如下：

/test/float.go

```go
package main

import (
	"fmt"
)

func main() {
	var float32 float32 = 1.0
	var float64 float64 = 1.0

	fmt.Println("float32", float32)
	fmt.Println("float64", float64)

}
```



## 1.7 复数类型 (complex64 complex128)

Go语言中**复数**的**类型**有两种，分别是 complex128（64 位实数和虚数）和 complex64（32 位实数和虚数），其中 complex128 为**复数**的默认**类型**。 **复数**的值由三部分组成RE + IMi，其中RE 是实数部分，IM 是虚数部分，RE 和IM 均为float **类型**，而最后的i 是虚数单位。

```go
var x complex128 = complex(1, 2) // 1+2i
var y complex128 = complex(3, 4) // 3+4i
fmt.Println(x*y)                 // "(-5+10i)"
fmt.Println(real(x*y))           // "-5"
fmt.Println(imag(x*y))           // "10"
```



## 1.8类型推断

变量类型通过右边的值推理而来。如果申明右边的值是有类型的，那么新变量也是一样的类型：

```go
var i int
j := i  // j is an int as well
```

如果右边只是一个数值常量，没有具体类型，那么新变量可能是 int 、 float64 以及 complex128 三种类型中的一种，取决于常量的精度。

```go
i := 42             // int
f := 3.142          // float64
g := 0.867 + 0.5i   // complex128
```

接下来做个实验吧！ 改变例子中 `v` 的初始值，观察它是如何影响变量类型的：

/test/types.go

```go
package main

import "fmt"


func main() {
    v := 42     // change me!
    fmt.Printf("v is of type %T\n", v)
}
```

## 1.9类型转换

**表达式** ( `expression` ) `T(v)` 将值 `v` 转换成类型 `T` ， 这就是所谓的 **类型转换** ( `type conversions` )。

这是一些数值类型转换：

```go
var i int = 42
var f float64 = float64(i)
var u uint = uint(f)
```

或者简写成：

```go
i := 42
f := float(i)
u := uint(f)
```

跟 C 语言有所不同， Go 在不同类型之间赋值，需要显式类型转换。 不信，将下面例子中 `float64` 和 `unit` 类型转换移除，看看发生什么？

/test/typetransfer.go

```go
package main

import (
    "fmt"
    "math"
)
func main() {
    var x, y int = 3, 4
    var f float64 = math.Sqrt(float64(x*x + y*y))
    var z uint = uint(f)
    fmt.Println(x, y, z)
}
```

## 1.10 零值

变量申明时没有显式赋初始值，则默认是“ **零** ”。

不同的类型有不同的“ **零** ”：

- 对于数值类型是 `0` ；

- 对于布尔类型是 `false` ；

- 对于字符串类型是 `""` (空字符串)；

  /test/zerovalue.go

  ```go
  package main
  import "fmt"
  func main() {
      var i int
      var f float64
      var b bool
      var s string
      fmt.Printf("%v %v %v %q\n", i, f, b, s)
  }
  ```

## 1.11 包

每个 Go 程序都是由一些包组成的。

程序从 main 包开始执行。

/test/pkg.go

```go
package main
import (
    "fmt"
    "math/rand"
)
func main() {
    fmt.Println("My favorite number is", rand.Intn(10))
}
```

在这个程序，通过 import 导入两个包， `fmt` 和 `math/rand` (包路径)。

按照惯例，包名与包路径最后部分相同。 例如， `math/rand` 包中的源码文件都以 `package rand` 语句开头。



## 1.12 import语句

Go 通过 `import` 语句引入包并在代码中使用。

import 语句有两种不同的写法，上面例子是其中的一种写法—— **批量导入** ； 第二种则是分成多个语句：

```go
import "fmt"
import "math"
```

两种写法虽然没有实质区别，还是 **推荐采用批量写法** ，这是 **最佳风格** 。

## 1.13 名字导出

在 Go 语言，以大写字母开头的名字就会被 **导出** ( `exported` )。 举例， `Pizza` 就是一个导出名字， `math` 包中的 `Pi` 也是。

/test/export-name.go

```go
package main
 import (
     "fmt"
     "math"
 )
 func main() {
     fmt.Println(math.Pi)
 }
```

相反， `pizza` 和 `pi` 由于不是大写字母开头，因此不会被导出。

一个包导入后，只能引用到导出名字。 其他任何非导出名字在包外是没有办法访问到的(不可见)。

## 1.14 函数

Go 语言中，函数可以接受零或多个参数：

/test/funcs.go

```go
package main

import "fmt"


func add(x int, y int) int {
    return x + y
}

func main() {
    fmt.Println(add(43, 13))
}
```

在这个例子中， `add` 函数接受两个整型( `int` )参数。 注意到，类型申明紧跟在参数名之后，与其他语言有些区别。

如果参数类型相同，则在最后一个申明即可，前面的可以省略。

因此，可以将 `x int, y int` 简写成 `x, y int` 。

## 1.15 返回多个值

Go 函数可以非常优雅地返回多个值，比起定义结构体返回指针之类的舒服多啦！ 写个简单的程序交换两个字符串：

/test/multiple-return-value.go

```go
package main

import "fmt"


func swap(x, y string) (string, string) {
    return y, x
}

func main() {
    a, b := swap("hello", "world")
    fmt.Println(a, b)
}
```

## 1.16 命名返回值

Go 函数返回值可以被命名( `named` )，命名后当做函数参数来对待。 命名的意义在于指明各个返回值含义。

/test/name-return-value.go

```go
 package main

 import "fmt"


 func split(sum int) (x, y int) {
     x = sum * 4 / 9
     y = sum - x
     return
 }

 func main() {
     fmt.Println(split(17))
 }
```

一个不带任何参数的 `return` 语句返回所有命名返回值， 这就是所谓的裸返回 ( `naked return` )。 裸返回只推荐在短函数中使用，如在长函数中滥用，则影响代码可读性 。

## 1.17 变量

`var` 语句 **申明** ( `declare` )变量列表； 跟 [函数](https://golang.fasionchan.com/zh_CN/latest/tour/functions.html) 参数列表一样，类型在最后指定。

`var` 语句的作用域(可见范围)可以是 **包级别** 或者 **函数级别** 。 下面这个例子同时包含这两种级别：

/test/vars.go

```go
package main

 import "fmt"

 var c, python, java bool


 func main() {
     var i int
     fmt.Println(i, c, python, java)
 }
```

作用域是啥意思呢？

以上述代码为例，变量 `c` 、 `python` 、 `java` 的作用域是 **包级别** ， 意味着包内任何函数都可以访问这些变量； 定义在函数内部的 `i` 则是 **函数级别** ， 只有在 `main` 函数内部才能访问。

## 1.18 初始值

变量申明可以带初始值，一个变量一个。 在初始值存在的情况下，类型可以忽略；变量则继承初始值的类型。

/test/inits-values.go

```go
package main

import "fmt"

var i, j int = 1, 2


func main() {
    var c, python, java = true, false, "no!"
    fmt.Println(i, j, c, python, java)
}
```

## 1.19 简式申明

在函数内部，可以用 `:=` 赋值语句代替 `var` 变量申明语句， 变量类型也可以省略，这就是 **简式申明** 。

/test/short-variable.go

```go
package main

import "fmt"
func main() {
    var i, j int = 1, 2
    k := 3
    c, python, java := true, false, "no!"

    fmt.Println(i, j, k, c, python, java)
}
```

在函数外部，每个语句都必须由一个关键字开始(如var 、 func 等)， := 语句不可用。

## 1.20 常量

常量(constants)申明与变量一样，只不过换成 const 关键字。 常量可以是字符、字符串、布尔，或者数值类型。 另外，常量不能使用 := 语法申明。

/test/constants.go

```go
package main

import "fmt"

const Pi = 3.14


func main() {
    const World = "世界"
    fmt.Println("Hello", World)
    fmt.Println("Happy", Pi, "Day")

    const Truth = true
    fmt.Println("Go rules?", Truth)
}
```

## 1.21 数值常量

数值常量是高精度数值。 常量虽然没有指定类型，却可以根据实际情况采用合适类型，保证精度够用。

试试输出 needInt(Big) ：

/test/num-constants.go

```go
package main

import "fmt"

const (
    // Create a huge number by shifting a 1 bit left 100 places.
    // In other worlds, the binary number that is 1 followed by 100 zeros.
    Big = 1 << 100

    // Shift it right again 99 places, so we end up with 1<<1, or 2.
    Small = Big >> 99
)


func needInt(x int) int { return x*10 + 1 }


func needFloat(x float64) float64 {
    return x * 0.1
}

func main() {
    fmt.Println(needInt(Small))
    fmt.Println(needFloat(Small))
    fmt.Println(needFloat(Big))
}
```

## 1.22 小节

# 第2章 Golang复杂数据类型

## 2.1 map

映射表( map)是一种将键(key)映射到值 ( value )的数据结构。

映射表的零值是 nil。 一个 nil 映射表既不包含任何键，也不能添加。

映射表同样可以通过 [make](https://golang.org/pkg/builtin/#make) 函数来创建并初始化：

/test/maps.go

```go
package main

import "fmt"

type Vertex struct {
    Lat, Long float64
}

var m map[string]Vertex


func main() {
    m =make(map[string]Vertex)
    m["Bell Labs"] = Vertex{
        40.68433, -74.39967,
    }
    fmt.Println(m["Bell Labs"])
}
```

## 2.2 字面量

映射表也可以用 字面量 ( literal )定义。 写法与 [结构体]字面量类似，额外写上键而已。

/test/map-values.go

```go
package main

import "fmt"

type Vertex struct {
    Lat, Long float64
}

var m = map[string]Vertex{
    "Bell Labs": Vertex{
        40.68433, -74.39967,
    },
    "Google": Vertex{
        37.42202, -122.08408,
    },
}


func main() {
    fmt.Println(m)
}
```

当然了，你也可以省略类型：

/test/maps.go

```go
package main

import "fmt"

type Vertex struct {
    Lat, Long float64
}

var m = map[string]Vertex{
    "Bell Labs": {40.68433, -74.39967},
    "Google": {37.42202, -122.08408},
}


func main() {
    fmt.Println(m)
}
```

## 2.3 操作

**插入** 或 **更新** 映射表 m 中的一个元素：

```go
m[key] = elem
```

取出一个元素：

```go
elem = m[key]
```

删除一个元素：

```go
delete(m, key)
```

通过 **双赋值** ( two-value assignment )测试给定键是否存在：

```
elem, ok = m[key]
```

这样一来，如果 k 在 m 中存在， ok 便是 true ；否则， ok 则是 false ，而 elem 则是字典元素类型的 [零值]。

/test/op-maps.go

```go
package main

import "fmt"


func main() {
    m := make(map[string]int)

    m["Answer"] = 42
    fmt.Println("The value:", m["Answer"])

    m["Answer"] = 48
    fmt.Println("The value:", m["Answer"])

    delete(m, "Answer")
    fmt.Println("The value:", m["Answer"])

    v, ok := m["Answer"]
    fmt.Println("The value:", v, "Present?", ok)
}
```

注解

注意到，如果变量 elem 或者 ok 未声明，可以采用 [简式申明]。即：

```go
elem, ok := m[key]
```

## 2.4 struct

Go 语言也有结构体——由若干 [字段](https://golang.fasionchan.com/zh_CN/latest/tour/structs.html#tour-structs-fields) ( `field` )组成的集合。

/test/structs.go

```go
package main

import "fmt"

type Vertex struct {
    X int
    Y int
}


func main() {
    fmt.Println(Vertex{1, 2})
}
```

例子定义了一个名为 Vertex 的结构体，用于表示一个顶点。 结构体包含两个字段，分别是 X 和 Y ，类型都是 int 。



## 2.5 结构体字段

结构体字段可以通过点号 `.` 操作符访问。

/test/struct-fields.go

```go
package main

 import "fmt"

 type Vertex struct {
     X int
     Y int
 }


 func main() {
     v := Vertex{1, 2}
     fmt.Println(v.X)

     v.X = 4
     fmt.Println(v.X)
 }
```

## 2.5 结构体指针

结构体字段可以通过指针来访问。

假设我们有一个结构体指针 p ，访问字段 X 理论上可以这么写 (*p).X。 然而，这看上去很累赘不是？ 作为很人性化的语言， Go 允许直接写成 p.X 。 这两种写法没有什么实质性的区别，但是后者显然更为清晰。

/test/struct-pointers.go

```go
package main

import "fmt"

type Vertex struct {
    X int
    Y int
}


func main() {
    v := Vertex{1, 2}
    p := &v
    p.X = 1e9
    fmt.Println(v)
}
```

## 2.6 结构体字面量

结构体字面量( literal)，即通过列举字段值来表示一个新分配的结构体。

可以通过 字段名: 语法指定部分字段值，其他字段则默认为零值。 由于指定了字段名，字段列举顺序也就无关紧要了。

在结构体之前加上 & 操作符，则返回对应的结构体指针。

/test/struct-values.go

```go
package main

import "fmt"

type Vertex struct {
    X, Y int
}

var (
    v1 = Vertex{1, 2}   // has type Vertex
    v2 = Vertex{X: 1}   // Y:0 is implicit
    v3 = Vertex{}       // X:0 and Y:0
    p  = &Vertex{1, 2}  // has type *Vertex
)


func main() {
    fmt.Println(v1, p, v2, v3)
}
```

## 2.7 slice

数组长度是固定的。相反切片 ( slice )是一个数组元素的弹性视图，长度可以是动态的。 实际上，切片比数组更为常用。

类型[]T 就是一个由类型 T 元素组成的切片。

切片通过两个索引下标定义，一个表示下边界 ( low bound )，一个表示上边界 ( high bound )，以冒号( := )分隔：

```
a[low : high]
```

这表示一个 **半开半闭** 区间，包括第一个元素，但不包括最后一个。

以下表达式创建一个包含元素 1 到元素 3 的切片(不包括元素 4)：

```
a[1:4]
```

完整例子如下：

/test/slices.go

```go
package main

import "fmt"


func main() {
    primes := [6]int{2, 3, 5, 7, 11, 13}

    var s []int = primes[1:4]
    fmt.Println(s)
}
```

## 2.8 数组引用

切片实际上并 不存储任何数据 ，只是用来描述关联数组的一部分。 因此，修改切片元素等价于修改对应的数组元素，其他共用该数组的切片对此也可见。 换句话讲， 切片就像是数组的引用 。

/test/slice-pointers.go

```go
package main

import "fmt"


func main() {
    names := [4]string{
        "John",
        "Paul",
        "George",
        "Ringo",
    }
    fmt.Println(names)

    a := names[0:2]
    b := names[1:3]
    fmt.Println(a, b)

    b[0] = "XXX"
    fmt.Println(a, b)
    fmt.Println(names)
}
```



## 2.9 下标默认值

定义切片，可以忽略上边界或者下边界，而使用 **默认值** 。 对于下边界，默认值为 0 ；下边界，默认值则是 **切片长度** 。

因此，对于数组：

```go
var a [10]int
```

以下切片表达式均是等价的：

```go
a[0:10]
a[:10]
a[0:]
a[:]
```

/test/slice-bounds.go

```go
package main

import "fmt"


func main() {
    s := []int{2, 3, 5, 7, 11, 13}

    s = s[1:4]
    fmt.Println(s)

    s = s[:2]
    fmt.Println(s)

    s = s[1:]
    fmt.Println(s)
}
```

## 2.10 长度和容量

切片有两个重要属性， 长度 ( length )和 容量 ( capacity )。切片的长度等于切片包含的元素个数。切片的容量等于底下数组的元素个数，从切片第一个元素算起。

对于切片 s ，长度和容量分别可以通过表达式 len(s)以及 cap(s) 获得。通过重切( re-slicing )，你可以扩张一个切片的长度，只要容量足够。 你可以试试修改下面这个例子，将切片扩张到超出容量，看看会发生什么事情：

/test/slice-len-cap.go

```go
package main

import "fmt"


func main() {
    s := []int{2, 3, 5, 7, 11, 13}
    printSlice(s)

    // Slice the slice to give it zero length.
    s = s[:0]
    printSlice(s)

    // Extend its length.
    s = s[:4]
    printSlice(s)

    // Drop its first two values.
    s = s[2:]
    printSlice(s)
}


func printSlice(s []int) {
    fmt.Printf("len=%d cap=%d %v\n", len(s), cap(s), s)
}
```

## 2.11 空切片

切片的零值 是 nil ，即空切片 。 空切片长度和容量均为 0 ，当然也不需要底层数组。

/test/nil-slices.go

```go
package main

import "fmt"


func main() {
    var s []int
    fmt.Println(s, len(s), cap(s))
    if s == nil {
        fmt.Println("nil!")
    }
}
```

## 2.12 make关键字

切片可以由内置函数 [make]来创建，相当于你可以创建动态长度的数组。make 函数分配一个由 [零值]填充的数组，并返回一个引用该数组的切片：

```go
a := make([]int, 5) // len(a)=5
```

要指定容量，可以通过 make 函数第三个参数指定：

```go
b := make([]int, 0, 5) // len(b)=0, cap(b)=5

b = b[:cap(b)]  // len(b)=5, cap(b)=5
b = b[1:]       // len(b)=4, cap(b)=4
```

完整例子如下：

/test/making-slices.go

```go
package main

import "fmt"

func main() {
    a := make([]int, 5)
    printSlice("a", a)

    b := make([]int, 0, 5)
    printSlice("b", b)

    c := b[:2]
    printSlice("c", c)

    d := c[2:5]
    printSlice("d", d)
}

func printSlice(s string, x []int) {
    fmt.Printf("%s len=%d cap=%d %v\n",
        s, len(x), cap(x), x)
}
```

## 2.13 切片的切片

切片可以包含任何类型，当然包括其他切片。

/test/slices-of-slices.go

```go
 package main

 import (
     "fmt"
     "strings"
 )

 func main() {
     // Create a tic-tac-toe board.
     board := [][]string{
         []string{"-", "_", "_"},
         []string{"-", "_", "_"},
         []string{"-", "_", "_"},
     }

     // The players take turns.
     board[0][0] = "X"
     board[2][2] = "O"
     board[1][2] = "X"
     board[1][0] = "O"
     board[0][2] = "X"

     for i := 0; i < len(board); i++ {
         fmt.Printf("%s\n", strings.Join(board[i], " "))
     }
 }
```

## 2.14 元素追加

向切片追加元素是一个很常用的操作，为此 Go 提供了一个 内置函数 。 [内置包文档] 详细描述了这个内置函数 [append](https://golang.org/pkg/builtin/#append) ：

```go
func append(s []T, vs ...T) []T
```

append 函数第一个参数 s 是一个类型为 T 的切片，其余参数均为追加至 s 的 T 元素。append 函数返回一个新切片，包含原切片以及所有追加元素。如果底层数组太小， append 函数会分配一个更大的数组，新切片则指向新数组。

/test/append.go

```go
package main

import "fmt"

func main() {
    var s []int
    printSlice(s)

    // append works on nil slices.
    s = append(s, 0)
    printSlice(s)

    // The slice grows as needed.
    s = append(s, 1)
    printSlice(s)

    // We can add more than one elements at a time.
    s = append(s, 2, 3, 4)
    printSlice(s)
}

func printSlice(s []int) {
    fmt.Printf("len=%d cap=%d %v\n", len(s), cap(s), s)
}
```



## 2.15 遍历

配合 range 关键字， for 循环可对切片进行 遍历 。 下节，我们将看到，这种做法也适用于map。每次迭代都返回两个值，第一个是 下标 ( index )，第二个是与该下标对应的 元素拷贝 。

/test/range.go

```go
package main

import "fmt"

var pow = []int{1, 2, 4, 8, 16, 32, 64, 128}

func main() {
    for i, v := range pow {
        fmt.Printf("2**%d=%d\n", i, v)
    }
}
```



如果无须下标，可以直接赋值给下划线 _ 。 如果只要下标，则不写后半部分即可。

/test/range-continued.go

```go
package main

import "fmt"

func main() {
    pow := make([]int, 10)

    for i := range pow {
        pow[i] = 1 << uint(i)   // == 2**i
    }

    for _, value := range pow {
        fmt.Printf("%d\n", value)
    }
}
```



## 2.16 array

Go 也有数组，[n]T 就表示一个由 n 个类型 T 元素组成的数组类型。下面这个表达式，申明了一个由 10 个整数组成的数组变量：

```go
var a [10]int
```

数组的长度是类型的一部分(不同长度意味着不同类型)，所以数组没有办法调整尺寸。 这看上去很有局限性；然而并不用太担心， Go 提供的方式很方便。

/test/arrays.go

```go
package main

import "fmt"


func main() {
    var a [2]string
    a[0] = "Hello"
    a[1] = "World"
    fmt.Println(a[0], a[1])
    fmt.Println(a)

    primes := [6]int{2, 3, 5, 7, 11, 13}
    fmt.Println(primes)
}
```

## 2.17 pointer

Go 语言也有指针。 指针用来保存一个值的内存地址。类型 *T 就是类型 T 的指针类型。 指针的零值 ( zero value)是:nil 。

```go
var p *int
```

操作符( `operator` ) `&` 用来取被操作数( `operand` )的指针(内存地址)：

```go
i := 42
p = &i
```

操作符 `*` 用来取出指针指向的值：

```go
fmt.Println(*p)
*p = 21
```

这个操作简称取值 (dereferencing)。

/test/pointers.go

```go
package main

import "fmt"


func main() {
    i, j := 42, 2701

    p := &i         // point to i
    fmt.Println(*p) // read i through the pointer

    *p = 21         // set i through the pointer
    fmt.Println(i)  // see the new value of i

    p = &j          // point to j
    *p = *p / 37    // divide j through the pointer
    fmt.Println(j)  // see the new value of j
}
```

注解

与 C 语言不同， Go 语言指针没有指针算术( pointer arithmetic )。

## 2.18 函数值

在 Go 语言，函数也是一种值( C++ 函数对象、Python函数类似)，可以被传递。跟其他普通值一样，函数也可以作为参数传递或作为返回值返回。

/test/function-values.go

```go
package main

import (
    "fmt"
    "math"
)


func compute(fn func(float64, float64) float64) float64 {
    return fn(3, 4)
}


func main() {
    hypot := func(x, y float64) float64 {
        return math.Sqrt(x*x + y*y)
    }
    fmt.Println(hypot(5, 12))

    fmt.Println(compute(hypot))
    fmt.Println(compute(math.Pow))
}
```

## 2.19 闭包

Go函数可以是 闭包 。 闭包是指一个引用外部变量的 [函数值]函数对象。 闭包函数可以访问外部变量，也可以为其赋值。 如此看来，闭包函数相当于与外部变量绑在一起。

/test/function-closures.go

```go
package main

import "fmt"


func adder() func(int) int {
    sum := 0
    return func(x int) int {
        sum += x
        return sum
    }
}


func main() {
    pos, neg := adder(), adder()
    for i := 0; i < 10; i++ {
        fmt.Println(
            pos(i),
            neg(-2*i),
        )
    }
}
```

这个例子， adder函数返回了一个闭包函数。 每个闭包函数都与自己的 sum 变量绑定，互相独立。

## 2.20 方法

Go 语言没有类的概念。 但是，你可以为某个类型定义 方法 ( method )。方法是一个带接收者参数的特殊函数。 接收者参数位于 func 关键字与方法名之间，以括号包围。下面这个例子中，Abs 方法有一个 Vertex 类型的接收者参数 v ：

/test/methods.go

```go
package main

import (
    "fmt"
    "math"
)

type Vertex struct {
    X, Y float64
}

func (v Vertex) Abs() float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func main() {
    v := Vertex{3, 4}
    fmt.Println(v.Abs())
}
```

再次强调： 方法只是一个带有接收者参数的函数而已 。你可以重写 Abs ，将其实现成一个普通函数，功能上并没有任何区别：

/test/methods-funcs.go

```go
package main

import (
    "fmt"
    "math"
)

type Vertex struct {
    X, Y float64
}

func Abs(v Vertex) float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func main() {
    v := Vertex{3, 4}
    fmt.Println(Abs(v))
}
```

## 2.21 非结构体方法

不仅 [结构体] 可以定义方法，其他任何自定义类型均可。以下就是一例，为数值类型 MyFloat定义方法 Abs ：

/test/methods-continued.go

```go
package main

import (
    "fmt"
    "math"
)

type MyFloat float64

func (f MyFloat) Abs() float64 {
    if f < 0 {
        return float64(-f)
    }
    return float64(f)
}

func main() {
    f := MyFloat(-math.Sqrt2)
    fmt.Println(f.Abs())
}
```

方法和对应类型定义必须在同一个包定义。

## 2.22 指针接收者

方法接收者可以定义成指针。这样一来，对于类型 T来说，接收者参数的类型就是 *T 。 需要注意的是， T 本身不能是指针，比如 *int 。例子中， Scale 方法就定义在 *Vertex 上：

/test/methods-pointers.go

```go
 package main

 import (
     "fmt"
     "math"
 )

 type Vertex struct {
     X, Y float64
 }

 func (v Vertex) Abs() float64 {
     return math.Sqrt(v.X*v.X + v.Y*v.Y)
 }

 func (v *Vertex) Scale(f float64) {
     v.X = v.X * f
     v.Y = v.Y * f
 }

 func main() {
     v := Vertex{3, 4}
     v.Scale(10)
     fmt.Println(v.Abs())
 }
```

接收者参数定义成指针的好处是，方法代码可以修改指针指向的值。 由于方法经常需要修改对应的值，因此指针接收者参数相对来说更常用。读者可以自行修改程序，将 * 号从 Scale方法移除，并观察程序行为。 不出意外，你将看到程序输出5 。换句话讲，并没有修改到目标值。 这是为啥呢？如果定义值接收者( value receiver )， Scale 方法相当于在原 Verte 值的一个拷贝上操作(适用于其他参数)。 因此，为了修改 Vertex 值，接收者参数必须定义成指针。

## 2.23 传值与传引用

接下来，我们将 Abs 和 Scale 方法重写成普通函数。

/test/methods-pointers-explained.go

```go
package main

import (
    "fmt"
    "math"
)

type Vertex struct {
    X, Y float64
}

func Abs(v Vertex) float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func Scale(v *Vertex, f float64) {
    v.X = v.X * f
    v.Y = v.Y * f
}

func main() {
    v := Vertex{3, 4}
    Scale(&v, 10)
    fmt.Println(Abs(v))
}
```

同样，将 * 号从 Scale 函数移除会怎样？ 不出意外，结果是类似的。这其实是编程里最经典的 传值 、 传引用问题， 传指针相当于传引用 。

## 2.24 间接传指针

对比上面两个程序，你可能已经注意到了——带指针参数的函数只能传指针：

```go
var v Vertex
ScaleFunc(v, 5)     // Compile error!
ScaleFunc(&v, 5)    // OK
```

然而，对于方法，不管接收者是一个值还是指针，均可调用：

```go
var v Vertex
v.Scale(5)      // OK

p := &v
p.Scale(10)     // OK
```

对于语句 `v.Scale(5)` ，尽管 `v` 是一个值而不是指针，还是自动调用了带指针接收者参数的方法。 这是因为，`Scale` 方法需要指针接收者参数， Go 按照惯例将 `v.Scale(5)` 解释成： `(&v).Scale(5)` 。 这就是 **间接传指针** ，或者叫做 **隐式传指针** 。

/test/indirection.go

```go
package main

import "fmt"

type Vertex struct {
    X, Y float64
}

func (v *Vertex) Scale(f float64) {
    v.X = v.X * f
    v.Y = v.Y * f
}

func ScaleFunc(v *Vertex, f float64) {
    v.X = v.X * f
    v.Y = v.Y * f
}

func main() {
    v := Vertex{3, 4}
    v.Scale(2)
    ScaleFunc(&v, 10)

    p := &Vertex{4, 3}
    p.Scale(3)
    ScaleFunc(p, 8)

    fmt.Println(v, p)
}
```

## 2.25 间接传值

对普通 [函数] 来说，值参数只能传对应类型的值，传指针则导致编译错误：

```go
var v Vertex
fmt.Println(AbsFunc(v))     // OK
fmt.Println(AbsFunc(&v))    // Compile error!
```

相反，就算方法定义了值接收者参数，用指针调用也是可以的：

```go
var v Vertex
fmt.Println(v.Abs())    // OK

p := &v
fmt.Println(p.Abs())    // OK
```

在这，方法调用语句 p.Abs()则被解释成： (*p).Abs() 。 这就是间接传值，或者叫做隐式传值。

/test/indirection-values.go

```go
package main

import (
    "fmt"
    "math"
)

type Vertex struct {
    X, Y float64
}

func (v Vertex) Abs() float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func AbsFunc(v Vertex) float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func main() {
    v := Vertex{3, 4}
    fmt.Println(v.Abs())
    fmt.Println(AbsFunc(v))

    p := &Vertex{4, 3}
    fmt.Println(p.Abs())
    fmt.Println(AbsFunc(p))
}
```

## 2.26 传值还是传指针

那么，接收者参数到底是实现成值还是指针呢？ 如何选择？使用指针接收者参数主要有两方面考虑：首先，只有这种方式能够对指向的值进行修改。其次，从性能方面考虑，使用指针可以避免在每次调用方法时拷贝值。 这种方式相对来说更高效，特别是当接收者 [结构体]很大很复杂时。在这个例子， Scale 方法和Abs方法接收者参数类型均为 *Vertex，尽管 Abs 方法并不修改其接收者：

/test/methods-with-pointer-receivers.go

```go
package main

import (
    "fmt"
    "math"
)

type Vertex struct {
    X, Y float64
}

func (v *Vertex) Scale(f float64) {
    v.X = v.X * f
    v.Y = v.Y * f
}

func (v *Vertex) Abs() float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func main() {
    v := Vertex{3, 4}
    fmt.Println("Before scaling: %+v, Abs: %v\n", v, v.Abs())
    v.Scale(5)
    fmt.Println("After scaling: %+v, Abs: %v\n", v, v.Abs())
}
```

通常，不管为何种类型编写方法，均需要定义 **值接收者** 或者 **指针接收者** ，不能混用。

## 2.27 小节

# 第3章 Golang分支开发

## 3.1 if

跟 for 语句一样， if 语句条件表达式不需要括号包围，但是花括号却不能省略。

/test/if.go

```go
package main

import (
    "fmt"
    "math"
)


func sqrt(x float64) string {
    if x < 0 {
        return sqrt(-x) + "i"
    }
    return fmt.Sprint(math.Sqrt(x))
}


func main() {
    fmt.Println(sqrt(2), sqrt(-4))
}
```

## 3.2 初始语句

if 语句同样支持初始化语句，在条件表达式求值之前执行。 初始化语句一般都是 := 赋值语句。

/test/if-with-a-short-statement.go

```go
package main

import (
    "fmt"
    "math"
)


func pow(x, n, lim float64) float64 {
    if v := math.Pow(x, n); v < lim {
        return v
    }
    return lim
}


func main() {
    fmt.Println(
        pow(3, 2, 10),
        pow(3, 3, 20),
    )
}
```

在初始语句中申明的变量，只在 if 结构中可见。

## 3.3 if-else 语句

在初始化语句定义的变量，在 else代码块也是可见的。

/test/if-and-else.go

```go
package main

import (
    "fmt"
    "math"
)


func pow(x, n, lim float64) float64 {
    if v := math.Pow(x, n); v < lim {
        return v
    } else {
        fmt.Printf("%g >= %g\n", v, lim)
    }
    // can't use v here, though
    return lim
}


func main() {
    fmt.Println(
        pow(3, 2, 10),
        pow(3, 3, 20),
    )
}
```

注解

main 函数中两次 pow 调用都在 fmt.Println 调用之前执行。 因为，调用 fmt.Println 前，需要对参数进行求值。

## 3.4 for

Go 只有一种循环结构—— for 循环。

最基本的 for 语句包含 3 部分，以分号 `;` 分隔：

- **初始语句** ：在第一次迭代判断之前；
- **条件语句(表达式)** ：在每次迭代前求值并判断；
- **迭代后语句** ：在每次迭代后执行；

```go
for 初始语句; 条件语句; 迭代后语句 {
    代码体
}
```

当条件表达式求值为 false 时，循环将停止迭代并退出。

/test/for.go

```go
package main

import "fmt"


func main() {
    sum := 0
    for i := 0; i < 10; i++ {
        sum += i
    }
    fmt.Println(sum)
}
```

注解

跟 C 、 Java 或者 JavaScript 等其他语言不同， Go 语言 for 语句 3 部分不需要用括号包住， 但花括号是必要的，任何时候都不能省略 。另外，与其他语言类似，初始语句与迭代后语句也是可选的：

/test/for-continued.go

```
package main

import "fmt"

func main() {
    sum := 1
    for ; sum < 1000; {
        sum += sum
    }
    fmt.Println(sum)
}
```

实际上， Go 也是支持 while 语句的，只不过关键字还换成 for ：

/test/for-is-gos-while.go

```go
package main

import "fmt"


func main() {
    sum := 1
    for sum < 1000 {
        sum += sum
    }
    fmt.Println(sum)
}
```

## 3.5 无限循环

如果省略循环条件，循环将永远执行 。 这种循环就是众所周知的死循环，也叫做无限循环。 对我来说，我更愿意用无限循环。 因为， 循环更应该用在程序有问题，循环行为不符合作者预期的场景。无限循环是 Go 语言中最紧凑的循环结构：

/test/forever.go

```go
package main


func main() {
    for {
    }
}
```

警告

使用无限循环时要特别小心！

## 3.6 switch

switch 语句也是一种经典控制语句，可以看做是 if-else 语句链的简写。

/test/switch.go

```go
package main

import (
    "fmt"
    "runtime"
)


func main() {
    fmt.Print("Go runs on ")

    switch os := runtime.GOOS; os {
        case "darwin":
            fmt.Println("OS X.")

        case "linux":
            fmt.Println("Linux.")

        default:
            // freebsd, openbsd
            // plan9, windows...
            fmt.Printf("%s.\n", os)
    }
}
```

Go 语言 switch 结构跟 C 、 C++ 、 Java 、 JavaScript 以及 PHP 等类似， 不同的是， Go 只执行匹配的 case 代码体，不包括下面的。 对于其他语言，一般需要在每个 case 末尾处用 break 语句来结束。 实际上， Go 相当于自动在每个 case 末尾添加了 break 语句， 这避免了大量因为漏掉 break 而导致的错误。

另外， Go 语言 switch 更为灵活， case 条件不必是常量，也不必是整数。

## 3.7 检查顺序

switch 从上往下对 case 进行检查，直到匹配。

/test/switch-evaluation-order.go

```go
package main

import (
    "fmt"
    "time"
)


func main() {
    fmt.Println("When's Saturday?")
    today := time.Now().Weekday()
    switch time.Saturday {
        case today + 0:
            fmt.Println("Today.")
        case today + 1:
            fmt.Println("Tomorrow.")
        case today + 2:
            fmt.Println("In two days.")
        default:
            fmt.Println("Too far away.")
    }
}
```

举另一个例子，如果 i 的值为零，那么函数 f 就不会被调用了：

```go
switch i {
    case 0:
    case f():
}
```

## 3.8 省略条件

在 Go 语言， switch 条件可以省略，等价于switch true 。 这种结构非常简洁，可以用来代替过长的 if-else 链。

/test/switch-with-no-condition.go

```go
package main

import (
    "fmt"
    "time"
)


func main() {
    t := time.Now()
    switch {
        case t.Hour() < 12:
            fmt.Println("Good morning!")
        case t.Hour() < 17:
            fmt.Println("Good afternoon.")
        default:
            fmt.Println("Good evening.")
    }
}
```

## 3.9 defer

defer语句将函数执行推迟到调用函数(包含函数)退出。 函数调用参数还是立马求值，只是执行推迟而已。你可能已经猜到这个程序输出什么了：

/test/defer.go

```go
package main

import "fmt"


func main() {
    defer fmt.Println("world")

    fmt.Println("hello")
}
```

对，就是这么简单！

## 3.10 defer栈

与函数调用类似，推迟执行的函数调用也被推到一个栈。 当函数返回时，这些被推迟执行的函数调用将被执行，以后进先出(last-in-first-out )的顺序。

/test/defer-multi.go

```go
package main

import "fmt"


func main() {
    fmt.Println("counting")

    for i := 0; i < 10; i++ {
        defer fmt.Println(i)
    }

    fmt.Println("done")
}
```

## 3.11 小节

# 第4章 Golang并发编程

## 4.1并发之道协程

A *goroutine* is a lightweight thread managed by the Go runtime.

```
go f(x, y, z)
```

starts a new goroutine running

```
f(x, y, z)
```

The evaluation of `f`, `x`, `y`, and `z` happens in the current goroutine and the execution of `f` happens in the new goroutine.

Goroutines run in the same address space, so access to shared memory must be synchronized. The [`sync`](https://golang.org/pkg/sync/) package provides useful primitives, although you won't need them much in Go as there are other primitives. (See the next slide.)

```
package main

import (
	"fmt"
	"time"
)

func say(s string) {
	for i := 0; i < 5; i++ {
		time.Sleep(100 * time.Millisecond)
		fmt.Println(s)
	}
}

func main() {
	go say("world")
	say("hello")
}
```



## 4.2 并发之道channel 

Channels are a typed conduit through which you can send and receive values with the channel operator, `<-`.

```
ch <- v    // Send v to channel ch.
v := <-ch  // Receive from ch, and
           // assign value to v.
```

(The data flows in the direction of the arrow.)

Like maps and slices, channels must be created before use:

```
ch := make(chan int)
```

By default, sends and receives block until the other side is ready. This allows goroutines to synchronize without explicit locks or condition variables.

The example code sums the numbers in a slice, distributing the work between two goroutines. Once both goroutines have completed their computation, it calculates the final result.

```
package main

import "fmt"

func sum(s []int, c chan int) {
	sum := 0
	for _, v := range s {
		sum += v
	}
	c <- sum // send sum to c
}

func main() {
	s := []int{7, 2, 8, -9, 4, 0}

	c := make(chan int)
	go sum(s[:len(s)/2], c)
	go sum(s[len(s)/2:], c)
	x, y := <-c, <-c // receive from c
	
	fmt.Println(x, y, x+y)

}
```



## 4.3 管道缓存之Buffered Channels

Channels can be *buffered*. Provide the buffer length as the second argument to `make` to initialize a buffered channel:

```
ch := make(chan int, 100)
```

Sends to a buffered channel block only when the buffer is full. Receives block when the buffer is empty.

Modify the example to overfill the buffer and see what happens.

```
package main

import "fmt"

func main() {
	ch := make(chan int, 2)
	ch <- 1
	ch <- 2
	fmt.Println(<-ch)
	fmt.Println(<-ch)
}
```



## 4.4 多路复用之select

The `select` statement lets a goroutine wait on multiple communication operations.

A `select` blocks until one of its cases can run, then it executes that case. It chooses one at random if multiple are ready.

```
package main

import "fmt"

func fibonacci(c, quit chan int) {
	x, y := 0, 1
	for {
		select {
		case c <- x:
			x, y = y, x+y
		case <-quit:
			fmt.Println("quit")
			return
		}
	}
}

func main() {
	c := make(chan int)
	quit := make(chan int)
	go func() {
		for i := 0; i < 10; i++ {
			fmt.Println(<-c)
		}
		quit <- 0
	}()
	fibonacci(c, quit)
}
```



## 4.5 管道之Range和Close

A sender can `close` a channel to indicate that no more values will be sent. Receivers can test whether a channel has been closed by assigning a second parameter to the receive expression: after

```
v, ok := <-ch
```

`ok` is `false` if there are no more values to receive and the channel is closed.

The loop `for i := range c` receives values from the channel repeatedly until it is closed.

**Note:** Only the sender should close a channel, never the receiver. Sending on a closed channel will cause a panic.

**Another note:** Channels aren't like files; you don't usually need to close them. Closing is only necessary when the receiver must be told there are no more values coming, such as to terminate a `range` loop.

```
package main

import (
	"fmt"
)

func fibonacci(n int, c chan int) {
	x, y := 0, 1
	for i := 0; i < n; i++ {
		c <- x
		x, y = y, x+y
	}
	close(c)
}

func main() {
	c := make(chan int, 10)
	go fibonacci(cap(c), c)
	for i := range c {
		fmt.Println(i)
	}
}
```



## 4.6 管道Default Selection

The `default` case in a `select` is run if no other case is ready.

Use a `default` case to try a send or receive without blocking:

```
select {
case i := <-c:
    // use i
default:
    // receiving from c would block
}
```

```
package main

import (
	"fmt"
	"time"
)

func main() {
	tick := time.Tick(100 * time.Millisecond)
	boom := time.After(500 * time.Millisecond)
	for {
		select {
		case <-tick:
			fmt.Println("tick.")
		case <-boom:
			fmt.Println("BOOM!")
			return
		default:
			fmt.Println("    .")
			time.Sleep(50 * time.Millisecond)
		}
	}
}
```



## 4.7 Golang二叉树之一

There can be many different binary trees with the same sequence of values stored in it. For example, here are two binary trees storing the sequence 1, 1, 2, 3, 5, 8, 13.

![img](https://tour.golang.org/content/img/tree.png)

A function to check whether two binary trees store the same sequence is quite complex in most languages. We'll use Go's concurrency and channels to write a simple solution.

This example uses the `tree` package, which defines the type:

```
type Tree struct {
    Left  *Tree
    Value int
    Right *Tree
}
```

## 4.8 Golang二叉树之二

**1.** Implement the `Walk` function.

**2.** Test the `Walk` function.

The function `tree.New(k)` constructs a randomly-structured (but always sorted) binary tree holding the values `k`, `2k`, `3k`, ..., `10k`.

Create a new channel `ch` and kick off the walker:

```
go Walk(tree.New(1), ch)
```

Then read and print 10 values from the channel. It should be the numbers 1, 2, 3, ..., 10.

**3.** Implement the `Same` function using `Walk` to determine whether `t1` and `t2` store the same values.

**4.** Test the `Same` function.

`Same(tree.New(1), tree.New(1))` should return true, and `Same(tree.New(1), tree.New(2))` should return false.

The documentation for `Tree` can be found [here](https://godoc.org/golang.org/x/tour/tree#Tree).



```
package main

import "golang.org/x/tour/tree"

// Walk walks the tree t sending all values
// from the tree to the channel ch.
func Walk(t *tree.Tree, ch chan int)

// Same determines whether the trees
// t1 and t2 contain the same values.
func Same(t1, t2 *tree.Tree) bool

func main() {
}
```



## 4.9 锁

We've seen how channels are great for communication among goroutines.

But what if we don't need communication? What if we just want to make sure only one goroutine can access a variable at a time to avoid conflicts?

This concept is called *mutual exclusion*, and the conventional name for the data structure that provides it is *mutex*.

Go's standard library provides mutual exclusion with [`sync.Mutex`](https://golang.org/pkg/sync/#Mutex) and its two methods:

- `Lock`
- `Unlock`

We can define a block of code to be executed in mutual exclusion by surrounding it with a call to `Lock` and `Unlock` as shown on the `Inc` method.

We can also use `defer` to ensure the mutex will be unlocked as in the `Value` method.

```go
package main

import (
	"fmt"
	"sync"
	"time"
)

// SafeCounter is safe to use concurrently.
type SafeCounter struct {
	mu sync.Mutex
	v  map[string]int
}

// Inc increments the counter for the given key.
func (c *SafeCounter) Inc(key string) {
	c.mu.Lock()
	// Lock so only one goroutine at a time can access the map c.v.
	c.v[key]++
	c.mu.Unlock()
}

// Value returns the current value of the counter for the given key.
func (c *SafeCounter) Value(key string) int {
	c.mu.Lock()
	// Lock so only one goroutine at a time can access the map c.v.
	defer c.mu.Unlock()
	return c.v[key]
}

func main() {
	c := SafeCounter{v: make(map[string]int)}
	for i := 0; i < 1000; i++ {
		go c.Inc("somekey")
	}

	time.Sleep(time.Second)
	fmt.Println(c.Value("somekey"))

}
```

## 4.10 小节

本小节主要是介绍go高级用法
