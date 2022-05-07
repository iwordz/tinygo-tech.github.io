<<<<<<< HEAD
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



=======
>>>>>>> 0d8dd3f1be01f19fe0ca8e7eec1f2bfbff82d101
# 目录

[toc]

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
