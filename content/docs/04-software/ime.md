+++
title = '中文输入法'
date = 2025-08-10
draft = false
weight = 14
+++
# 中文输入法

许多人使用中国大公司开发的免费输入法，比如搜狗输入法、百度输入法、讯飞输入法等。

然而有研究表明，这些输入法普遍存在安全隐患，甚至可能主动收集用户的使用数据并偷偷上传到服务器。因此，**强烈建议你不要使用来自中国大公司的输入法**。好在，除了这些大公司的输入法，我们还有选择。

[RIME 中州韵输入法引擎](https://rime.im/)是开源软件，它不属于任何大公司，由一群志愿者维护，不会收集或上传你的个人数据。它可能不如商业输入法一样“智能”，但是它更安全。在不同的操作系统上，RIME 输入法有不同的名字，也有不同的安装和设置方法。

## 一、iOS 系统

iOS 系统自带的中文输入法可以使用，同时推荐另外两种：[Gboard](https://apps.apple.com/us/app/gboard-the-google-keyboard/id1091700242) 和基于 RIME 的“[仓输入法](https://apps.apple.com/us/app/%E4%BB%93%E8%BE%93%E5%85%A5%E6%B3%95/id6446617683)”。

Gboard 是 Google 出品的多语言键盘，支持超过 150 种语言的输入，但请注意它是来自商业公司的闭源软件。

## 二、Android 系统

不推荐使用 Android 系统自带的输入法，尤其不建议使用国产安卓手机的输入法。而是推荐另外两种：[Gboard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin), 和基于 RIME 的“[同文输入法](https://play.google.com/store/apps/details?id=com.osfans.trime)”。

Gboard 需要从 Google Play Store 或者 [APKPure](https://apkpure.com/gboard-the-google-keyboard/com.google.android.inputmethod.latin) 下载，同文输入法可以从 Google Play Store 或者 [F-droid](https://f-droid.org/packages/com.osfans.trime/) 下载。

需要注意的是，同文输入法没有九宫格键盘，在小屏幕手机上面使用可能不太方便。

##  三、Windows 系统里的 RIME：小狼毫输入法

1. 访问 RIME 网站，下载小狼毫输入法安装文件。安全起见，不要从其它地方下载。

	官方网站目前提供三种不同版本的小狼毫输入法下载，分别对应不同的 Windows 版本。请选择与你的系统版本对应的软件。
	
	https://rime.im/download/
	
	**提醒**：如果你还在使用 Windows 10 甚至 Windows 7 版本的系统，请[尽快升级到 Windows 11](/docs/02-computer/windows/)。

2. 安装下载好的小狼毫输入法安装文件，它的文件名应该类似于这样：**weasel-0.17.4.0-installer.exe**

3. 安装的时候，你可以顺便完成一些基本设置：

- **选择安装路径**

	默认安装在 C 盘。如果你不熟悉 Windows 的文件夹结构，建议你保留默认设置，就让它安装在 C 盘。

- **选择用户文件夹路径**

	如果你不熟悉 Windows 的文件夹结构，建议你让用户文件夹使用默认位置。

- **选择你需要的输入法**

	RIME 输入法引擎同时支持许多种输入法方案，你可以根据自己的需要来决定要保留哪些、取消哪些。像注音、仓颉等输入法，如果你不需要，就可以将它前面的 ✅️ 取消，再接着安装。如果没有在这一步选择取消，你就需要在安装结束之后手动修改配置文件，那会有些麻烦。

	![Windows RIME 选择输入法](/docs/images/rime-windows-im-selection.png)

- **选择输入法的主题（皮肤）**

	最后一步是选择你需要的主题，也俗称“皮肤”。完成这一步，如果没有出错（一般很少出错），小狼毫输入法就已经安装好了！

4. 日常使用小狼毫输入法。

	小狼毫输入法安装完毕之后，根据你安装时候的选择，可能默认会有“朙月拼音”和“朙月拼音・简化字”两种输入法。

	打开一个能够输入汉字的软件（比如记事本），通过点击电脑右下角托盘里的输入法图标，将输入法切换成 RIME。

	将光标固定在记事本中，按下 F4 键，就可以查看当前可用的输入法。这一操作也可以通过 **Ctrl+`**（该键位于 Tab 键的上方，数字 1 键的左边）组合快捷键实现，它与 F4 键的作用相同。

	使用上下方向键，选择你想使用的输入法，按回车键（Enter）确认你的选择。这样就可以开始用了。

## 四、macOS 系统里的 RIME：鼠须管输入法

1. 访问 RIME 网站，下载鼠须管输入法的最新版本。

	请注意选择正确的版本：鼠须管 0.16.2 版本针对 macOS 13 以下的系统，这个版本的鼠须管已经停止更新；鼠须管 1.0.3 版本针对 macOS 13 和更新版本的系统。
	
	https://rime.im/download/
	
	**提醒**：如果你还在使用 macOS 12 甚至更低版本的系统，请[尽快升级到 macOS 13 或更高版本](/docs/02-computer/macos/#二确保系统定期更新)。从 2024 年 10 月起，macOS 12 已经无法接收来自苹果公司的安全更新支持。

2. 安装鼠须管输入法

	你可以点击刚才下载到的 .pkg 文件安装，也可以使用 homebrew 安装。如果想使用 homebrew，你需要先安装 [homebrew](https://brew.sh/zh-cn/), 再在“终端”里面输入以下的命令。

	`brew install squirrel-app`

3. 配置鼠须管输入法

	安装完成之后，进入【系统偏好设置】→【键盘】→【输入法】，点击左下角的 + 号，在底部搜索框搜索“鼠须管”，然后选择“鼠须管”，点击“添加”。之后需要重启输入法，让刚才的变更生效。
	
	![macOS RIME config](/docs/images/macos-rime-1.png)

## 五、Linux 系统里的 RIME

如果你用的是比较常见的 Linux 系统，比如 Ubuntu，那么你的系统软件源里很可能已经包含 RIME 输入法。你需要 IBus 或者 Fcitx5（只需安装其中一个即可）来支持使用 RIME. 以下就以 Ubuntu 系统为例，说明怎样安装和设置 RIME 输入法。

### 选项一：安装 IBus 和 RIME

在终端里运行以下命令，安装所需的软件包：

`sudo apt install ibus-rime`
	
安装完成之后，在系统菜单里找到“**IBus 首选项**”，点击打开它（以下截图基于 Xfce 桌面环境，如果你使用不同的桌面环境，可能会看到不同的截图，但添加 RIME 输入法的过程与此类似）：
	
![IBus RIME](/docs/images/ibus-rime-1.png)
	
在“IBus 首选项”里，点击它的第二个标签页“输入法”：
	
![IBus RIME](/docs/images/ibus-rime-2.png)
	
点击“输入法”标签页右侧栏的“添加”按钮，就会弹出一个“选择输入法”的窗口：
	
![IBus RIME](/docs/images/ibus-rime-3.png)
	
在“选择输入法”窗口点击“中文”，然后点击选择“Rime”：
	
![IBus RIME](/docs/images/ibus-rime-4.png)

这样就安装并设置好了 IBus 和 RIME 输入法，在系统托盘的输入法图标上面点击右键，选择“重新启动”，只需一两秒钟，RIME 输入法就可以使用了。

### 选项二：安装 Fcitx5 和 RIME

在终端里运行以下命令，安装所需的软件包：

`sudo apt install fcitx5 fcitx5-chinese-addons fcitx5-rime librime-plugin-lua`
	
安装完成之后，在系统菜单里找到“**Fcitx 5 配置**”，点击打开它。

你会看到左、右两栏：左栏是“当前输入法”，也就是当前已经激活、可用的输入法；右栏是“可用输入法”，意味着这些输入法已经安装在系统里，但还未激活，暂时不能使用。在右栏里，找到“汉语”→“中州韵”，用鼠标选中它，如下图。（以下截图基于 Xfce 桌面环境，如果你使用不同的桌面环境，可能会看到不同的截图，但添加 RIME 输入法的过程与此类似。）

![fcitx 5 config](/docs/images/fcitx5-rime-1.png)

选中右栏的“中州韵”之后，点击两栏之间的向左箭头 ⬅️ 图标，就可以把右栏（可用输入法）的“中州韵”添加到左栏（当前输入法）。然后点击右下角的“应用”和“确定”，就算添加成功，如下图。

![fcitx 5 config](/docs/images/fcitx5-rime-2.png)

添加成功之后，点击系统托盘里的输入法图标，选择“重新启动”。你就可以开始使用 Fcitx 5 和 RIME 输入法。打开一个文字编辑器，用  **Ctrl+`** 组合键（或使用 F4 键）就可以查看可用的输入法，如下图。

![fcitx 5 config](/docs/images/fcitx5-rime-3.png)

以上只是介绍 RIME 输入法的基本安装方法和设置，并未包含高级设置内容。事实上，它的高级设置非常繁多复杂，甚至可以专门写好几篇教程。如果你只是想安装一种输入法来输入汉字，没有更多要求的话，以上方法已经够用。如果你想对 RIME 进行更复杂的设置，可以查看它的[官方文档](https://rime.im/docs/)，或参考其他网友分享的内容。
