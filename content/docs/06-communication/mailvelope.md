+++
title = '借助 Mailvelope 使用 PGP 加密邮件'
date = 2024-04-10
draft = false
weight = 33
+++
# 借助 Mailvelope 使用 PGP 加密邮件

传统上，使用 PGP 加密、解密邮件是件技术活，很多新手不知应该如何操作。Mailvelope 的出现总算让问题变得简单多了！

[Mailvelope](https://mailvelope.com/en/) 是一个浏览器扩展，可以安装在 Firefox（包括 LibreWolf）浏览器上。安装成功之后，如下设置和使用。

### 1. 第一步：为你的邮箱生成密钥

点击顶部菜单的 Key management, 会出现如下界面。

依次填入：你的名字（你想以什么名字来使用这个邮箱，由你决定）、电子邮箱，最后为你的秘钥设置密码，密码需要输入两次。然后点击右下角的 Generate 完成。

![Mailvelope](/docs/images/mailvelope01.png)

### 2. 第二步：查看你的密钥

完成第一步之后，Mailvelope 就会为你的邮箱生成一对密钥：私钥和公钥。

这时，你会在 Key management 列表当中看到你的邮箱和刚刚生成的秘钥。点击你的邮箱地址，就会看到密钥的详情，如下图。

![Mailvelope](/docs/images/mailvelope02.png)

### 3. 第三步：导出你的公钥

在第二步的界面中，点击右上角的 Export, 就可以导出自己的公钥（Public）和私钥（Private）。公钥要公开分享给全世界（至少要分享给你的通信对象），而私钥却要自己保管好，绝对绝对不能把私钥告诉任何人。

选择公钥（Public），你会看见一长串的随机字符，如下图。点击右下角的 Save, 就可以将公钥保存成一个 .asc 文件，将它保存在电脑里。

![Mailvelope](/docs/images/mailvelope03.png)

### 4. 第四步、将你的公钥分享给别人

公钥的作用是：当 A 想要给你发送加密邮箱时，A 要知道与你的邮箱对应的公钥。所以，你应该将公钥分享给别人。一般有这样几种做法：

- 将导出的公钥 asc 文件作为邮件附件，直接发送给通信对象。
- 将公钥的 fingerprint 信息放在邮件的签名里。请回到第二个步骤的图中，找到图中右下角的 fingerprint, 复制它后面那一串包含大写字母和阿拉伯数字的字符。将这一串字符完整地放在邮件签名里。别人通过这一串 fingerprint 就能找到你的 PGP 公钥。
- 将公钥的 .asc 文件或者 fingerprint 放在你的个人网站、社交媒体的介绍里，同时不要忘了附上邮箱地址，不然别人不知道要写信给谁。
- 将你的公钥 .asc 文件上传到专门的公钥服务器分享，别人在这些服务器上搜索你的邮箱地址，就能找到你的公钥。常见公钥服务器比如 [Mailvelope key server](https://keys.mailvelope.com/), [MIT PGP Key Server](https://pgp.mit.edu/), [OpenPGP key server](https://keys.openpgp.org/).

### 5. 第五步、导入通信对象的公钥

要给别人写一封 PGP 加密邮件，你需要知道对方的邮箱地址和 PGP 公钥。如果你还不知道，请直接找对方询问。如果对方没有 PGP 公钥，你可以按照以上方法帮其设置。

假设你已经知道 A  的邮箱和 PGP 公钥，它可能是一个 .asc 文件，也可能是非常长的一串随机字符。

在 Mailvelope 的 Key management 界面，点击 Import, 来到如下界面： 

![Mailvelope](/docs/images/mailvelope04.png)

如果 A 的 PGP 公钥是一个 .asc 文件，就点击上图中的 Add file, 选择 .asc 文件，然后点击右下角的 Import keys.

如果 A 的 PGP 公钥是一串随机字符，就全选、复制这串字符，然后在 Import 界面里点击 Import key from clipboard, 最后点击右下角的 Import keys.

以上两种方式的作用一样，取决于你拿到的公钥文件是什么样的。

### 6. 第六步、写一封加密邮件

要给别人发送 PGP 加密邮件之前，一定要将其公钥导入 Mailvelope. 我们在上一步已经完成导入。

点击 Mailvelope 顶端菜单里的 Encrypt. 会看到如下界面：

![Mailvelope](/docs/images/mailvelope05.png)


假设你要给 tigger@pooh.com 发送加密邮件，在 Recipient 的位置输入 tigger@pooh.com 的邮箱。由于你已经导入 Tigger 的公钥，所以 Mailvelope 会识别到 Tigger 的公钥。点击确认收件人。

然后在 Message 栏目输入你想要发送的邮件内容，你可以写很长很长的内容。最后点击这个界面左上角的 Encrypt 按钮，即可完成信息加密。如下图所示：

![Mailvelope](/docs/images/mailvelope06.png)

你可以点击下载 .asc 文件，也可以全选、复制密文全文。注意，密文全文包括开头的 **-----BEGIN PGP MESSAGE-----** 和结尾的 **-----END PGP MESSAGE-----**

然后将 .asc 文件（它的内容即是密文全文）作为邮件附件发送到 Tigger 的邮箱，或者复制密文全文，将其粘贴在邮件正文里发送给 Tigger。 这段密文使用 Tigger 的公钥加密，因此只有 Tigger 的私钥才能将其解密。其他人没有 Tigger 的私钥，即使能够截取这段密文，也无法将其解密还原成为人类可以读懂的文字。

那么，Tigger 收到密文之后要如何解密呢？请看下一步。

### 7. 第七步、解密一封加密邮件

假设收到密文的 Tigger 也使用 Mailvelope.

Tigger 将密文全文（记得包括开头和结尾）复制，然后打开 Mailvelope 顶端的 Decrypt 菜单，就会来到如下界面。将密文全文粘贴在 Text to decrypt 栏，然后点击右上角的 Decrypt 按钮。

![Mailvelope](/docs/images/mailvelope07.png)

由于这段密文使用 tigger@pooh.com 的公钥加密，因此当点击右上角的 Decrypt 按钮之后，Mailvelope 会要求输入 tigger@pooh.com 的密钥管理密码。还记得我们在第一步设置的密码吗？

如果密码正确，就有权使用 tigger@pooh.com 的私钥来解密这段密文。解密成功，Mailvelope 会生成一个可供下载的 txt 文档。

下载这个 txt 文档，将其保存在电脑里。使用记事本软件将它打开，即可看到解密之后的内容，也就是 Winnie 写的那句邮件内容“新年快乐！”。

由于这是加密邮件，建议你阅读之后马上将其删除，而不要永久保存。

以上就是使用 Mailvelope 加密和解密的全过程。
