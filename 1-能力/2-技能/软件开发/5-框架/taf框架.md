# JCE语言

## 每一个JCE对象定义了一个接口及其操作。接口、操作和客户端和服务器之间交换的数据类型采用JCE语言定义。JCE可以用与编程语言和机器无关的方式定义客户端和服务端的通信协议。JCE定义被JCE翻译器翻译成某个编程语言的代码。也就是说，与协议相关的API是自动生成的代码定义的。

# JCE语言映射

## C++

## GO

# 客户端和服务段结构

## 子主题

#  ![](https://docimg7.docs.qq.com/image/hOrKwD-A9LrqQ-Y6F7Jflg.png?w=1098&h=664)taf提供的服务

## TafRegistry

## TafPatch

## TafNode

## TafLog

## TafStat

## TafConfig

## TafProperty

# 简介

## TAF的全称是Total Application Framework或者Tencent Application Framework，是网络应用程序的中间件，介于应用层与传输层之间，提供了远过程调用(RPC)的接口，简化了网络程序的编写，使得程序员从Socket编程接口中解放出来将精力放在业务逻辑(Business logic)的编写上

# 整体架构图

## 子主题

#  ![](https://docimg2.docs.qq.com/image/j87-HlwXcvIwPpOKgzEWeA.png?w=729&h=456)协议层次

##   

#  ![](https://docimg5.docs.qq.com/image/kujUlk9VlM45rksg_P1f0A.jpeg?w=209&h=115)术语

## JCE对象

### 可以有多个实例

### 可以有多个接口

#### 每个接口可以有多个操作

### 有单独的对象标识，用于区分不同的对象

## proxy

### JCE对象的本地大使， 客户端通过代理与目标对象通信

### 分类

#### 直接代理

##### 直接将地址写死的代理

#### 简介代理

## Locator

### 定位服务

### Taf所提供的TafRegistry就是这样一个定位服务

## Replication

### 一个对象有多个实例， 通过副本集冗余实现高可用

### 多实例无状态 或者 共享数据库

## Servant

### JCE对象中某个操作的实现

## 调用方式

### 同步调用

### 异步调用

### 单向调用