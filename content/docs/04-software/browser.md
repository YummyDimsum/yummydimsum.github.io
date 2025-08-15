+++
title = '网页浏览器'
date = 2024-04-10
draft = false
weight = 15
+++
# 网页浏览器

首先，无论电脑还是手机，都不要使用中国公司的浏览器。

中国公司的浏览器种类繁多，无法在此一一列举，这里只能给出我们推荐使用的浏览器并解释原因。

## 一、Windows 系统和 macOS 系统

推荐使用 Firefox, LibreWolf, Brave, Mullvad 这几种浏览器。

### 1. Firefox 浏览器

https://www.mozilla.org/en-US/firefox/all/#product-desktop-release

【请注意】<u>**一定不要使用中国版的 Firefox**</u>

怎样区分中国版和国际版？中国版的网站是 www.firefox.com.cn, 国际版的网站是 www.mozilla.org

在中国大陆地区直接访问 www.mozilla.org 有可能会被自动跳转到 www.firefox.com.cn , 所以你也可以直接点击这个链接，进入国际版 Firefox 的下载页面。 https://www.mozilla.org/zh-CN/firefox/new/

### 2. LibreWolf 浏览器

https://librewolf.net/

LibreWolf 基于最新版 Firefox 浏览器改进而来，它在 Firefox 的基础上增加了一些安全设置，比如默认开启“增强跟踪保护”功能的“严格”模式，从而主动阻止网站上的跟踪器。不过这可能会导致个别网页无法正常打开，好在它大多数时候都能正常使用。

更多关于它的特性，可以查看这里： https://librewolf.net/docs/features/

### 3. Brave 浏览器

https://brave.com/

Brave 浏览器默认有许多安全设置，比如拦截广告和追踪器，以及浏览器自带的一个 VPN 服务。浏览器本身免费，但 VPN 服务收费。

### 4. Mullvad 浏览器

https://mullvad.net/en/browser

Mullvad 浏览器由 [Mullvad VPN](https://mullvad.net/) 团队和 [Tor 浏览器](https://www.torproject.org/)团队（后面的章节就会提到这两种工具）合作开发。它默认就有许多安全设置，比如开启隐私浏览模式，安装两款最知名的安全防护扩展：uBlock Origin 和 NoScript，而且将浏览器时区设置成 UTC 时区，从而不暴露你的真实时区等等。

这里有一个详细的清单，介绍 Mullvad 浏览器通过怎样的设置来增强安全性：  https://mullvad.net/en/browser/hard-facts

另外还有 [Tor 浏览器](https://www.torproject.org/)可以帮助在线匿名。详细请看《上网安全》一章[相关小节](/docs/05-internet/tor/)。

### 5. 不推荐使用

不推荐使用 Windows 系统自带的 Edge 浏览器和 macOS 系统自带的 Safari 浏览器。除非有些网站特别声明必须使用 Edge 浏览器，也只在这种情况下才使用。

也不推荐使用 Google Chrome 浏览器，虽然它已经成为全世界最流行的浏览器，但它在保护用户隐私方面做得并不理想。Google 公司[公开承认](https://www.solidot.org/story?sid=77157)，即使在“隐身模式”里，Google 也仍然在收集 Chrome 用户的访问记录。

## 二、iOS 系统

推荐使用 Firefox, Brave 或 DuckDuckGo 浏览器，你可以在 App Store 里找到它们。

不推荐使用系统自带的 Safari 浏览器。iPad 请按照同样原则选择。

另外还有 [Onion Browser](https://onionbrowser.com/), 它是基于 Tor 网络运行的浏览器，也有助于帮助在线匿名。

## 三、Android 系统

推荐使用 Firefox, Brave 或 DuckDuckGo 浏览器，不推荐使用系统自带的各种浏览器。尤其<u>**不要使用国产安卓手机自带的浏览器**</u>！

如果手机的应用商店里找不到这几种浏览器，可以使用 [APKPure](https://apkpure.com/) 或者 [F-droid](https://f-droid.org/) 下载安装，具体操作方法，可以参考第三部分关于“[安卓手机](/docs/03-mobile/android/)”的相关内容。

Tor 浏览器也有 Android 版本，可以从 [Google Play Store](https://play.google.com/store/apps/details?id=org.torproject.torbrowser) 或 [F-droid](https://tb-manual.torproject.org/zh-CN/mobile-tor/) 下载。

## 四、检查浏览器是否足够安全

无论使用哪种浏览器，如果没有做好安全设置，也有可能会暴露你的很多上网记录和历史。

比较常见和知名的安全隐患是 WebRTC. 如果浏览器没有禁用 WebRTC 功能，即使你使用 VPN，浏览器也会泄漏你的真实 IP 地址。访问以下这个网页，查看你的浏览器是否有 WebRTC 泄漏问题。

https://browserleaks.com/webrtc

如果看到这一行字（如下图），说明你的浏览器没有 WebRTC 泄漏问题。

![WebRTC leak test](/docs/images/webrtc.png)

以上推荐的几种浏览器，有些已经默认禁用 WebRTC, 有些则没有禁用。可以通过安装浏览器扩展来禁用。详细[请见后文](../extension/)。
