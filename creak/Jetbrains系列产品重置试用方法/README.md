[原文地址](https://zhile.io/2020/11/18/jetbrains-eval-reset.html)

---

## 原文内容

### 0x0. 项目背景
Jetbrains家的产品有一个很良心的地方，他会允许你试用30天（这个数字写死在代码里了）以评估是否你真的需要为它而付费。
但很多时候会出现一种情况：IDE并不能按照我们实际的试用时间来计算。
我举个例子：如果我们开始了试用，然后媳妇生孩子要你回去陪产！陪产时我们并无空闲对IDE试用评估，它依旧算试用时间。（只是举个例子，或许你并没有女朋友）
发现了吗？你未能真的有30天来对它进行全面的试用评估，你甚至无法作出是否付费的决定。此时你会想要延长试用时间，然而Jetbrains并未提供相关功能，该怎么办？

事实上有一款插件可以实现这个功能，你或许可以用它来重置一下试用时间。但切记不要无休止的一直试用，这并不是这个插件的本意！

### 0x1. 如何安装
1. 插件市场安装：
在Settings/Preferences... -> Plugins 内手动添加第三方插件仓库地址：https://plugins.zhile.io
搜索：IDE Eval Reset插件进行安装。如果搜索不到请注意是否做好了上一步？网络是否通畅？
插件会提示安装成功。
2. 下载安装：
点击[这个链接(v2.1.6)](https://plugins.zhile.io/files/ide-eval-resetter-2.1.6.zip)下载插件的zip包（macOS可能会自动解压，然后把zip包丢进回收站）
通常可以直接把zip包拖进IDE的窗口来进行插件的安装。如果无法拖动安装，你可以在Settings/Preferences... -> Plugins 里手动安装插件（Install Plugin From Disk...）
插件会提示安装成功。

### 0x2. 如何使用
一般来说，在IDE窗口切出去或切回来时（窗口失去/得到焦点）会触发事件，检测是否长时间（25天）没有重置，给通知让你选择。（初次安装因为无法获取上次重置时间，会直接给予提示）
也可以手动唤出插件的主界面：
如果IDE没有打开项目，在Welcome界面点击菜单：Get Help -> Eval Reset
如果IDE打开了项目，点击菜单：Help -> Eval Reset
唤出的插件主界面中包含了一些显示信息，2个按钮，1个勾选项：
按钮：Reload 用来刷新界面上的显示信息。
按钮：Reset 点击会询问是否重置试用信息并重启IDE。选择Yes则执行重置操作并重启IDE生效，选择No则什么也不做。（此为手动重置方式）
勾选项：Auto reset before per restart 如果勾选了，则自勾选后每次重启/退出IDE时会自动重置试用信息，你无需做额外的事情。（此为自动重置方式）
### 0x3. 如何更新
1. 插件更新机制（推荐）：
IDE会自行检测其自身和所安装插件的更新并给予提示。如果本插件有更新，你会收到提示看到更新日志，自行选择是否更新。
点击IDE的Check for Updates... 菜单手动检测IDE和所安装插件的更新。如果本插件有更新，你会收到提示看到更新日志，自行选择是否更新。
插件更新可能会需要重启IDE。
2. 手动更新：
从本页面下载最新的插件zip包安装更新。参考本文：下载安装小节。
插件更新需要重启IDE。
### 0x4. 一些说明
本插件默认不会显示其主界面，如果你需要，参考本文：如何使用小节。
市场付费插件的试用信息也会一并重置。
对于某些付费插件（如: Iedis 2, MinBatis）来说，你可能需要去取掉javaagent配置（如果有）后重启IDE：
如果IDE没有打开项目，在Welcome界面点击菜单：Configure -> Edit Custom VM Options... -> 移除 -javaagent: 开头的行。
如果IDE打开了项目，点击菜单：Help -> Edit Custom VM Options... -> 移除 -javaagent: 开头的行。
重置需要重启IDE生效！
重置后并不弹出Licenses对话框让你选择输入License或试用，这和之前的重置脚本/插件不同（省去这烦人的一步）。
如果长达25天不曾有任何重置动作，IDE会有通知询问你是否进行重置。
如果勾选：Auto reset before per restart ，重置是静默无感知的。
简单来说：勾选了Auto reset before per restart则无需再管，一劳永逸。
### 0x5. 开源信息
插件是学习研究项目，源代码是开放的。源码仓库地址：Gitee。
如果你有更好的想法，欢迎给我提Pull Request来共同研究完善。
插件源码使用：GPL-2.0开源协议发布。
插件使用PHP编写，毕竟PHP是世界上最好的编程语言！
### 0x6. 支持的产品
- IntelliJ IDEA
- AppCode
- CLion
- DataGrip
- GoLand
- PhpStorm
- PyCharm
- Rider
- RubyMine
- WebStorm

----

### 插件离线安装下载

- [ide-eval-resetter-2.1.6](https://github.com/superbeyone/JetBrainsActiveCode/raw/master/creak/Jetbrains%E7%B3%BB%E5%88%97%E4%BA%A7%E5%93%81%E9%87%8D%E7%BD%AE%E8%AF%95%E7%94%A8%E6%96%B9%E6%B3%95/ide-eval-resetter-2.1.6.zip)