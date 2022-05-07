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
- [第5章 注册配置中心实现机制](#%E7%AC%AC5%E7%AB%A0-%E6%B3%A8%E5%86%8C%E9%85%8D%E7%BD%AE%E4%B8%AD%E5%BF%83%E5%AE%9E%E7%8E%B0%E6%9C%BA%E5%88%B6)
  - [5.1 注册中心的介绍](#51-%E6%B3%A8%E5%86%8C%E4%B8%AD%E5%BF%83%E7%9A%84%E4%BB%8B%E7%BB%8D)
    - [几大主流注册中心介绍](#%E5%87%A0%E5%A4%A7%E4%B8%BB%E6%B5%81%E6%B3%A8%E5%86%8C%E4%B8%AD%E5%BF%83%E4%BB%8B%E7%BB%8D)
      - [zookeeper](#zookeeper)
      - [Eureka](#eureka)
      - [Nacos](#nacos)
      - [Consul](#consul)
      - [注册中心功能大比拼](#%E6%B3%A8%E5%86%8C%E4%B8%AD%E5%BF%83%E5%8A%9F%E8%83%BD%E5%A4%A7%E6%AF%94%E6%8B%BC)
  - [5.2 注册中心的安装](#52-%E6%B3%A8%E5%86%8C%E4%B8%AD%E5%BF%83%E7%9A%84%E5%AE%89%E8%A3%85)
  - [5.3 编写第一个handler](#53-%E7%BC%96%E5%86%99%E7%AC%AC%E4%B8%80%E4%B8%AAhandler)
  - [5.4 配置中心和注册中心使用](#54-%E9%85%8D%E7%BD%AE%E4%B8%AD%E5%BF%83%E5%92%8C%E6%B3%A8%E5%86%8C%E4%B8%AD%E5%BF%83%E4%BD%BF%E7%94%A8)
  - [5.5 完善consul配置](#55-%E5%AE%8C%E5%96%84consul%E9%85%8D%E7%BD%AE)
  - [5.6 小节](#56-%E5%B0%8F%E8%8A%82)
- [第6章 链路追踪系统简介](#%E7%AC%AC6%E7%AB%A0-%E9%93%BE%E8%B7%AF%E8%BF%BD%E8%B8%AA%E7%B3%BB%E7%BB%9F%E7%AE%80%E4%BB%8B)
  - [6.1 Zipkin介绍](#61-zipkin%E4%BB%8B%E7%BB%8D)
  - [6.2 GO中使用zipkin](#62-go%E4%B8%AD%E4%BD%BF%E7%94%A8zipkin)
  - [6.3 TinyGo中service使用zipkin](#63-tinygo%E4%B8%ADservice%E4%BD%BF%E7%94%A8zipkin)
  - [6.4 链路追逐使用](#64-%E9%93%BE%E8%B7%AF%E8%BF%BD%E9%80%90%E4%BD%BF%E7%94%A8)
  - [6.5 小节](#65-%E5%B0%8F%E8%8A%82)
- [第7章熔断、限流、负载均衡](#%E7%AC%AC7%E7%AB%A0%E7%86%94%E6%96%AD%E9%99%90%E6%B5%81%E8%B4%9F%E8%BD%BD%E5%9D%87%E8%A1%A1)
  - [7.1 熔断器作用和原理](#71-%E7%86%94%E6%96%AD%E5%99%A8%E4%BD%9C%E7%94%A8%E5%92%8C%E5%8E%9F%E7%90%86)
  - [7.2 限流的作用和原理](#72-%E9%99%90%E6%B5%81%E7%9A%84%E4%BD%9C%E7%94%A8%E5%92%8C%E5%8E%9F%E7%90%86)
  - [7.3 负载均衡的作用和原理](#73-%E8%B4%9F%E8%BD%BD%E5%9D%87%E8%A1%A1%E7%9A%84%E4%BD%9C%E7%94%A8%E5%92%8C%E5%8E%9F%E7%90%86)
  - [7.4 使用TinyGo快速实现API微服务网关](#74-%E4%BD%BF%E7%94%A8tinygo%E5%BF%AB%E9%80%9F%E5%AE%9E%E7%8E%B0api%E5%BE%AE%E6%9C%8D%E5%8A%A1%E7%BD%91%E5%85%B3)
  - [7.5 熔断在TinyGO中使用案例](#75-%E7%86%94%E6%96%AD%E5%9C%A8tinygo%E4%B8%AD%E4%BD%BF%E7%94%A8%E6%A1%88%E4%BE%8B)
  - [7.6 小节](#76-%E5%B0%8F%E8%8A%82)
- [第8章微服务性能监控](#%E7%AC%AC8%E7%AB%A0%E5%BE%AE%E6%9C%8D%E5%8A%A1%E6%80%A7%E8%83%BD%E7%9B%91%E6%8E%A7)
  - [8.1 微服务监控和传统监控介绍](#81-%E5%BE%AE%E6%9C%8D%E5%8A%A1%E7%9B%91%E6%8E%A7%E5%92%8C%E4%BC%A0%E7%BB%9F%E7%9B%91%E6%8E%A7%E4%BB%8B%E7%BB%8D)
  - [8.2 TinyGO如何快速增加promethous监控](#82-tinygo%E5%A6%82%E4%BD%95%E5%BF%AB%E9%80%9F%E5%A2%9E%E5%8A%A0promethous%E7%9B%91%E6%8E%A7)
  - [8.3 promethous指标关键指标设置](#83-promethous%E6%8C%87%E6%A0%87%E5%85%B3%E9%94%AE%E6%8C%87%E6%A0%87%E8%AE%BE%E7%BD%AE)
  - [8.4 小节](#84-%E5%B0%8F%E8%8A%82)
- [第9章微服务日志收集](#%E7%AC%AC9%E7%AB%A0%E5%BE%AE%E6%9C%8D%E5%8A%A1%E6%97%A5%E5%BF%97%E6%94%B6%E9%9B%86)
  - [9.1 ELK原理](#91-elk%E5%8E%9F%E7%90%86)
  - [9.2 Filebeat原理](#92-filebeat%E5%8E%9F%E7%90%86)
  - [9.3 Logstash原理](#93-logstash%E5%8E%9F%E7%90%86)
  - [9.4 docker-co mpose安装ELK](#94-docker-co-mpose%E5%AE%89%E8%A3%85elk)
  - [9.5 TinyGo封装zap](#95-tinygo%E5%B0%81%E8%A3%85zap)
  - [9.6 Kibana可视化](#96-kibana%E5%8F%AF%E8%A7%86%E5%8C%96)
  - [9.7小节](#97%E5%B0%8F%E8%8A%82)
- [第10章 自研微服务tgo框架](#%E7%AC%AC10%E7%AB%A0-%E8%87%AA%E7%A0%94%E5%BE%AE%E6%9C%8D%E5%8A%A1tgo%E6%A1%86%E6%9E%B6)
  - [5.1 什么是微服务？](#51-%E4%BB%80%E4%B9%88%E6%98%AF%E5%BE%AE%E6%9C%8D%E5%8A%A1)
  - [5.2 常见微服务框架](#52-%E5%B8%B8%E8%A7%81%E5%BE%AE%E6%9C%8D%E5%8A%A1%E6%A1%86%E6%9E%B6)
    - [5.2.1 Spring Cloud](#521-spring-cloud)
    - [5.2.2 Dubbo](#522-dubbo)
    - [5.2.3 Dropwizard](#523-dropwizard)
    - [5.2.4 Go-Kit](#524-go-kit)
  - [5.3 TinyGO微服务代码实例](#53-tinygo%E5%BE%AE%E6%9C%8D%E5%8A%A1%E4%BB%A3%E7%A0%81%E5%AE%9E%E4%BE%8B)
    - [5.3.1 网关启动程序](#531-%E7%BD%91%E5%85%B3%E5%90%AF%E5%8A%A8%E7%A8%8B%E5%BA%8F)
    - [5.3.2 使用TinyGO进行微服务模块开发](#532-%E4%BD%BF%E7%94%A8tinygo%E8%BF%9B%E8%A1%8C%E5%BE%AE%E6%9C%8D%E5%8A%A1%E6%A8%A1%E5%9D%97%E5%BC%80%E5%8F%91)
    - [5.3.4 TinyGO微服务如何启动？](#534-tinygo%E5%BE%AE%E6%9C%8D%E5%8A%A1%E5%A6%82%E4%BD%95%E5%90%AF%E5%8A%A8)
  - [5.4 TinyGo框架介绍](#54-tinygo%E6%A1%86%E6%9E%B6%E4%BB%8B%E7%BB%8D)
    - [5.4.1 框架介绍](#541-%E6%A1%86%E6%9E%B6%E4%BB%8B%E7%BB%8D)
    - [5.4.2 框架基本使用](#542-%E6%A1%86%E6%9E%B6%E5%9F%BA%E6%9C%AC%E4%BD%BF%E7%94%A8)
      - [5.4.2.1 初始化项目](#5421-%E5%88%9D%E5%A7%8B%E5%8C%96%E9%A1%B9%E7%9B%AE)
    - [5.4.2.2 代码生成](#5422-%E4%BB%A3%E7%A0%81%E7%94%9F%E6%88%90)
    - [5.4.2.3 限流配置](#5423-%E9%99%90%E6%B5%81%E9%85%8D%E7%BD%AE)
    - [5.4.2.4 初始化路由方法](#5424-%E5%88%9D%E5%A7%8B%E5%8C%96%E8%B7%AF%E7%94%B1%E6%96%B9%E6%B3%95)
    - [5.4.2.5 Golang对象池使用](#5425-golang%E5%AF%B9%E8%B1%A1%E6%B1%A0%E4%BD%BF%E7%94%A8)
      - [5.4.2.6 Redis使用方法](#5426-redis%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95)
      - [5.4.2.7 MySQL使用方法](#5427-mysql%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95)
      - [5.4.2.8 logger使用方法](#5428-logger%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95)
    - [5.5 框架基础结构介绍](#55-%E6%A1%86%E6%9E%B6%E5%9F%BA%E7%A1%80%E7%BB%93%E6%9E%84%E4%BB%8B%E7%BB%8D)
    - [5.4.3 运行程序](#543-%E8%BF%90%E8%A1%8C%E7%A8%8B%E5%BA%8F)
      - [5.4.3.1 运行](#5431-%E8%BF%90%E8%A1%8C)
      - [5.4.3.2 远程配置模式](#5432-%E8%BF%9C%E7%A8%8B%E9%85%8D%E7%BD%AE%E6%A8%A1%E5%BC%8F)
      - [5.4.3.3 本地配置文件模式](#5433-%E6%9C%AC%E5%9C%B0%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%E6%A8%A1%E5%BC%8F)
    - [5.4.4.参数验证基础库](#544%E5%8F%82%E6%95%B0%E9%AA%8C%E8%AF%81%E5%9F%BA%E7%A1%80%E5%BA%93)
      - [在entity目录下req.go文件写入,构造请求参数校验即可。](#%E5%9C%A8entity%E7%9B%AE%E5%BD%95%E4%B8%8Breqgo%E6%96%87%E4%BB%B6%E5%86%99%E5%85%A5%E6%9E%84%E9%80%A0%E8%AF%B7%E6%B1%82%E5%8F%82%E6%95%B0%E6%A0%A1%E9%AA%8C%E5%8D%B3%E5%8F%AF)
      - [具体如何使用请看 github.com/go-playground/validator/v10,使用案例如何](#%E5%85%B7%E4%BD%93%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E8%AF%B7%E7%9C%8B-githubcomgo-playgroundvalidatorv10%E4%BD%BF%E7%94%A8%E6%A1%88%E4%BE%8B%E5%A6%82%E4%BD%95)
  - [5.5 小节](#55-%E5%B0%8F%E8%8A%82)
  - [](#)

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

# 第5章 注册配置中心实现机制

## 5.1 注册中心的介绍

提到注册中心概念相比大家并不陌生,注册中心是互联网业务中最重要的中间件之一，主要用来做微服务中服务注册和服务发现，说到这个, 先扯一下服务发现, 当我们的系统服务从单机时代走向分布式时代的时候, 其实就衍生了服务发现需求，最早大家的服务发现是通DNS协议实现的, 就是网路IP协议, 通过DNS + LVS基本就实现了http形式的服务发现, 这个时候IP通常是配置在LVS.之后大家开始玩起RPC服务, 服务的部署开始频繁.为了实现动态上下线, 后来出现注册中心目的其实就是推送IP列.下面通过一张图说明一下注册中心工作流程:

![img](https://s2.ax1x.com/2020/03/05/3TXlKP.gif)

如上图清晰的表达了注册中心的交互过程, 体现出三种角色之间关系:

- 服务提供者 Service Provider (Server):
  - 服务启动后向RegistryCenter**注册**自己的一个实例
  - 定期向RegistryCenter发送**心跳**(heartbeat), 证明自己还能苟一会
  - 服务关闭时向RegistryCenter发起注销
- 服务消费者 Service Consumer(Client):
  - 服务启动后RegistryCenter订阅所需要使用的服务(Server), 并缓存到实例列表中
  - 向对应服务(Server)发起**调用**时,从内存中的该服务的实例列表选择一个,进行远程调用.
  - 服务关闭时向RegistryCenter取消订阅
- 注册中心 Service Registry Center:
  - Server超过一定时间未**心跳**时,从服务的实例列表移除.
  - 服务的实例列表发生变化(新增或者移除)时,通知订阅该服务的 Consumer,从而让 Consumer 能够刷新本地缓存. 有些 注册中心不提供这项功能, 例如Eureka,二手Client 定期轮询更新本地缓存

### 几大主流注册中心介绍

#### zookeeper

Zoopkeeper 在国内很长一段时间都是注册中心一哥.大部分是因为Dubbo 在国能的盛行。

#### Eureka

Eureka是一家在线影片租赁提供商Netflix开源的, 这家公司的理念还是满超前的.

很多Spring Cloud的组件都是Netflix做的, 这是Netflix的微服务生态.方便Spring开发人员构建微服务基础框架.而Eureka则借着微服务概念的流行,与SpringCloud生态的深度结合,也获取了大量的粉丝。

#### Nacos

Nacos 是阿里开源的, 功能其实也很多, 服务注册, 配置管理, 动态 DNS 服务, 元数据管理。

#### Consul

Consul 是 HashiCorp 公司推出的开源工具，用于实现分布式系统的服务发现与配置。Consul 是分布式的、高可用的、 可横向扩展的。

#### 注册中心功能大比拼

|                  | Nacos                     | Eureka     | Consul            | zookeeper  |
| ---------------- | ------------------------- | ---------- | ----------------- | ---------- |
| 数据一致性       | AP/CP                     | AP         | CP                | CP         |
| 健康检查         | TCP/HTTP/MySql/ClientBeat | ClientBeat | TCP/HTTP/grpc/Cmd | Keep Alive |
| 负载均衡策略     | 权重/metadata/Selector    | Ribbon     | Fabio             | -          |
| 雪崩保护         | 有                        | 有         | 无                | 无         |
| 容量             | 100w                      | 5000       | 百万级            | 百万级     |
| 自动注销实例     | √                         | √          | ×                 | √          |
| 访问协议         | HTTP/DNS                  | HTTP       | HTTP/DNS          | TCP        |
| 监听支持         | √                         | √          | √                 | √          |
| 多数据中心       | √                         | √          | √                 | ×          |
| 跨注册中心同步   | √                         | ×          | √                 | ×          |
| Spring Cloud集成 | √                         | √          | √                 | ×          |
| Dubbo集成        | √                         | ×          | ×                 | √          |
| K8s集成          | √                         | ×          | √                 | ×          |

## 5.2 注册中心的安装

本节主要Consul工具

## 5.3 编写第一个handler



## 5.4 配置中心和注册中心使用



## 5.5 完善consul配置



## 5.6 小节

这篇文章盘点注册中心各自的特性,主要有以下的特性。

- Nacos大而全
- Eureka 小而美
- Consul其实跟Nacos比较相似.
- zookeeper 性能好难扩展

# 第6章 链路追踪系统简介

## 6.1 Zipkin介绍

## 6.2 GO中使用zipkin

## 6.3 TinyGo中service使用zipkin

## 6.4 链路追逐使用

## 6.5 小节

# 第7章熔断、限流、负载均衡

## 7.1 熔断器作用和原理

## 7.2 限流的作用和原理

## 7.3 负载均衡的作用和原理

## 7.4 使用TinyGo快速实现API微服务网关

## 7.5 熔断在TinyGO中使用案例

## 7.6 小节

# 第8章微服务性能监控

## 8.1 微服务监控和传统监控介绍

## 8.2 TinyGO如何快速增加promethous监控

## 8.3 promethous指标关键指标设置

## 8.4 小节

# 第9章微服务日志收集

## 9.1 ELK原理

## 9.2 Filebeat原理

## 9.3 Logstash原理

## 9.4 docker-co mpose安装ELK

## 9.5 TinyGo封装zap

## 9.6 Kibana可视化

## 9.7小节



# 第10章 自研微服务tgo框架

## 5.1 什么是微服务？

微服务是一种用于构建应用的架构方案。微服务架构有别于更为传统的单体式方案，可将应用拆分成多个核心功能。每个功能都被称为一项服务，可以单独构建和部署，这意味着各项服务在工作（和出现故障）时不会相互影响。也是一种开发软件的架构和组织方法，其中软件由通过明确定义的 API 进行通信的小型独立服务组成。这些服务由各个小型独立团队负责。微服务架构使应用程序更易于扩展和更快地开发，从而加速创新并缩短新功能的上市时间。微服务可通过分布式部署，大幅提升您的团队和日常工作效率。您还可以并行开发多个微服务。这意味着更多开发人员可以同时开发同一个应用，进而缩短开发所需的时间。

加速做好面市准备

由于开发周期缩短，微服务架构有助于实现更加敏捷的部署和更新。

高度可扩展

随着某些服务的不断扩展，您可以跨多个服务器和基础架构进行部署，充分满足自身需求。

出色的弹性

只要确保正确构建，这些独立的服务就不会彼此影响。这意味着，一个服务出现故障不会导致整个应用下线，这一点与单体式应用模型不同。

易于部署

相对于传统的单体式应用，基于微服务的应用更加模块化且小巧，所以您无需为它们的部署操心。虽然对部署时的协作要求更高，但之后能获得巨大回报。

易于访问

由于大型应用被拆分成了多个小型服务，所以开发人员能够更加轻松地理解、更新和增强这些服务，从而缩短开发周期（尤其是在搭配使用敏捷的开发方法时）。

更加开放

由于使用了多语言 API，所以开发人员可以根据需要实现的功能，自由选用最适合的语言和技术。

------

所面临的挑战

如果您的企业正在考虑迁移到微服务架构，那么不仅是应用要变，相关人员的工作方式也会随之而变。在某种意义上，改变企业和文化[并不容易](https://www.redhat.com/zh/blog/state-microservices)，因为每个团队都有自己的部署节奏和所负责的服务，而且这些服务都拥有自己的客户群。这些可能并不是开发人员通常要担心的问题，但是这些问题却决定了微服务架构能否取得成功。微服务的八类挑战：

1. **构建：**您必须花时间明确各个服务间的依赖关系。要知道，由于存在这些依赖关系，当您完成一个构建时，可能会触发多个其他构建。您还需要考虑微服务[对于数据的影响]。
2. **测试：** 集成测试和端到端测试可能会前所未有的难以实施，但却更加重要。根据您在架构相互支撑的服务时所采用的不同方式，架构中的一个部分出现故障，很可能会导致其他部分也随之出现故障。
3. **版本管理：**在更新到新版本时，请记住：向后兼容性可能会因更新操作而失效。要解决这一问题，您可以利用条件逻辑来进行构建，但是构建会变得繁复、难以控制且快速。或者，您也可以为不同的客户端维护多个活跃版本，但是相关的维护和管理工作会变得更加庞杂。
4. **部署：**没错，这也是一大挑战，至少是首次设置时所要面临的一大挑战。为了简化部署，您必须先大量投资[自动化](https://www.redhat.com/zh/topics/automation)，因为人工部署无法应对微服务的复杂性。请好好思考您要以何种方式以及怎样的顺序来部署各项服务。
5. **日志记录：**使用分布式系统时，您需要利用集中式日志将所有相关信息集中到一处。否则，积累的日志数量将让您难以招架。
6. **监控：**您必须通过一个集中式视图来了解整个系统的情况，以便找出问题的根源。
7. **调试：**无法进行远程调试，因为这种方式无法涵盖数十个或数百个服务。不幸的是，关于应该如何进行调试，目前还没有标准答案。
8. **连接：**请考虑使用服务探索功能，无论是集中式的还是集成式。

## 5.2 常见微服务框架

### 5.2.1 Spring Cloud

Spring Cloud是一个系列框架的合计，基于HTTP的RETS服务构建服务体系，Spring Cloud能够帮助架构师构建一整套完整的微服务架构技术生态链。

### 5.2.2 Dubbo

Dubbo是由阿里巴巴开源的分布式服务化治理框架，通过RPC请求方式访问。Dubbo是在阿里巴巴的电商平台中逐渐探索演进所形成的，经历过复杂业务的高并发挑战，比Spring Cloud的开源时间还要早。目前阿里、京东、当当、携程、去哪等一些企业都在使用Dubbo。

### 5.2.3 Dropwizard

Dropwizard将Java生态系统中各个问题域里最好的组建集成于一身，能够快速打造一个Rest风格的后台，还可以整合Dropwizard核心以外的项目。国内现在使用Dropwizard还很少，资源也不多，但是与Spring Boot相比，Dropwizard在轻量化上更有优势，同时如果用过Spring，那么基本也会使用Spring Boot。

### 5.2.4 Go-Kit

Go-Kit是分布式开发的工具合集，适合用于大型业务场景下构建微服务

## 5.3 TinyGO微服务代码实例

### 5.3.1 网关启动程序

/cmd/main.go

```go
package main

import (

    "github.com/iwordz/tinygo"
    "github.com/iwordz/tinygo/config"
    "github.com/iwordz/tinygo/router"

)

func init() {

    //初始化路由
    router.NewRouter().Get("/user/").SetServiceName("UserCenter").SetTokenFlag(false).RPCToJson()
    router.NewRouter().Get("/home/config").SetServiceName("UserCenter").SetTokenFlag(false).RPCToJson()

}

func main() {

    tinygo.SetupEnv(config.TinyGoRun{Env: "local", Config: "etc/conf/app.toml"}).RunGatewayService() 

}
```



### 5.3.2 使用TinyGO进行微服务模块开发



/cmd/main.go

```go
package main

import (
	"github.com/iwordz/tinygo"
	"github.com/iwordz/tinygo/examples/demo/services"
	"github.com/iwordz/tinygo/examples/demo/transports"
	"github.com/iwordz/tinygo/router"
)

func init() {
	//初始化路由
	router.NewRouter().Get("/user/").SetDecodeRequestFunc(transports.DecodeUserRequest).SetDecodeServiceFunc(services.User).SetTokenFlag(false).DisableEnc()
	router.NewRouter().Get("/home/config").SetDecodeRequestFunc(transports.DecodeGetHomeConfigRequest).SetDecodeServiceFunc(services.GetHomeConfig).SetTokenFlag(false).EnableEnc()
	router.NewRouter().Get("/custom/http/response").SetDecodeRequestFunc(transports.DecodeCustomHttpResponseRequest).SetDecodeServiceFunc(services.CustomHttpResponse).SetTokenFlag(false).SetCustomHttpResponse(true).EnableEnc()
}

func main() {
	//tinygo.Run()
	tinygo.SystemEnv().Run()
}
```



```
注解:详情请到源码examples目录demo和gateway目录查看源代码.
```



### 5.3.4 TinyGO微服务如何启动？

本地需要在本地安装consul服务并且启动,修改etc/conf/app.toml文件中新增如下配置：

```
[ServiceInfo]
IsMicroService = true
ServiceTimeout ="5s"    #服务健康超时时间
ServiceInterval = "3s"   #服务健康检查间隔时间
ServiceUnRegistryTimeout = "30s"  #服务不可用时从注册中心删除的时间
ServiceHeartbeatPort = 8012
ServerName       = "UserCenter"
ServerID         = "UserCenter_5"
ServerTag        = "UserCenter"
ServerPort       = 8008
ServerAddr = ":8008"
PprofAddr = ":60601"
FillInterval = 1
Capacity = 1000
```



## 5.4 TinyGo框架介绍

### 5.4.1 框架介绍

TbGo是一个完全由Golang开发的web框架，目前仅支持HTTP，支持RestfullAPI模式、底层无缝支持MySQL、Redis、支持Apollo配置中心。也是一款支持微服务的Golang框架，并且是一个快速开发 Go 应用的 HTTP 框架，他可以用来快速开发 API、Web 及后端服务等各种应用，是一个 RESTful 的框架。源码：https://github.com/iwordz/tinygo，TinyGo框架目录结构,下面详细介绍下这些包作用：

```go
//使用app初始化
//app包目录主要是初始化框架全局使用对象，比如:logger,serverConfig,application context,cache,redis,mysql等实力对象。
//tinygo/tinygo.go
///调用示例:
//初始化application context和数据库连接

	appCtx := app.Instance().SetLogger(logger).SetCache(newCache).SetServerConfig(sConfig).SetDbInstance(db.GetInstances()).SetRedisInstance(redis.GetInstances()).SetContext().GetContext()
	var g group.Group
	g.Add(func() (err error) {
		logger.Infow("start_server", "server_info", fmt.Sprintf("Http Server start at port %s", appCtx.ServerConfig.SConfig.ServerAddr))
		err = http.ListenAndServe(appCtx.ServerConfig.SConfig.ServerAddr, middleware.MakeHttpHandlers(appCtx))
		if err != nil {
			return
		}
		err = http.ListenAndServe(appCtx.ServerConfig.SConfig.PprofAddr, nil)
		if err != nil {
			return
		}
		return nil
	}, func(err error) {
		logger.Errorw("srv init failed", "err", err.Error())
	})
	err := g.Run()
	if err != nil {
		logger.Errorw("srv run failed", "err", err.Error())
		return
	}


```

```go
//balancer包主要是微服务负载均衡算法，主要实现:一次性Hash、随机、Round Robin、权重等负载均衡算法。
//balancer初始化代码

package middleware

//NewServer constructs a new server middleware handler
func newRPCServer(ctx *context.Context, svc string) *rpc.Server {
	ds := discovery.Discovery{Mu: sync.Mutex{}, SvcName: svc, LbType: config.Instance().ServiceInfo.LBType}
	err := ds.FirstInitService() //一次性初始化内容
	if err != nil {
		panic("newRPCServer init err " + err.Error())
	}
	go ds.AutoRefreshConsul() //自动获取LoadBalancer实例
	return &rpc.Server{Ctx: ctx, ServerName: svc, Ds: ds}
}


package discovery

import (
	"github.com/iwordz/tinygo/balancer"
	"github.com/iwordz/tinygo/consul"
	"github.com/iwordz/tinygo/consul/api"
	"net"
	"strconv"
	"sync"
	"time"
)

var (
	Lb      balancer.LoadBalance
	oldNods int
)

type Discovery struct {
	LbType    balancer.LbType
	SvcName   string
	DsAddress string
	Mu        sync.Mutex
}

//获取负载均衡对象
func (ds *Discovery) GetLb() balancer.LoadBalance {
	ds.Mu.Lock()
	ds.Mu.Unlock()
	return Lb
}

//首次初始化consul服务发现
func (ds *Discovery) FirstInitService() error {
	ds.fetch()
	return nil
}

//自动更新节点
func (ds *Discovery) AutoRefreshConsul() {
	//10s自动发现新注册的负载均衡节点
	tick := time.NewTicker(10 * time.Second)
	for {
		select {
		case <-tick.C:
			ds.fetch()
		}
	}
}

func (ds *Discovery) fetch() {
	ds.Mu.Lock()
	ds.Mu.Unlock()
	var lastIndex uint64
	services, metaInfo, err := consul.NewClientConsul().Health().Service(ds.SvcName, ds.SvcName, true, &api.QueryOptions{
		WaitIndex: lastIndex, // 同步点，这个调用将一直阻塞，直到有新的更新
	})
	if err != nil {
		panic("AutoRefreshConsul err " + err.Error())
	}
	if oldNods != len(services) {
		lastIndex = metaInfo.LastIndex
		Lb = balancer.LoadBalanceFactory(ds.LbType)
		for _, service := range services {
			err = Lb.Add(net.JoinHostPort(service.Service.Address, strconv.Itoa(service.Service.Port)))
			if err != nil {
				panic(err)
			}
		}
		oldNods = len(services)
	}
}
```

```go
//cache包是实现本地local cache。

```

```go
//cmd框架测试启动包。
package main

import (
	"github.com/iwordz/tinygo"
)

func init() {

//初始化路由router.NewRouter().Post("/user/").SetDecodeRequestFunc(transports.DecodeUserRequest).SetDecodeServiceFunc(services.User).SetTokenFlag(false).ToJson()

}

func main() {
  tinygo.SystemEnv().Run()
}
```

```go
//config是配置解析包，主要实现了local file模式和Apollo远程配置两种方式。
package config

```

```go
//consul是微服务服务发现客户端实现，主要使用consul实现。
package consul

import (
	conf "github.com/iwordz/tinygo/config"
	"github.com/hashicorp/consul/api"
	"sync"
)

var (
	client = &api.Client{}
	once   = sync.Once{}
	config = &api.Config{}
	err    error
)

func init() {
	once.Do(func() {
		config = api.DefaultConfig()
		if conf.Instance().ServiceInfo.ConsulService == "" {
			//默认值
			conf.Instance().ServiceInfo.ConsulService = "127.0.0.1:8500"
		}
		config.Address = conf.Instance().ServiceInfo.ConsulService // consul server
		client, err = api.NewClient(config)
		if err != nil {
			panic(err)
		}
	})

}

func NewClientConsul() *api.Client {
	return client
}
```

```go
//context是application上下文相关的包，主要用来承载数据库DB实例信息，logger实例信息等。传递HTTP Requst相关Data。结合cmd/server.go启动类初始化application context对象。
package context

import (
	"context"
	"github.com/iwordz/tinygo/config"
	"github.com/go-redis/redis"
	"go.uber.org/zap"
	"net/http"
	"sync"
	"xorm.io/xorm"
)

type Context struct {
	//Mu            sync.Mutex
	Ctx           context.Context
	IsVerifyToken bool
	//auth token func by verify token
	AuthTokenFunc func(*RequestContext) (bool, error)
	HttpToContext func(*RequestContext) *RequestContext
	Logger        *zap.SugaredLogger
	ServerConfig  *config.ServerConfig
	DBInstance    map[string]*xorm.Engine
	RedisInstance map[string]*redis.Client
}

type RequestContext struct {
	Authorization  string
	Request        interface{}
	Response       interface{}
	DecodeService  func(*RequestContext) (interface{}, error)
	DecodeRequest  func(*RequestContext) (interface{}, error)
	OriginReq      *http.Request
	Err            error
	Rw             http.ResponseWriter
	UserAgent      string
	RequestHeader  map[string][]string
	ResponseHeader map[string]string
	EnableEncrypt  bool
	AppCtx         *Context
}

var (
	once   sync.Once
	appCtx *Context
)

func init() {
	once.Do(func() {
		appCtx = new(Context)
	})
}
func (app *Context) SetContext(ctx *Context) {
	appCtx = ctx
}
func (app *Context) GetContext() *Context {
	return appCtx
}
```

```go
//db是MySQL相关操作包。
package db

import (
	"fmt"
	"sync"
	"time"

	appConfig "gitbub.com/iwordz/tinygo/config"
	_ "github.com/go-sql-driver/mysql"
	"xorm.io/xorm"
)

const (
	defaultDbNum    = 16 //默认是16个库,
	defaultTableNum = 32 //默认是64个表
)

var (
	_dbInstances      = map[string]_dbInstanceConfigInner{}
	_globalDbInstance = map[string]*xorm.Engine{}
	dbInitializeOnce  sync.Once
)

type (
	connConfig struct {
		Mu              *sync.Mutex
		InstanceName    string
		InstanceType    string
		Host            string
		User            string
		Pass            string
		Port            int
		MaxIdleCount    int //最小空闲连接数量
		MaxOpenCount    int //最大连接数
		Timeout         int //连接超时时间
		MaxConnLifetime int
		ShowSql         bool
		Dbname          string
		Charset         string
	}

	_dbInstanceConfigInner struct {
		DBInstance   *xorm.Engine
		ConnDBConfig connConfig
	}
)

func init() {
}

func _newDB(instanceName string) *xorm.Engine {

	if _, ok := _dbInstances[instanceName]; !ok {
		panic("instance name is not exists")
	}
	_config := _dbInstances[instanceName]
	_config.ConnDBConfig.Mu.Lock()
	defer _config.ConnDBConfig.Mu.Unlock()
	if _config.DBInstance != nil {
		//mysql数据库连接对象使用之前判断是否可用
		if err := _config.DBInstance.Ping(); err == nil {
			//连接conn可用，直接返回当前可用conn
			return _config.DBInstance
		}
	}
	if _config.DBInstance != nil {
		//将不可用的连接conn重置为nil
		_config.DBInstance = nil
	}
	engine, err := xorm.NewEngine(_config.ConnDBConfig.InstanceType, fmt.Sprintf("%s:%s@tcp(%s:%d)/%s?charset=utf8", _config.ConnDBConfig.User, _config.ConnDBConfig.Pass, _config.ConnDBConfig.Host, _config.ConnDBConfig.Port, _config.ConnDBConfig.Dbname))
	if err != nil {
		panic("new db " + err.Error())
	}
	if err = engine.Ping(); err != nil {
		panic("new db ping() " + err.Error())
	}
	if _config.ConnDBConfig.ShowSql {
		//engine.ShowExecTime(true)
		engine.ShowSQL(true)
	}
	if _config.ConnDBConfig.MaxOpenCount > 0 {
		engine.SetMaxOpenConns(_config.ConnDBConfig.MaxOpenCount)
	}
	if _config.ConnDBConfig.MaxIdleCount > 0 {
		engine.SetMaxIdleConns(_config.ConnDBConfig.MaxIdleCount)
	}
	if _config.ConnDBConfig.MaxConnLifetime > 0 {
		engine.SetConnMaxLifetime(time.Duration(_config.ConnDBConfig.MaxConnLifetime) * time.Second)
	}
	if _config.ConnDBConfig.ShowSql {
		engine.ShowSQL(true)
	}
	if _config.ConnDBConfig.Timeout > 0 {

	}
	_config.DBInstance = engine
	_dbInstances[instanceName] = _config
	return engine
}

func GetInstances() map[string]*xorm.Engine {
	dbInitializeOnce.Do(func() {
		dbInitialize()
	})
	return _globalDbInstance
}

func GetInstance(instanceName string) *xorm.Engine {
	return GetInstances()[instanceName]
}

func dbInitialize() {
	//初始化数据源map
	if len(appConfig.Instance().Mysql) == 0 {
		//panic("mysql config is empty")
		return
	}
	var lock = &sync.Mutex{}
	for _, _configMysql := range appConfig.Instance().Mysql {
		_tmp := _dbInstanceConfigInner{}
		_tmp.DBInstance = nil
		dbConn := connConfig{
			Mu:           lock,
			InstanceName: _configMysql.InstanceName,
			InstanceType: _configMysql.DbType,
			Host:         _configMysql.Host,
			User:         _configMysql.User,
			Pass:         _configMysql.Pass,
			Port:         _configMysql.Port,
			MaxIdleCount: 1000,
			MaxOpenCount: 1000,
			Timeout:      5,
			Dbname:       _configMysql.Dbname,
			Charset:      _configMysql.Charset,
		}
		_tmp.ConnDBConfig = dbConn
		_dbInstances[dbConn.InstanceName] = _tmp
		_globalDbInstance[_configMysql.InstanceName] = _newDB(_configMysql.InstanceName)
	}
}

func ShardingKey() int {
	return 1
}

```

```go
//discovery是微服务服务发现相关实现。
package discovery

import (
	"github.com/iwordz/tinygo/balancer"
	"github.com/iwordz/tinygo/consul"
	"github.com/hashicorp/consul/api"
	"net"
	"strconv"
	"sync"
	"time"
)

var (
	Lb      balancer.LoadBalance
	oldNods int
)

type Discovery struct {
	LbType    balancer.LbType
	SvcName   string
	DsAddress string
	Mu        sync.Mutex
}

//获取负载均衡对象
func (ds *Discovery) GetLb() balancer.LoadBalance {
	ds.Mu.Lock()
	ds.Mu.Unlock()
	return Lb
}

//首次初始化consul服务发现
func (ds *Discovery) FirstInitService() error {
	ds.fetch()
	return nil
}

//自动更新节点
func (ds *Discovery) AutoRefreshConsul() {
	//10s自动发现新注册的负载均衡节点
	tick := time.NewTicker(10 * time.Second)
	for {
		select {
		case <-tick.C:
			ds.fetch()
		}
	}
}

func (ds *Discovery) fetch() {
	ds.Mu.Lock()
	ds.Mu.Unlock()
	var lastIndex uint64
	services, metaInfo, err := consul.NewClientConsul().Health().Service(ds.SvcName, ds.SvcName, true, &api.QueryOptions{
		WaitIndex: lastIndex, // 同步点，这个调用将一直阻塞，直到有新的更新
	})
	if err != nil {
		panic("AutoRefreshConsul err " + err.Error())
	}
	if oldNods != len(services) {
		lastIndex = metaInfo.LastIndex
		Lb = balancer.LoadBalanceFactory(ds.LbType)
		for _, service := range services {
			err = Lb.Add(net.JoinHostPort(service.Service.Address, strconv.Itoa(service.Service.Port)))
			if err != nil {
				panic(err)
			}
		}
		oldNods = len(services)
	}
}

```

```go
//endpoints是TinyGo框架service、requset、token等执行层。
package endpoints

import (
	"github.com/iwordz/tinygo/context"
)

//decode request func is call by deal http request
type (
	DecodeRequestFunc func(*context.RequestContext) (interface{}, error)
	//decode service func is call by  deal service logic
	DecodeServicesFunc func(*context.RequestContext) (interface{}, error)

	//error service func is call by  deal service logic error
	ErrorServicesFunc func(*context.RequestContext)

	//encode response func is call by return client data
	EncodeResponseFunc func(*context.RequestContext) error

	//auth token func by verify token
	AuthTokenFunc func(*context.RequestContext) (bool, error)

	//decode http to context
	DeCodeHttpToContextFunc func(*context.RequestContext) *context.RequestContext

	//request func
	RequestFunc func(*context.RequestContext) *context.RequestContext

	//middleware func
	Middleware func(Endpoint) Endpoint

	//endpoint type
	//Endpoint func(ctx *context.Context, req DecodeRequestFunc, service DecodeServicesFunc) (response interface{}, err error)
	Endpoint func(*context.RequestContext) (response interface{}, err error)
)

// MakeEndpoint make endpoint
//call service
func MakeEndpoint() Endpoint {
	return func(reqCtx *context.RequestContext) (response interface{}, err error) {
		if reqCtx == nil {
			panic("init ctx error")
		}
		if reqCtx.AppCtx.HttpToContext == nil {
			panic("init ctx error")
		}
		//http request transfer context
		reqCtx.AppCtx.HttpToContext(reqCtx)
		if reqCtx.AppCtx.IsVerifyToken {
			//token验证
			_, err := reqCtx.AppCtx.AuthTokenFunc(reqCtx)
			if err != nil {
				return nil, err
			}
		}
		reqCtx.Request, err = reqCtx.DecodeRequest(reqCtx)
		if err != nil {
			return nil, err
		}
		response, err = reqCtx.DecodeService(reqCtx)
		if err != nil {
			return nil, err
		}
		return response, err
	}
}
```

```go
//err是错误处理包。
package basicError

type Failure interface {
	Failed() error
}

type (
	ErrType struct {
		Code int
		Err  error
	}

	BusinessErrorWrapper struct {
		Code  int    `json:"code"`
		Error string `json:"error"`
	}
)

func (e ErrType) Error() string {
	return e.Err.Error()
}

func (e ErrType) GetCode() int {
	return e.Code
}

//使用示例
package err

import (
	"errors"

	basicError "github.com/iwordz/tinygo/err"
)

var (
	//DB err
	DBErr = basicError.ErrType{Code: 10000, Err: errors.New("DB error")}
)
```

```go
//etc是配置文件目录。


```

```go
//examples存放TinyGo代码示例目录。demo是普通的HTTP接口代码，gateway是网关类型实现代码。
```

```go
//instrument是TinyGo框架限流的具体实现包。
package instrument

import (
	"errors"
	"github.com/iwordz/tinygo/context"
	"github.com/iwordz/tinygo/endpoints"
	basicError "github.com/iwordz/tinygo/err"
	"github.com/gorilla/mux"
	"github.com/juju/ratelimit"
	stdHTTP "net/http"
)

var (
	ErrLimitExceed = basicError.ErrType{Code: 1, Err: errors.New("rate limit exceed!")}
)

//NewTokenBucketLimitWithJuju 使用juju rate limit 创建限流中间件
func NewTokenBucketLimitWithJuju(bkt *ratelimit.Bucket) endpoints.Middleware {
	return func(next endpoints.Endpoint) endpoints.Endpoint {
		return func(reqCtx *context.RequestContext) (response interface{}, err error) {
			if bkt.TakeAvailable(1) == 0 {
				return nil, ErrLimitExceed
			}
			return next(reqCtx)
		}
	}
}

func NewCORSMethodMiddleware(ctx *context.Context) mux.MiddlewareFunc {
	return func(next stdHTTP.Handler) stdHTTP.Handler {
		return stdHTTP.HandlerFunc(func(rw stdHTTP.ResponseWriter, req *stdHTTP.Request) {
			if req.Method == stdHTTP.MethodOptions {
				rw.Header().Set("Access-Control-Allow-Origin", ctx.ServerConfig.SConfig.AllowOrigin) //允许访问所有域
				rw.Header().Set("Access-Control-Allow-Headers", ctx.ServerConfig.SConfig.AllowHeaders)
				rw.Header().Set("Access-Control-Allow-Credentials", ctx.ServerConfig.SConfig.AllowCredentials) //允许
				rw.Header().Set("Access-Control-Allow-Methods", ctx.ServerConfig.SConfig.AllowMethods)         //允许接受
				rw.WriteHeader(stdHTTP.StatusOK)
				return
			}
			next.ServeHTTP(rw, req)
		})
	}
}

```

```go
//log是logger具体实现。logger对象在框架初始化时在application context对象中已经存在，可直接使用，例如：
ctx.AppCtx.Logger.Infow("xxxxx", "xxxx", "xxxxxx")

```

```go
//middleware是TinyGo框架中间件层，主要处理框架标准Response、Err等事务。
//MakeHttpHandlers被cmd/server.go调用，用来初始化http handler
// MakeHttpHandler make server handler use mux
func MakeHttpHandlers(ctx *context.Context) stdHTTP.Handler {
	r := mux.NewRouter()
	initEndpoints := endpoints.MakeEndpoint()
	rateBucket := ratelimit.NewBucketWithQuantum(time.Second*time.Duration(ctx.ServerConfig.SConfig.FillInterval), ctx.ServerConfig.SConfig.Capacity, ctx.ServerConfig.SConfig.Capacity)
	endpoint := instrument.NewTokenBucketLimitWithJuju(rateBucket)(initEndpoints)
	for pattern, rr := range router.RouterMap {
		var ns = &server.Server{}
		if rr.UseCustomHttpResponse {
			//使用自定义response func return
			ns = newServer(endpoint, rr.DecodeRequestFunc, nil, rr.DecodeServiceFunc, rr.VerifyToken, rr.AuthTokenFunc, nil, false, ctx)
		} else {
			//使用框架定义response func return
			ns = newServer(endpoint, rr.DecodeRequestFunc, EncodeBasicResponse, rr.DecodeServiceFunc, rr.VerifyToken, rr.AuthTokenFunc, EncodeError, rr.EnableEncrypt, ctx)
		}
		if rr.EnableCORS {
			r.Methods(rr.HttpMethod, stdHTTP.MethodOptions).Path(pattern).Handler(ns)
		} else {
			r.Methods(rr.HttpMethod).Path(pattern).Handler(ns)
		}
	}
	return r
}

////MakeHttpHandler/server.go调用，用来初始化http handler
// MakeHttpHandler make server handler use mux
func MakeRPCHandlers(ctx *context.Context) stdHTTP.Handler {
	r := mux.NewRouter()
	for pattern, rr := range router.RouterMap {
		newServer := newRPCServer(ctx, rr.ServiceName)
		r.Methods(rr.HttpMethod).Path(pattern).Handler(newServer)
	}
	return r
}

//NewServer constructs a new server middleware handler
func newServer(endpoint endpoints.Endpoint, dec endpoints.DecodeRequestFunc, enc endpoints.EncodeResponseFunc, svc endpoints.DecodeServicesFunc, isVerifyToken bool, authToken endpoints.AuthTokenFunc, errFunc endpoints.ErrorServicesFunc, enableEncrypt bool, ctx *context.Context) *server.Server {
	return &server.Server{Ctx: ctx, Endpoint: endpoint, DecodeServices: svc, DecodeRequest: dec, EncodeResponse: enc, IsVerifyToken: isVerifyToken, AuthToken: authToken, ErrorServices: errFunc, HttpToContext: HTTPToContext(), EnableEncrypt: enableEncrypt}
}

//NewServer constructs a new server middleware handler
func newRPCServer(ctx *context.Context, svc string) *rpc.Server {
	ds := discovery.Discovery{Mu: sync.Mutex{}, SvcName: svc, LbType: config.Instance().ServiceInfo.LBType}
	err := ds.FirstInitService() //一次性初始化内容
	if err != nil {
		panic("newRPCServer init err " + err.Error())
	}
	go ds.AutoRefreshConsul() //自动获取LoadBalancer实例
	return &rpc.Server{Ctx: ctx, ServerName: svc, Ds: ds}
}
```

```go
//pool是对象池包，主要实现了Http Request buffer、Byte buffer等功能。

package pool

import (
	"bytes"
	"github.com/iwordz/tinygo/config"
	"github.com/iwordz/tinygo/context"
	"github.com/iwordz/tinygo/tool/decrypt"
	"io"
	"sync"
)

var (
	RequestApi = &adapter{}
)

func init() {
	RequestApi = NewPoolApi()
}

type adapter struct {
	pool sync.Pool
}

func NewPoolApi() *adapter {
	return &adapter{
		pool: sync.Pool{
			New: func() interface{} {
				return bytes.NewBuffer(make([]byte, 4096))
			},
		},
	}
}

func (api *adapter) ReadAll(reqCtx *context.RequestContext) (b []byte, err error) {
	buffer := api.pool.Get().(*bytes.Buffer)
	buffer.Reset()
	defer func() {
		if buffer != nil {
			api.pool.Put(buffer)
			buffer = nil
		}
	}()
	_, err = io.Copy(buffer, reqCtx.OriginReq.Body)
	if reqCtx.EnableEncrypt {
		//解密
		return decrypt.Dec(config.Instance().ServiceInfo.AesMethod, buffer.Bytes(), []byte(config.Instance().ServiceInfo.AesKey)), nil
	}
	return buffer.Bytes(), err
}

func (api *adapter) NewBytesBuffer() bytes.Buffer {
	buffer := api.pool.Get().(*bytes.Buffer)
	buffer.Reset()
	defer func() {
		if buffer != nil {
			api.pool.Put(buffer)
			buffer = nil
		}
	}()
	return *buffer
}

//调用示例
func DecodeXxxxxRequest(ctx *context.RequestContext) (interface{}, error) {
	data, err := pool.RequestApi.ReadAll(ctx) //初始化对象池子
	request := entity.HomeConfigRequest{}
	if err != nil {
		return request, err
	}
	err = jsoniter.Unmarshal(data, &request)
	if err != nil {
		return request, err
	}
	return request, nil
}

//对象输出字符串
func (log LoggingOut) Formation() string {
	b, err := jsoniter.Marshal(log.Out)
	if err != nil {
		return fmt.Sprintf("%+v", err.Error())
	}
	out := pool.RequestApi.NewBytesBuffer() //初始化对象池子
	err = json.Indent(&out, b, "", "    ")
	if err != nil {
		return fmt.Sprintf("%+v", err.Error())
	}
	app.Instance().Logger().Info(out.String())
	return out.String()
}
```

```go
//proxy是路由代理层包，主要处理router相关信息。
package proxy
//此处省略一万行代码
func init() {
	//全局初始化工厂和代理方法
	router.NewRouter = func() router.Router {
		r := &router.RouterImpl{}
		p := &Proxy{r, nil, nil, nil, nil}
		return p
	}

	log.New = func(isDev bool) log.Log {
		r := &log.Impl{}
		p := &Proxy{nil, r, nil, nil, nil}
		return p
	}
	request.New = func() request.ValidatorRequest {
		r := &request.ValidatorRequestImpl{}
		p := &Proxy{nil, nil, r, nil, nil}
		return p
	}

	encode.New = func(out interface{}) encode.Encode {
		r := &encode.Impl{Out: out}
		p := &Proxy{nil, nil, nil, r, nil}
		return p
	}

	decode.New = func(in []byte, out interface{}) decode.Decode {
		r := &decode.Impl{Out: out, In: in}
		p := &Proxy{nil, nil, nil, nil, r}
		return p
	}

}
```

```go
//redis是Redis具体实现包。
package redis

import (
	"fmt"
	"github.com/iwordz/tinygo/config"
	"github.com/go-redis/redis"
	"sync"
)

var (
	_redisInstances     = map[string]*redis.Client{}
	redisInitializeOnce sync.Once
)

type (
	opt struct {
		Host     string
		Port     int
		Password string
		DB       int
		Mu       sync.Mutex
	}
)

func init() {
}

func (o *opt) newClient() *redis.Client {
	redisClient := redis.NewClient(&redis.Options{
		Addr:     fmt.Sprintf("%s:%d", o.Host, o.Port),
		Password: o.Password, // no password set
		DB:       o.DB,       // use default DB
	})
	if err := redisClient.Ping().Err(); err != nil {
		panic("redis connect error " + err.Error())
	}
	return redisClient
}

func GetInstances() map[string]*redis.Client {
	redisInitializeOnce.Do(func() {
		redisInitialize()
	})
	return _redisInstances
}

func GetInstance(instanceName string) *redis.Client {
	return GetInstances()[instanceName]
}

func redisInitialize() {
	if len(config.Instance().Redis) > 0 {
		for _, redisConfig := range config.Instance().Redis {
			opt := opt{Host: redisConfig.Host,
				Password: redisConfig.Password,
				Port:     redisConfig.Port,
				DB:       redisConfig.Db,
				Mu:       sync.Mutex{},
			}
			_redisInstances[redisConfig.InstanceName] = opt.newClient()
		}
	}
}

//调用redis示例
redisClient := ctx.AppCtx.RedisInstance["testInstanceName"]
redisClient.Set("key", 1, 0)
```

```go
//register是微服务注册中心包。
package main

import (
	"github.com/iwordz/tinygo"
	"github.com/iwordz/tinygo/examples/demo/services"
	"github.com/iwordz/tinygo/examples/demo/transports"
	"github.com/iwordz/tinygo/router"
)

func init() {
	//初始化路由	router.NewRouter().Get("/xxxx/xxx/xxxx").SetDecodeRequestFunc(transports.DecodeCustomHttpResponseRequest).SetDecodeServiceFunc(services.CustomHttpResponse).SetTokenFlag(false).SetCustomHttpResponse(true).EnableEnc()
}

func main() {
	//tinygo.Run()
	tinygo.SystemEnv().RunMicroService() //启用微服务注册模式
}
```

```go
//request是Http Requset校验包。
package request

import (
	"github.com/go-playground/validator/v10"
)

var (
	New = func() ValidatorRequest {
		return &ValidatorRequestImpl{validator.New()}
	}
)

type ValidatorRequest interface {
	ReqValidator(request interface{}) error
}

type ValidatorRequestImpl struct {
	Stu *validator.Validate
}

func (valImpl *ValidatorRequestImpl) ReqValidator(body interface{}) error {
	return valImpl.Stu.Struct(body)
}

//调用示例
func DecodeXxxxxRequest(ctx *context.Context) (interface{}, error) {
	data ,err := pool.RequestApi.ReadAll(ctx.OriginReq)
	request := entity.XxxxxRequest{}
	if err != nil {
		return request , err
	}
	err = jsoniter.Unmarshal(data, &request)
	if err != nil {
		return request, err
	}
	if err = req.New().ReqValidator(request);err != nil {
    		return nil,errors.New("参数错误") //校验参数
    }
	return request,nil
}
```

```go
//router是路由具体实现和proxy包相互依赖。
package router

import (
	"github.com/iwordz/tinygo/auth"
	"github.com/iwordz/tinygo/endpoints"
	"reflect"
	"runtime"
	"strings"
	"sync"
)

type Router interface {
  //service是否返回
	SetCustomHttpResponse(res bool) *RouterImpl 
  //rpc调用
	RPCToJson()   
  //http服务
	ToJson()           
  //绑定http方法
	SetServiceName(svcName string) *RouterImpl 
	//GET方法请求一个指定资源的表示形式. 使用GET的请求应该只被用于获取数据.
	Get(pattern string) *RouterImpl
	//HEAD方法请求一个与GET请求的响应相同的响应，但没有响应体.
	Head(pattern string) *RouterImpl
	//POST方法用于将实体提交到指定的资源，通常导致在服务器上的状态变化或副作用.
	Post(pattern string) *RouterImpl
	//PUT方法用请求有效载荷替换目标资源的所有当前表示。
	Put(pattern string) *RouterImpl
	//DELETE方法删除指定的资源。
	Delete(pattern string) *RouterImpl
	//CONNECT方法建立一个到由目标资源标识的服务器的隧道。
	Connect(pattern string) *RouterImpl
	//OPTIONS方法用于描述目标资源的通信选项。
	Options(pattern string) *RouterImpl
	//TRACE方法沿着到目标资源的路径执行一个消息环回测试。
	Trace(pattern string) *RouterImpl
	//PATCH方法用于对资源应用部分修改。
	Patch(pattern string) *RouterImpl
	//path string
	Pattern(pattern string) *RouterImpl
	//绑定参数解析函数
	SetDecodeRequestFunc(decodeRequestFunc endpoints.DecodeRequestFunc) *RouterImpl
	//绑定业务逻辑函数
	SetDecodeServiceFunc(decodeServiceFunc endpoints.DecodeServicesFunc) *RouterImpl
	//绑定http上下文转换
	SetHttpToContextFunc(decodeHttpToContextFunc endpoints.DeCodeHttpToContextFunc) *RouterImpl
	//绑定token解析函数
	SetAuthTokenFunc(decodeAuthTokenFunc endpoints.AuthTokenFunc) *RouterImpl
	//绑定设定是否需要token函数
	SetTokenFlag(verifyToken bool) *RouterImpl
	//cors preflight
	SetCORSFlag(cors bool) *RouterImpl
}

type RouterType map[string]RouterImpl
type RouterImpl struct {
	HttpMethod              string                            //路由请求方法
	VerifyToken             bool                              //是否需要验证token
	DecodeRequestFunc       endpoints.DecodeRequestFunc       //绑定解析Request函数
	DecodeServiceFunc       endpoints.DecodeServicesFunc      //绑定Service逻辑处理函数
	AuthTokenFunc           endpoints.AuthTokenFunc           //绑定判定token函数
	DeCodeHttpToContextFunc endpoints.DeCodeHttpToContextFunc //绑定http请求转为context函数
	PatternString           string                            //pattern path
	ServiceName             string                            //service name
	UseCustomHttpResponse   bool                              //使用自定义函数response
	EnableEncrypt           bool                              //是否开启加解密
	EnableCORS              bool                              //是否启用cors
}

var (
	RouterMap  = make(map[string]RouterImpl)
	routerImpl *RouterImpl
	once       = sync.Once{}
	NewRouter  = func() Router {
		once.Do(func() {
			routerImpl = new(RouterImpl)
		})
		return routerImpl
	}
)

func (r *RouterImpl) ToJson() {
	serviceName := runtime.FuncForPC(reflect.ValueOf(r.DecodeServiceFunc).Pointer()).Name()
	servicesName := strings.Split(serviceName, ".")
	RouterMap[r.PatternString] = RouterImpl{
		AuthTokenFunc:           r.AuthTokenFunc,
		ServiceName:             servicesName[1],
		VerifyToken:             r.VerifyToken,
		HttpMethod:              r.HttpMethod,
		DecodeRequestFunc:       r.DecodeRequestFunc,
		DecodeServiceFunc:       r.DecodeServiceFunc,
		DeCodeHttpToContextFunc: r.DeCodeHttpToContextFunc,
		UseCustomHttpResponse:   r.UseCustomHttpResponse,
		EnableCORS:              r.EnableCORS,
	}
	return
}

func (r *RouterImpl) RPCToJson() {
	RouterMap[r.PatternString] = RouterImpl{
		PatternString:           r.PatternString,
		AuthTokenFunc:           r.AuthTokenFunc,
		ServiceName:             r.ServiceName,
		VerifyToken:             r.VerifyToken,
		HttpMethod:              r.HttpMethod,
		DecodeRequestFunc:       r.DecodeRequestFunc,
		DecodeServiceFunc:       r.DecodeServiceFunc,
		DeCodeHttpToContextFunc: r.DeCodeHttpToContextFunc,
		EnableCORS:              r.EnableCORS,
	}
	return
}

//禁用加解密
func (r *RouterImpl) DisableEnc() {
	RouterMap[r.PatternString] = RouterImpl{
		PatternString:           r.PatternString,
		AuthTokenFunc:           r.AuthTokenFunc,
		ServiceName:             r.ServiceName,
		VerifyToken:             r.VerifyToken,
		HttpMethod:              r.HttpMethod,
		DecodeRequestFunc:       r.DecodeRequestFunc,
		DecodeServiceFunc:       r.DecodeServiceFunc,
		DeCodeHttpToContextFunc: r.DeCodeHttpToContextFunc,
		EnableCORS:              r.EnableCORS,
	}
	return
}

//开启加解密
func (r *RouterImpl) EnableEnc() {
	serviceName := runtime.FuncForPC(reflect.ValueOf(r.DecodeServiceFunc).Pointer()).Name()
	servicesName := strings.Split(serviceName, ".")
	RouterMap[r.PatternString] = RouterImpl{
		AuthTokenFunc:           r.AuthTokenFunc,
		ServiceName:             servicesName[1],
		VerifyToken:             r.VerifyToken,
		HttpMethod:              r.HttpMethod,
		DecodeRequestFunc:       r.DecodeRequestFunc,
		DecodeServiceFunc:       r.DecodeServiceFunc,
		DeCodeHttpToContextFunc: r.DeCodeHttpToContextFunc,
		UseCustomHttpResponse:   r.UseCustomHttpResponse,
		EnableEncrypt:           true,
		EnableCORS:              r.EnableCORS,
	}
	return
}

func (r *RouterImpl) Get(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "GET"
	return routerImpl
}
func (r *RouterImpl) Head(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "HEAD"
	return routerImpl
}
func (r *RouterImpl) Post(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "POST"
	return routerImpl
}
func (r *RouterImpl) Put(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "PUT"
	return routerImpl
}
func (r *RouterImpl) Delete(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "DELETE"
	return routerImpl
}
func (r *RouterImpl) Connect(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "CONNECT"
	return routerImpl
}
func (r *RouterImpl) Options(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "OPTIONS"
	return routerImpl
}

func (r *RouterImpl) Trace(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.HttpMethod = "TRACE"
	return routerImpl
}

func (r *RouterImpl) Patch(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	r.HttpMethod = "PATCH"
	return routerImpl
}

func (r *RouterImpl) Pattern(pattern string) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.PatternString = pattern
	return routerImpl
}

func (r *RouterImpl) SetDecodeRequestFunc(decodeRequestFunc endpoints.DecodeRequestFunc) *RouterImpl {
	if r == nil {
		panic("r is nil")
	}
	r.DecodeRequestFunc = decodeRequestFunc
	return routerImpl
}
func (r *RouterImpl) SetDecodeServiceFunc(decodeServiceFunc endpoints.DecodeServicesFunc) *RouterImpl {
	r.DecodeServiceFunc = decodeServiceFunc
	return routerImpl
}

func (r *RouterImpl) SetAuthTokenFunc(authTokenFunc endpoints.AuthTokenFunc) *RouterImpl {
	r.AuthTokenFunc = authTokenFunc
	return routerImpl
}

func (r *RouterImpl) SetHttpToContextFunc(httpToContextFunc endpoints.DeCodeHttpToContextFunc) *RouterImpl {
	r.DeCodeHttpToContextFunc = httpToContextFunc
	return routerImpl
}

func (r *RouterImpl) SetTokenFlag(verifyToken bool) *RouterImpl {
	if verifyToken {
		r.DeCodeHttpToContextFunc = auth.AuthorizationHTTPToContext
		r.AuthTokenFunc = auth.VerifyToken
	}
	r.VerifyToken = verifyToken
	return routerImpl
}

func (r *RouterImpl) SetCORSFlag(cors bool) *RouterImpl {
	r.EnableCORS = cors
	return routerImpl
}

func (r *RouterImpl) SetServiceName(svcName string) *RouterImpl {
	r.ServiceName = svcName
	return routerImpl
}

func (r *RouterImpl) SetCustomHttpResponse(res bool) *RouterImpl {
	r.UseCustomHttpResponse = res
	return routerImpl
}
```

```go
//rpc是微服务调用包，主要实现了server
package rpc

import (
	"fmt"
	stdHTTP "net/http"
	"net/http/httputil"
	"net/url"

	"github.com/iwordz/tinygo/config"
	"github.com/iwordz/tinygo/context"
	"github.com/iwordz/tinygo/discovery"
)

type Server struct {
	Ctx        *context.Context    //服务上下文对象
	ServerName string              //名字服务，用来识别服务发现的
	Endpoints  string              //格式为:http://ip:port,此字段使用ServerName发现ip+port拼接起来
	Ds         discovery.Discovery //服务发现实例对象
}

func (rs *Server) ServeHTTP(w stdHTTP.ResponseWriter, req *stdHTTP.Request) {
	hosts, err := rs.Ds.GetLb().Get("")
	if err != nil {
		rs.Ctx.Logger.Error("ServeHTTP", "err", err.Error())
		return
	}
	rs.Endpoints = fmt.Sprintf("http://%s", hosts)
	targetHost, _ := url.Parse(rs.Endpoints)
	// create the reverse proxy
	proxy := httputil.NewSingleHostReverseProxy(targetHost)
	// Update the headers to allow for SSL redirection
	req.URL.Host = targetHost.Host
	req.URL.Scheme = targetHost.Scheme
	req.Header.Set("X-Forwarded-Host", req.Header.Get("Host"))
	req.Host = targetHost.Host
	w.Header().Set("Access-Control-Allow-Origin", config.Instance().ServiceInfo.AllowOrigin) //允许访问所有域
	w.Header().Add("Access-Control-Allow-Headers", config.Instance().ServiceInfo.AllowHeaders)
	w.Header().Set("Access-Control-Allow-Credentials", config.Instance().ServiceInfo.AllowCredentials) //允许
	w.Header().Add("Access-Control-Allow-Methods", config.Instance().ServiceInfo.AllowMethods)         //允许接受
	w.Header().Set("Content-Type", config.Instance().ServiceInfo.ContentType)
	rs.Ctx.Logger.Infow("ServeHTTP", "rs.Endpoints", rs.Endpoints, "req.URL.Host", req.URL.Host, "req.URL.Scheme", req.URL.Scheme, "req.URL.Path", req.URL.Path, "req.URL.Query", req.URL.Query(), "req.Method", req.Method)
	proxy.ServeHTTP(w, req)
}
```

```go
//server是普通http server具体实现。
package server

import (
	stdHTTP "net/http"
	"time"

	"github.com/iwordz/tinygo/context"
	"github.com/iwordz/tinygo/endpoints"
	"github.com/iwordz/tinygo/tool/util"
)

type Server struct {
	Ctx            *context.Context
	Endpoint       endpoints.Endpoint
	DecodeServices endpoints.DecodeServicesFunc
	DecodeRequest  endpoints.DecodeRequestFunc
	EncodeResponse endpoints.EncodeResponseFunc
	IsVerifyToken  bool
	AuthToken      endpoints.AuthTokenFunc
	ErrorServices  endpoints.ErrorServicesFunc
	HttpToContext  endpoints.RequestFunc
	EnableEncrypt  bool
}

func (server *Server) newServerRequestContext(srv *Server, w stdHTTP.ResponseWriter, req *stdHTTP.Request) *context.RequestContext {
	reqCtx := &context.RequestContext{
		Request:       req,
		OriginReq:     req,
		Rw:            w,
		AppCtx:        srv.Ctx,
		DecodeService: srv.DecodeServices,
		DecodeRequest: srv.DecodeRequest,
		EnableEncrypt: srv.EnableEncrypt,
	}
	return reqCtx
}

func (server *Server) EnableCORS(reqCtx *context.RequestContext) bool {
	if reqCtx.OriginReq.Method == stdHTTP.MethodOptions {
		reqCtx.Rw.Header().Set("Access-Control-Allow-Origin", reqCtx.AppCtx.ServerConfig.SConfig.AllowOrigin)           //允许访问所有域
		reqCtx.Rw.Header().Set("Access-Control-Allow-Headers", reqCtx.AppCtx.ServerConfig.SConfig.AllowHeaders)         //允许header
		reqCtx.Rw.Header().Set("Access-Control-Allow-Credentials", reqCtx.AppCtx.ServerConfig.SConfig.AllowCredentials) //允许
		reqCtx.Rw.Header().Set("Access-Control-Allow-Methods", reqCtx.AppCtx.ServerConfig.SConfig.AllowMethods)         //允许接受
		reqCtx.Rw.WriteHeader(stdHTTP.StatusOK)
		return true
	}
	return false
}

//ServeHTTP handles the request by passing it to the real
//handler and logging the request details
func (server *Server) ServeHTTP(w stdHTTP.ResponseWriter, req *stdHTTP.Request) {

	startTime := time.Now()
	reqCtx := server.newServerRequestContext(server, w, req)
	if server.Ctx == nil {
		panic("fuck you need init application context")
	}
	reqCtx.Rw.Header().Set("Content-Type", reqCtx.AppCtx.ServerConfig.SConfig.ContentType)
	//判断是否需要跨域
	if server.EnableCORS(reqCtx) {
		return
	}

	//通过中间件将http request 转为context
	server.Ctx.HttpToContext = server.HttpToContext
	server.Ctx.IsVerifyToken = server.IsVerifyToken
	if server.Ctx.IsVerifyToken {
		if server.AuthToken == nil {
			panic("fuck you need setting auth token func")
		}
		server.Ctx.AuthTokenFunc = server.AuthToken
	}
	response, err := server.Endpoint(reqCtx)
	if err != nil {
		reqCtx.Err = err
		if server.ErrorServices != nil {
			server.ErrorServices(reqCtx)
		}
		return
	}
	reqCtx.Response = response
	if server.EncodeResponse != nil {
		err = server.EncodeResponse(reqCtx)
		if err != nil {
			server.ErrorServices(reqCtx)
			return
		}
	}

	defer server.Ctx.Logger.Infow("access_log",
		"user-agent", reqCtx.UserAgent,
		"user-header", reqCtx.RequestHeader,
		"remote_ip", util.RemoteIp(req),
		"request", reqCtx.Request,
		"response", reqCtx.Response,
		"took", time.Since(startTime).Seconds(),
		"err", reqCtx.Err,
	)
}

```

```go
//tool是公共工具类包。 此处代码省略。
```





### 5.4.2 框架基本使用

#### 5.4.2.1 初始化项目 

```
执行go run cmd/code/main.go --s=服务名称 --p=项目名称 --f=true

如出现：“启动生成框架代码” 说明代码生成成功
```



### 5.4.2.2 代码生成

```
### 生成逻辑代码 go run cmd/code/main.go --s=服务名称 --p=项目名称 --f=false

#### 如出现：“启动生成逻辑代码” 说明代码生成成功
```



### 5.4.2.3 限流配置

```
### 支持简单的限流功能，具体需要在etc/conf/app.toml配置文件中配置：

#### FillInterval = 1 单位为秒

#### Capacity = 1000 多个少FillInterval单位，允许的请求
```



### 5.4.2.4 初始化路由方法

在框架目录查看cmd/main.go文件中，查看路由初始化方法

```go
func init() {
    //初始化路由
    //接口不带token验证
    router.NewRouter().Get("/user/").SetDecodeRequestFunc(transports.DecodeUserRequest).SetDecodeServiceFunc(services.User).ToJson()
    //接口带token验证
    router.NewRouter().Get("/user/").SetDecodeRequestFunc(transports.DecodeUserRequest).SetDecodeServiceFunc(services.User).SetTokenFlag(true).ToJson()
    
    //Context刷新事件
    event.Events().AddListener(event.ContextRefreshed, func(e event.Event) {
        appCtx := e.(*event.ContextEvent).Context() // or: e.Source().(*context.Context)
        appCtx.Logger.Infow("init", "ContextRefreshed", "success")
    })
    //应用启动事件
    event.Events().AddListener(event.Start, func(e event.Event) {
        appCtx := e.(*event.ContextEvent).Context() // or: e.Source().(*context.Context)
        appCtx.Logger.Infow("init", "Start", "success")
    })
}
```

### 5.4.2.5 Golang对象池使用

使用方法如下

```go
 import (
 "github.com/iwordz/tinygo/pool"
 )

func init () {
   //初始化普通对象池对象
   obj1 := pool.RequestApi.NewBytesBuffer()

     //初始化http请求对象池对象
   obj2 := pool.RequestApi.ReadAll()
}
```

#### 5.4.2.6 Redis使用方法

```go
redisClient := appCtx.RedisInstance[constant.RedisInstance]
status := redisClient.MGet(redisKeys...).Val()
```

#### 5.4.2.7 MySQL使用方法

```go
dbClient := reqCtx.DBInstance[constant.MySQLConfigInstance]
dbClient.Where(model.Enable).Get(&config)
```

#### 5.4.2.8 logger使用方法

logger包含在在context对象中

```go
reqCtx.Logger.Infow("access_log",
		"user-agent", reqCtx.UserAgent,
		"user-header", reqCtx.RequestHeader,
		"remote_ip", util.RemoteIp(req),
		"request", reqCtx.Request,
		"response", reqCtx.Response,
		"took", time.Since(server.StartTime).Seconds(),
		"err", reqCtx.Err,
	)
```

使用app.Instance().GetLogger()获取logger对象

```go
 app.Instance().GetLogger().InfoW("start_server","port",30)
```

### 5.5 框架基础结构介绍

```
#### 2.5.1 transports 接收和解析客户端发送请求，将其转换为框架层request

#### 2.5.2 services 业务逻辑处理层

#### 2.5.3 entity dto层用来定义，每个service层request和response实体结构体

#### 2.5.4 model 数据库表对象层,目前tinygo框架使用的是Xorm,关于如何使用xorm请移步https://xorm.io/官方网站.

#### 2.5.6 cmd 应用启动入口,例如:server.go或者main.go

#### 2.5.7 etc 默认配置文件
```



### 5.4.3 运行程序

#### 5.4.3.1 运行

```go
执行 go build cmd/main.go && ./main --env=dev 读取本地默认配置，一般在etc/conf目录下app.toml
```



#### 5.4.3.2 远程配置模式

```shell
./main --env=dev --apolloAddr=[http://192.168.124.184:57071](http://192.168.124.184:57071/) --apolloAppId=com.example.apollo-go --apolloNamespaceName=application --apolloCluster=default
```



#### 5.4.3.3 本地配置文件模式

```
./main --env=local --config=/etc/conf/app.toml
```



### 5.4.4.参数验证基础库

#### 在entity目录下req.go文件写入,构造请求参数校验即可。

#### 具体如何使用请看 github.com/go-playground/validator/v10,使用案例如何

```go
type UserRequest struct {
   Email string `json:"email" validate:"required,email"`
   Name string `json:"name" validate:"required"`
}
```

## 5.5 小节



## 
