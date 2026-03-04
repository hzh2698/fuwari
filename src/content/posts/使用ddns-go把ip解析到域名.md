---
title: 使用ddns-go把ip解析到域名
published: 2026-03-04
description: ""
image: ""
tags: []
category: ""
draft: true
---

# 引言
之前教大家把[域名托管到了cloudflare](/posts/托管域名到cloudflare/)，这次教大家使用自己的域名。使用域名的方法很多，这篇文章讲如何把ip地址解析到域名（即ddns)

鉴于大部分人都没有公网ipv4，这篇文章主要讲如何解析ipv6地址到域名。

# 确认自己是否有ipv6

先关闭所有代理工具，用浏览器访问[ipw.cn](https://ipw.cn/)，如果显示ipv6访问优先，则说明有公网ipv6地址。或者可以在光猫或者路由器的拨号页面看有没有获取到2409，2408，240e开头的ipv6地址，如果有则说明有公网ipv6地址。有公网ipv6地址的可以继续看下面的内容。如果显示没有ipv6就可以关闭这篇文章了。

# 下载工具

这篇文章用到的工具是ddns-go。先打开[ddns-go的github仓库](https://github.com/jeessy2/ddns-go)，点击右下方的releases

选择符合自己系统和cpu架构的文件下载（现在的windows电脑基本上都是x64架构，选择windows_x86_64）