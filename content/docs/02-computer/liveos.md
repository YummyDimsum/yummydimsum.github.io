+++
title = '使用 Live USB 系统'
date = 2024-04-05
draft = false
weight = 7
+++
# 使用 Live USB 系统

从事敏感和危险工作的行动者一般分为两类，一种公开身份活动，一种完全匿名活动。前者并不需要隐藏真实身份，但可能希望保护信息、数据与通信安全，也就是有“加密”的需求。后者则不光要保护信息、数据与通信安全，还要保持匿名，不被别人识破身份，也就是同时需要“匿名”且“加密”。

这两类人的需求并不完全相同，但在很多场景之下需要类似的工具。

我们推荐从事敏感和危险工作的行动者学习制作和使用 Live USB 系统，也就是将操作系统（无论 Windows 还是 Linux）安装在一个小小的 U 盘上面，每次使用的时候，将 U 盘插在电脑上，选择从 U 盘启动并运行系统。使用结束之后，关闭系统和电脑，收起 U 盘。

这样做的好处是，你在公开使用的电脑和系统当中不会留下任何“敏感信息”和“敏感活动”，而且 Live USB 系统在关机之后可以清除所有使用记录，只留下一个干净的系统。这使得监控甚至抓捕你的人无法得到任何敏感信息和数据。

这些操作系统都可以安装在 USB 当中：[Windows 10](https://www.ubackup.com/articles/windows-10-live-usb.html), [Ubuntu Linux](https://ubuntu.com/tutorials/create-a-usb-stick-on-windows?ref=robododd.com#1-overview), [Tails Linux](https://tails.net/index.en.html),  [Whonix](https://www.whonix.org/wiki/USB_Installation), [antiS](https://github.com/mdrights/liveslak)。

它们大都是 GNU/Linux 系统，各有特色，适合不同需求的人，比如 Tails 和 Whonix 系统默认将所有网络请求和流量通过 Tor 网络转发，保证用户完全匿名。Windows 则适合大多数不熟悉 Linux 的用户。

可以用 [Rufus](https://rufus.ie/en/) 或 [UNetbootin](https://unetbootin.github.io/) 来制作 Live USB。详细方法请见各自的官方网站。
