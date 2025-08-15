+++
title = '即时通讯软件'
date = 2024-04-10
draft = false
weight = 17
+++
# 即时通讯软件

我们这里只推荐“**端对端加密**”的即时通讯软件。

所谓“端对端加密”的意思是，发送者发出的信息会被加密，直到接收者收到信息才会被解密。信息在传输过程中不会被第三方读取，因为第三方没有解密的“密钥”。

## Signal

https://signal.org/

端对端加密聊天软件，支持所有操作系统，可以设置聊天记录自动删除时间。

需要使用手机号码注册，但在注册完成之后，可以设置隐藏手机号码，采用唯一的用户名作为身份标识。

这是目前使用人数较多的安全通讯软件之一，我们专门撰写了一个页面介绍怎样使用和设置它，[点击这里](../signal/)阅读。

## Matrix

https://matrix.org/

端对端、去中心化的匿名聊天软件，不需要手机号码就能注册。有网页版、电脑客户端和手机客户端。

如果对匿名要求比较高，建议只使用网页版，而且只在 Tor 浏览器里使用。网页版地址： https://app.element.io

详细使用方法，可以参考这个教程：

https://matters.town/@thistlf/90530-matrix-%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%8C%96-%E5%8C%BF%E5%90%8D-%E5%AE%89%E5%85%A8%E7%9A%84%E5%8D%B3%E6%97%B6%E9%80%9A%E4%BF%A1-bafyreifwvmwayjpdhmtenxilxnccmjsmkoq4lu7v7au37bob6i4oi7o6he

## Element

这是 Matrix 是一个具体实现。所以同样具备端对端、去中心化、匿名的特点。

不需要手机号码就能注册。有网页版、电脑客户端和手机客户端。

如果对匿名要求比较高，建议只使用网页版，而且只在 Tor 浏览器里使用。网页版地址： https://app.element.io

Matrix 与 Element 的角色分工大致是这样：

- Matrix 提供并维护世界上最大的 Matrix 服务，也就是 [matrix.org](https://matrix.org)
- Element 提供世界上使用最为广泛的 matrix 客户端，也就是 [element.io](https://element.io)

## Session

https://getsession.org/

端对端加密聊天软件，支持所有操作系统。

基于 Signal 开发，并进一步加强安全与隐私。可以设置聊天记录自动删除时间。注册无需手机号码或邮箱。处于早期开发阶段。

## Delta Chat

https://delta.chat/zh_CN/

端对端加密聊天，支持所有操作系统。

基于电子邮箱，可以直接从 Delta Chat 客户端发出信息，对方在自己的邮箱收到信息。

## Briar

https://briarproject.org/

端到端加密聊天软件，仅支持 Android 系统。

它的特点是即使没有联网也能通过蓝牙与附近的人通信。

## Gajim

https://gajim.org/

基于 [XMPP 协议](https://xmpp.org/)的软件，端对端加密，支持 Windows 和 Linux 系统。

## ChatSecure

https://chatsecure.org/

端对端加密，仅支持 iOS 系统。

## Telegram

https://telegram.org/

Telegram 是非常流行的聊天软件，但要特别提醒的是，Telegram 早已被中国政府盯上，而且盗号现象严重，<u>**我们不推荐大家使用**</u>，除非你知道怎样使用和设置让它更安全。
