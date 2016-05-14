---
layout:     post
title:      "关于HTTP请求那些你必须知道的"
subtitle:   ""
date:       2006-05-12 19:12:03
author:     "Paian"
catalog: true
tags:
    - HTTP
---

## 关于HTTP请求那些你必须知道的

### 一、HTTP是一种无状态的协议

HTTP是一种无状态的协议。什么是无状态呢？就是不建立持久的连接，即服务器不保留连接的相关信息。一个客户端向服务器发出请求，web服务器返回响应，然后连接就被关闭了，这个处理过程是没有记忆的。如果后续的处理过程需要之前的一些信息，那就需要重新传递。

### 二、一个完整的HTTP请求

一个完整的HTTP请求：

1、建立TCP连接

2、web浏览器向web服务器发送请求命令

3、web浏览器发送请求头信息

4、web服务器应答

5、web服务器发送应答头信息

6、web服务器向浏览器发送数据

7、web服务器关闭TCP连接

一个HTTP请求一般由四部分组成：

1、请求的方法和动作，比如是GET还是POST

2、正在请求的URL

3、请求头，包含一些客户端环境的信息，身份验证的信息等

4、请求体，也就是请求正文，请求正文中可以包含客户提交的查询字符串信息，表单信息等

请求和请求体之间有一个空行。

### 三、GET和POST请求

- *GET请求：*

一般用于信息的获取，

使用URL传递参数（对所有人都是可见的），

对所发送的信息的数量也有限制，一般在2000个字节

- *POST请求：*

一般用于修改服务器上的资源（安全性更好），

对所发信息的数量无限制。

### 四、响应的组成部分

一个响应一般由三个部分组成：

1、一个数字和文字组成的状态码，用来显示请求是成功还是失败

2、响应头，响应头也和请求头一样包含许多有用的信息，例如服务器类型、日期时间、内容类型和长度等

3、响应体，也就是响应正文

