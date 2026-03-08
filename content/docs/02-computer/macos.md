+++
title = '运行 macOS 的苹果电脑'
date = 2024-04-05
draft = false
weight = 5
+++
# 运行 macOS 的苹果电脑

## 一、决定购买和使用之前

苹果电脑由美国 Apple 公司生产，它的电脑硬件与操作系统之间有着强绑定关系。也就是说，当你购买苹果电脑的时候，意味着你选择使用 macOS 系统；当你想要使用 macOS 系统的时候，你就会购买苹果电脑。

这种强绑定关系的好处是，硬件与系统之间极其优良的配合，因为它的系统就是为它的硬件准备的。有些人会在苹果电脑上面安装 Windows 系统，或者在 PC 机上面安装 macOS 系统，虽然这样也能运行，但肯定无法像苹果电脑搭载 macOS 系统那样舒服和流畅。

但是这种强绑定关系同时也带来一些问题，这是你在决定购买和使用苹果电脑之前要知道的。你有可能会遭遇这种情况：

电脑硬件完好无损，无论是电池还是硬盘都能正常工作。但是，由于苹果公司不断发布新的 macOS 系统，而新版系统对于电脑硬件配置要求较高，使得你的电脑无法升级到最新版本的系统，或者即使能够升级，也不能流畅地使用。你无法仅仅通过升级主板、内存或者显卡使其满足最新版 macOS 系统的要求。很多人在这个时候会被迫买一台新的电脑，也就是硬件配置更高、操作系统更新的苹果电脑。

点击以下链接，检查你的苹果电脑硬件能够支持的最新版本系统是多少。

- MacBook Air https://en.wikipedia.org/wiki/MacBook_Air#macOS

- MacBook Pro https://en.wikipedia.org/wiki/MacBook_Pro#macOS

- iMac https://en.wikipedia.org/wiki/IMac#Supported_Apple_operating_system_releases

根据上面的链接内容所示：

- 如果你使用 MacBook Air 电脑，想要升级到最新的 macOS 14 版本系统，那么你的 MacBook Air 机器至少需要是 2018 年版本。早于 2018 年的机器已经无法升级到 macOS 14 版本的系统。

- 如果你使用 MacBook Pro 电脑，想要升级到最新的 macOS 14 版本系统，那么你的 MacBook Pro 机器至少需要是 2018 年版本，早于 2018 年的机器已经无法升级到 macOS 14 版本的系统。

- 如果你使用 iMac 台式电脑，想要升级到最新的 macOS 14版本系统，那么你的 iMac 机器至少需要是 2019 年版本，早于 2019 年的机器已经无法升级到 macOS 14 版本的系统。

*提示：上述状况的解决办法之一是这样，如果你熟悉 GNU/Linux 操作系统，当你的苹果电脑无法再升级到最新版本 macOS 的时候，你可以将 macOS 从电脑中完全清除，为它安装某种占用硬件资源较少的 GNU/Linux 发行版。*

如果你可以选择，建议购买内存（RAM）至少 16GB 的苹果电脑，这样可以使电脑与软件运行更加顺畅。

## 二、确保系统定期更新

每个版本的 macOS 系统都有一定的“寿命”，即支援期限，一般小于四年。

比如 2019 年发布的 macOS 10.15 版本已于 2022 年 11 月停止安全更新；2020 年发布的 macOS 11 版本已于 2023 年 9 月停止安全更新。

如果苹果公司不再针对你所使用的系统提供安全更新，那么你的系统就比较容易受到攻击和入侵。这时应该尽快给系统升级，将它升级到能够接收官方安全更新的版本（不一定是最新版本的系统，但需要保证它是一个能够接收安全更新的系统）。

首先要确定自己正在使用哪个版本的 macOS. 进一步确认苹果公司是否仍然对这个版本的系统提供安全更新。搜索系统名称和版本号（比如搜索 macOS 12），即可在苹果公司官方网站或者维基百科页面看到这个版本系统的详情，查看其中的 "support status"（支持状态），确认是否仍然可以接收官方安全更新。

比如下图，来自英文维基百科 macOS 页面的 Timeline of releases 表格( https://en.wikipedia.org/wiki/MacOS#Timeline_of_releases )，用三种不同颜色标出不同版本的系统。绿色背景（macOS 15.6）是最新版系统；黄色背景（macOS 13.7.7 和 14.7.7）是较旧的版本，但苹果公司仍然提供安全更新；浅红色背景（macOS 11.7.10 和 12.7.6）是较旧的版本，而且苹果公司已经不再提供安全更新。

![macOS version](/docs/images/macos-version.png)

截止2026年3月，请你确保自己使用的 macOS 系统最低版本是 macOS 14, 它还能够接收官方安全更新。如果小于这个版本，请尽快给系统升级。

虽然保持电脑系统更新不能百分之百保证系统安全，但如果没有保持系统更新，肯定会面临更大风险。

## 三、开启防火墙并安装杀毒软件

针对 macOS 系统的防火墙软件，推荐以下几种：

- Radio Silence

https://radiosilenceapp.com/

- Security Growler

https://pirate.github.io/security-growler/

针对 macOS 系统的杀毒软件，推荐使用以下几种：

- AVG

https://www.avg.com/zh-tw/avg-antivirus-for-mac#pc

- Avira 

https://www.avira.com/zh-cn/free-antivirus-mac

## 四、更多安全设置

以下这个网页包含详细的 macOS 系统安全设置，请仔细阅读并按照其中指示操作。

https://securityinabox.org/zh/phones-and-computers/mac/

其中有些链接指向苹果公司（macOS 系统的开发者）官方网站，默认显示英文内容。点击打开这些链接之后，你可以将网页拉到最底部，在网页底部的右下角，可以看到语言切换按钮（如下图红色方框处），点击这个按钮，然后选择“中国大陆”，即可阅读中文版的指南。

![macOS Apple website](/docs/images/macos-apple.png)

这里还有一份详细完整的 macOS 安全指南（英文），如果你想让自己的苹果电脑更加安全，推荐仔细阅读。

https://drduh.github.io/macOS-Security-and-Privacy-Guide/

对于不太熟悉计算机的普通用户而言，这份指南过于复杂。但请你至少设置完成其中一些比较基础的部分。
