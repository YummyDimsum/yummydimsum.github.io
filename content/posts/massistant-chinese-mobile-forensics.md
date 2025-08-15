---
date: 2025-07-20
linktitle: 2025年7月：中国警察新的移动取证工具Massistant
menu:
  main:
    parent: translation
title: 2025年7月：中国警察新的移动取证工具Massistant
weight: 10
---
安全调查公司Lookout近期发布文章称，发现中国警方新的移动取证工具“Massistant”。以下是全文翻译，原文链接： https://www.lookout.com/threat-intelligence/article/massistant-chinese-mobile-forensics

标题：Lookout发现中国的移动取证工具Massistant

- “Massistant”被认为是2019年报道的中国取证工具“MFSocket”的后继产品，该工具归属于上市的网络安全公司美亚柏科。
- 该取证工具与相应的桌面软件配套使用。
- “Massistant”获得设备的GPS位置信息、短信、图片、音频、联系人和电话服务等访问权限。
- 美亚柏科与国内外执法部门保持合作关系，不仅作为监控硬件和软件的提供商，还通过为执法人员提供培训项目进行合作。
- 前往中国大陆及在中国大陆内部旅行，可能会导致游客、商务旅客和相关人员的机密移动数据被国家警方作为合法监听措施的一部分获取。

[Lookout威胁实验室](https://www.lookout.com/resources/threat-lab)的研究人员发现了一款名为“Massistant”的移动取证应用程序，供中国执法部门从移动设备收集大量信息。据信，该应用程序是“MFSocket”的后继产品，媒体曾在2019年报道过警察使用“MFSocket”取证。这些样本需要物理访问设备才能安装，并且没有通过Google Play商店分发。
‍
取证工具被执法人员用于从没收的设备中收集敏感数据，或在被执法人员拦截时使用。

这些工具可能对那些经常有高管和员工前往国外、尤其是前往边境管控严格的国家的企业构成风险。

2024年，[中国国家安全部引入了一项新立法](https://www.rfa.org/english/news/china/security-police-check-devices-05082024130107.html)，允许执法人员在无需搜查令的情况下收集和分析设备。有传闻称，中国执法部门对商务旅行者的设备进行了收集和分析。在某些情况下，研究人员在被执法部门扣押并归还的设备上发现了持久的、无界面的监控模块，以便在设备归还后仍能继续监控移动设备活动。

## Massistant：美亚柏科“MFSocket”的后继产品

2019年6月，一位名叫[Muyi Xiao](https://x.com/muyixiao)的中国记者发布一条推特评论（后来被删除），提到一种在中国社交媒体平台上被讨论的新型移动监控工具。据Xiao所述，一些中国网友声称他们的移动设备上被警察安装了一个名为“MFSocket”的应用程序。Xiao说这一监控工具属于一家上市的中国科技公司：厦门市美亚柏科信息股份有限公司。

随后，网络安全研究员巴蒂斯特·罗伯特（也被称为@fs0c131y）2019年6月公开分享了他对该应用的[分析](https://medium.com/@fs0c131y/mfsocket-a-chinese-surveillance-tool-58e8850c3de4)。在分析报告中，他指出签名证书显示美亚柏科是“MFSocket”应用程序的开发者。这些细节似乎证实了肖的说法。

自从那次报告以来，Lookout研究人员发现了一个名为“Massistant”的相关取证应用程序，我们认为这是“MFSocket”的后继产品。这些样本是在2019年中至2023年初之间获得的，主要使用引用美亚柏科的Android签名证书签署。

中国问答论坛显示，用户提到一个同名的应用程序，据称是警方以类似于“MFSocket”的方式安装在他们设备上的。

这些论坛帖子可以追溯到2020年年中，似乎支持了这样一种假设，即该工具是为了取代美亚柏科“手机大师”生态系统中的“MFSocket”移动组件而引入的。

根据一位[百度知道用户的说法](https://zhidao.baidu.com/question/530569080813144245.html)，国家公安部网站称卸载该软件是违法的，尽管Lookout的研究人员并未在公安部网站上发现与“Massistant”有关的任何内容。

与“MFSocket”类似，“Massistant”与桌面取证软件配合工作，从受损设备中提取数据。因此，取证工具不是连接到服务器，而是通过与“MFSocket”相同的10102端口连接到本地主机。可能是桌面组件通过端口转发服务（如 Android 调试桥提供的服务）与受损设备通信。

启动时，用户被提示同意一系列的访问权限请求，包括设备GPS位置数据、短信、图像、音频、联系人和电话服务，不需要其他交互。如果用户尝试退出应用程序，他们会收到一条通知，表示应用程序处于“获取数据”模式，退出将导致某些错误。此消息仅翻译为两种语言：中文（简体）和美国英语。

除了相同的端口引用外，“Massistant”和“MFSocket”还有其他许多相似之处。它们的代码显然有很大程度的重叠，“Massistant”明显是在较旧的“MFSocket”版本 5.0 应用程序基础上的一个迭代版本，并且它们被分配了相同的应用程序图标。此外，许多早期版本的“MFSocket”中的命令也被包含在“Massistant”中。

在大多数情况下，当两个应用程序共享功能时，它们的类是相同的。此外，“Massistant”包含一个名为“mfsocket.xml”的 XML 资源文件。

虽然目前“Massistant”似乎无法在离开桌面对应部分后从设备中提取数据，但它在设备上的存在以及任何日志细节或数据文件都会向设备所有者表明，如果设备被没收，他们的移动设备数据已被泄露。

与“MFSocket”类似，“Massistant”使用USBBroadcastReceiver，在USB断开连接时自动从设备中卸载。据推测，曾经发生过自动卸载失败的情况，导致中国网民在被中国当局没收设备后发现了这个多出来的应用程序。

新的“Massistant”应用程序在“MFSocket”功能集上引入了许多附加功能。通过一系列类引入了AccessibilityServices，这些类被美亚柏科开发人员称为“自动点击”（AutoClick），尝试自动绕过某些设备安全应用程序中的条件，例如在Miui安全中心工具提示时，自动允许“Massistant”运行。

“Massistant”的最新版本v8.5.7还引入了通过WiFi使用Android调试桥（ADB）连接被扣押设备的功能，并可向设备下载额外文件。此功能通过名为libNativeUtil.so的原生库实现。美亚柏科的中文商业网站曾在公告中提及将在2024年5月对移动大师系列产品的该功能进行进一步更新，但Lookout的研究人员尚未发现“Massistant”客户端的更新版本。

“Massistant”还引入了对第三方消息应用程序的额外支持。原来的“MFSocket”从Telegram收集应用数据；“Massistant”已拓展了这一功能，以收集来自Signal和Letstalk的消息数据。

## “MFSocket”和美亚柏科的关联

在调查过程中，Xiao发现了一份由美亚柏科发布的指南。[指南](https://web.archive.org/web/20190121075252/http://vlambda.com/wz_wHjxS7RIQb.html)中写道：“在取证过程中……DC-4501V2、DC-4700V2或FL-900V2手机取证系列会将MFSocket.apk推送到手机进行安装……”。这些版本代码指的是工具的第二个版本，即在中文美亚柏科网站300188[.]cn上宣传的“美亚柏科移动大师系列”。该商业网站以公司在深圳证券交易所的股票代码（300188）命名。公司还在meiyapico[.]com上提供英文和俄文网站。

2020年4月，美亚柏科在其官网发布声明，宣布停止对DC-4500/DC-4501V1、DC-4700V1和FL-900V1产品的升级，并将推出一套同名的新工具套件，这些产品将从Xiao分享的指南中提到的V2版本升级到V3版本。Lookout研究人员对于大约在这个时候“MFSocket”被“Massistant”所取代的判断持低可信度态度。

## 厦门美亚柏科信息股份有限公司

厦门美亚柏科信息股份有限公司（“美亚柏科”）是一家上市的中国科技公司，约占[中国大陆数字取证市场份额的40%](https://www.scmp.com/tech/start-ups/article/3017688/what-you-need-know-about-meiya-pico-chinas-low-profile-forensics)。

2023年12月，美亚柏科更名为国投智能（厦门）信息股份有限公司。然而，“MFSocket”和“Massistant”的签署证书仍将美亚柏科列为软件的开发组织。

记者们经常报道美亚柏科参与中国商业监控市场，其工具[被执法部门用于对该地区少数群体的监视](https://www.scmp.com/tech/start-ups/article/3017688/what-you-need-know-about-meiya-pico-chinas-low-profile-forensics)。2025年4月，Turquoise Roof的研究人员发布了[一份报告](https://turquoiseroof.org/a-long-shadow-the-expansion-and-export-of-chinas-digital-repression-model-in-tibet/)，详细说明该公司为位于拉萨的西藏警察学院提供培训和工具的采购情况。

美亚柏科经常宣传他们参与中国和国际执法产品展销会，包括国际刑警组织世界展销会。事实上，[美亚柏科以与众多国际政府客户的合作关系而自豪](https://www.aspi.org.au/report/mapping-more-chinas-tech-giants)，其中包括购买其法证和移动监控产品的俄罗斯军方。

截至2018年，据[报道](https://archive.is/w9lP8)，俄罗斯联邦调查委员会的军事调查局（военное следственное управление Следственного Комитета РФ）通过承包商“ExpertExpress LLC”购买了两款美亚柏科产品，即iDC-8811 Forensic Magicube V3和iDC-4501 Mobile Forensics System V2。这两款产品与Cellebrite的IFM-2008 Forensics Master套件一起，于2018年以500万卢布（约合74,000美元）的价格购买。这笔俄罗斯采购旨在帮助俄罗斯的军事刑事调查，并未针对外国受害者。

然而，俄罗斯的购买很可能后来被取消，因为出售公司ExpertExpress及其分包商Ester Solutions使用伪造许可证将美亚柏科解决方案出售给俄罗斯军方的调查委员会。2018年10月，Ester Solutions的所有者德米特里·萨图琴科因大规模欺诈指控被逮捕。

美亚柏科还受中国公安部的指示，负责培训“一带一路”倡议相关国家的代表进行数字取证调查。截至2019年9月，有[29个国家](https://public.opentech.fund/documents/English_Weber_WWW_of_Information_Controls_Final.pdf)被列为该倡议的参与者。

在2021年，美亚柏科被美国政府外国资产控制办公室根据[CMIC-EO13959计划](https://sanctionssearch.ofac.treas.gov/Details.aspx?id=33896)[实施制裁](https://ofac.treasury.gov/recent-actions/20211216)，该计划名为“对中国军事公司的制裁”。其声明的目标是：“[应对对共产党中国军队公司券融资的威胁](https://en.wikipedia.org/wiki/Executive_Order_13959)”。

## 结论

前往中国和在中国大陆旅行的游客、商务旅行者和相关人员可能面临机密手机数据被国家警察合法拦截的风险。Lookout客户可以免受“MFSocket”和“Massistant”的威胁。如果您认为您的设备可能已被入侵，请通过[此处](https://www.lookout.com/form/report-mobile-incident)联系我们。
