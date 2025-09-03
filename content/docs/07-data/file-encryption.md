+++
title = '文件加密以及常见加密软件'
date = 2024-04-10
draft = false
weight = 37
+++
# 文件加密软件推荐和使用方法

## 为什么需要加密文件

无论是自己保存重要文件，还是给别人传送、分享重要文件，最好都将文件加密，而不是直接存储和传输。

直接存储和传输的风险显而易见，只要文件被别人拦截获取，其中的内容——无论是个人隐私还是商业机密——就会全部暴露。

对于行动者来说，还要考虑到来自国家机器的威胁，

## 几种推荐的文件加密软件

推荐三种文件加密软件：VeraCrypt，PicoCrypt，和 Cryptomator。

### 1. VeraCrypt

VeraCrypt 的操作有些复杂，请看本站这个[专门介绍 VeraCrypt 用法的页面](/docs/07-data/veracrypt/)。

### 2. PicoCrypt

1. 下载安装

	https://github.com/Picocrypt/Picocrypt/releases

	以上链接是唯一提供 PicoCrypt 软件的正规途径，请不要从其它任何地方下载 PicoCrypt。

	这是一款非常轻量的文件加密软件，界面非常简单，使用也很简单，但它的加密功能却一点都不弱。

	它支持 Windows, Linux 和 macOS 系统，还有命令行界面和一个简单的网页端（ https://picocrypt.github.io/ ），不过网页端的功能比较有限。

	开发者2025年8月初将项目页面归档，意味着不再开发和维护这个软件，但仍提供下载。这仍然是一款值得信任的加密软件。

2. 基本加密和解密操作

	PicoCrypt 只有下图这一个操作界面，所有操作都在这里完成。

	![PicoCrypt](/docs/images/picocrypt-1.png)

	把你想要加密的文件或文件夹拖拽到 PicoCrypt 里，然后为给设置密码。可以自己输入密码，也可以用它自带的生成密码（Create）功能。

	![PicoCrypt](/docs/images/picocrypt-2.png)

	生成密码的时候，可以自己设置密码强度：包含多少位字符、是否包含字母、是否包含数字等等。密码生成之后，会自动复制到剪切板，请一定妥善保存密码，否则就无法解密文件。

	如果只是简单的加密，设置完密码就可以了。然后点击最底部的“Encrypt”按钮，文件就会自动加密。加密之后的文件扩展名是 .pcv。

	![PicoCrypt](/docs/images/picocrypt-4.png)
	
	解密的时候，把已经加密的 .pcv 文件拖拽到 PicoCrypt 里，输入密码，点击“Decrypt”按钮即可。（如果设置了 keyfile，还需要导入 keyfile。）
	
	注意，PicoCrypt 只能识别 .pcv 扩展名的文件并进行解密，其它扩展名的文件都会被视作需要加密的文件，而不是需要解密的文件。
	
3. 高级加密特性

	PicoCrypt 还有几个高级加密功能值得介绍：

	- 支持密钥文件。像许多加密软件一些，PicoCrypt 也支持密钥文件。你可以导入已有的密钥文件，也可以让 PicoCrypt 帮你生成一个密钥文件，甚至可以按顺序导入多个密钥文件。注意：如果导入多个密钥文件来加密，顺序非常重要，也就是说，解密文件的时候，要用同样的顺序导入这些密钥文件。

	- Paranoid mode，偏执模式，可以理解为最高级别的安全保护。官方文档里说，如果你是手持绝密文件、面临威胁的举报人，最好就使用这个模式加密。用法也很简单，在 Paranoid mode 前面的方框里打勾 ✅️ 即可。

		**注意**：不要与 Deniability 模式同时使用。

	- Reed-Solomon，里德-所罗门模式。如果你想把文件加密之后长期存放在云端或者移动硬盘，推荐使用这种模式。在这种模式里，即使你的文件有一部分损坏（3%以内），PicoCrypt 仍然能够纠正错误并解密文件。

	- Deniability，否认能力，简单说就是假装自己并没有给文件加密。设想一种场景，警察正在检查你的电脑，发现有几个疑似“已加密文件”的文件，可能会进一步怀疑你想隐藏什么东西，进而逼迫你交出解密的密码。如果想避免这种情况发生，就从源头上解决它，Deniability 既能帮你加密文件，又让已加密文件看上去像个普通文件，而不是那么明显的已加密文件。

		**注意**：不要与 Paranoid mode 同时使用，因为 Deniability 会让 Paranoid mode 的额外安全措施失效。

### 3. Cryptomator

1. 下载安装

	https://cryptomator.org/

	Cryptomator 支持 Windows, Linux 和 macOS，桌面版免费；也支持 Android 和 iOS，不过都要收费，Android 版 $16, iOS 版 $9.99（在不同国家的价格可能略有差异）。
	
2. 加密操作

	- **添加保险库**。打开已经安装好的 Cryptomator，点击左下角的 ➕ 图标，添加一个新的保险库。所谓**保险库**，就是一个由 Cryptomator 加密的文件夹。
	
	![Cryptomator](/docs/images/cryptomator-1.png)
	
	- **给保险库命名**。设置一个方便识别的名字，但最好不要透露加密文件的内容。比如 `summerTravel` 这个名字就比 `JulyProtest` 更好一些，因为前者看上去更普通，不容易引起注意。
	
	![Cryptomator](/docs/images/cryptomator-2.png)

	- **选择保险库的存储位置**。选择电脑系统的某个位置，或者移动硬盘的某个位置，用于存储加密保险库。
	
	![Cryptomator](/docs/images/cryptomator-3.png)
	
	- **设置保险库的密码**。请设置尽量长且复杂的安全密码。具体请参考点心指南[关于密码的页面](/docs/04-software/password/)。
	
	![Cryptomator](/docs/images/cryptomator-4.png)
	
	- **妥善保存恢复密钥**。设置密码的时候，请同时创建恢复密钥。在同一个页面里，选择“好的，有备无患”。Cryptomator 就会生成由许多个英文单词组成的恢复密钥。请一定妥善保管恢复密钥，它是你唯一可以重置保险库密码的凭证。
	
	![Cryptomator](/docs/images/cryptomator-5.png)
	
3. 解密操作

	- **输入密码，简单解密**。只须打开 Cryptomator 软件，就能看到你创建的所有保险库，选择想要解密的保险库，输入对应的密码，就可以解密。解密之后，你就可以进入文件夹，查看或修改其中的文件。操作完成之后，关闭 Cryptomator 即可。
	
	![Cryptomator](/docs/images/cryptomator-7.png)
	
	只有通过 Cryptomator 打开保险库，才能看到其中真正存储的文件。（如下图）
	
	![Cryptomator](/docs/images/cryptomator-8.png)
	
	如果没有通过 Cryptomator 打开，而是直接从文件管理器打开保险库，看到的只是一堆经过加密的文件。（如下图）
	
	![Cryptomator](/docs/images/cryptomator-9.png)
	
4. 注意：Cryptomator 并不适用于所有人
	
	Cryptomator 虽然简单易用，但它并不一定适用于每一个人。尤其是那些身处危险环境的活动家，如果你可能会被警察盘查，或者被检查电子设备，那最好不要用 Cryptomator 来加密，因为它容易暴露你“正在加密文件”，这可能会让警察进一步怀疑你想隐藏什么。
	
	对于身处危险环境的活动家，我们建议你使用 VeraCrypt 或者 PicoCrypt，它们的“否认能力”（Deniability）功能，可以一定程度隐藏你“正在加密文件”这一事实，从而避免引起警察进一步的怀疑。
