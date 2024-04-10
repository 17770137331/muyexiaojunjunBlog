---
title: node版本管理工具nvm
date: 2024-04-09 17:47:00
tags:
  - 技术
updated: 2024-04-09 18:51:56
categories:
  - 技术
excerpt: nvm全英文也叫node.js version management，是一个nodejs的版本管理工具。nvm和n都是node.js版本管理工具，为了解决node.js各种版本存在不兼容现象可以通过它可以安装和切换不同版本的node.js
cover: https://gongjv.jun-ye.top/myblog/image/default.webp
---
nvm是什么

nvm全英文也叫node.js version management，是一个nodejs的版本管理工具。nvm和n都是node.js版本管理工具，为了解决node.js各种版本存在不兼容现象可以通过它可以安装和切换不同版本的node.js。

nvm下载

可在点此在[github](https://github.com/coreybutler/nvm-windows/releases)上下载最新版本,本次下载安装的是windows版本。目前最新版本v1.1.12,更新日期：2023-11-23。

下载链接v1.1.12：[nvm 1.1.12-setup.zip](https://nvm.uihtm.com/nvm-1.1.12-setup.zip)

下载链接v1.1.11：[nvm 1.1.11-setup.zip](https://nvm.uihtm.com/nvm-1.1.11-setup.zip)

下载链接v1.1.10：[nvm 1.1.10-setup.zip](https://nvm.uihtm.com/nvm-1.1.10-setup.zip)

<!-- 网盘链接：[nvm 1.1.10-setup.zip](https://pan.baidu.com/s/12E7d46XLVxGOmTDevVB58g?pwd=ntfm) -->

nvm安装

1. **卸载之前的node后安装nvm**, nvm-setup.exe安装版，直接运行nvm-setup.exe

![step1.png](https://gongjv.jun-ye.top/myblog/image/nvm.001.png)

2.选择nvm安装路径

![step2.png](https://gongjv.jun-ye.top/myblog/image/nvm.002.png)

3.选择nodejs路径

![step3.png](https://gongjv.jun-ye.top/myblog/image/nvm.003.png)

4.确认安装即可

![step4.png](https://gongjv.jun-ye.top/myblog/image/nvm.004.png)

5.安装完确认

![step5.png](https://gongjv.jun-ye.top/myblog/image/nvm.005.png)

打开CMD，输入命令 nvm ，安装成功则如下显示。可以看到里面列出了各种命令，本节最后会列出这些命令的中文示意。

nvm命令提示

nvm arch：显示node是运行在32位还是64位。

nvm install <version> [arch] ：安装node， version是特定版本也可以是最新稳定版本latest。可选参数arch指定安装32位还是64位版本，默认是系统位数。可以添加--insecure绕过远程服务器的SSL。

nvm list [available] ：显示已安装的列表。可选参数available，显示可安装的所有版本。list可简化为ls。

nvm on ：开启node.js版本管理。

nvm off ：关闭node.js版本管理。

nvm proxy [url] ：设置下载代理。不加可选参数url，显示当前代理。将url设置为none则移除代理。

nvm node\_mirror [url] ：设置node镜像。默认是https://nodejs.org/dist/。如果不写url，则使用默认url。设置后可至安装目录settings.txt文件查看，也可直接在该文件操作。

nvm npm\_mirror [url] ：设置npm镜像。https://github.com/npm/cli/archive/。如果不写url，则使用默认url。设置后可至安装目录settings.txt文件查看，也可直接在该文件操作。

nvm uninstall <version> ：卸载指定版本node。

nvm use [version] [arch] ：使用制定版本node。可指定32/64位。

nvm root [path] ：设置存储不同版本node的目录。如果未设置，默认使用当前目录。

nvm version ：显示nvm版本。version可简化为v。

安装node.js版本

nvm list available 显示可下载版本的部分列表

![st-available.png](https://gongjv.jun-ye.top/myblog/image/nvm.006.jpeg)

nvm install latest安装最新版本 ( 安装时可以在上面看到 node.js 、 npm 相应的版本号 ，不建议安装最新版本)

![stall-latest.png](https://gongjv.jun-ye.top/myblog/image/nvm.007.png)

nvm install 版本号 安装指定的版本的nodejs

![install-node.png](https://gongjv.jun-ye.top/myblog/image/nvm.008.png)

查看已安装版本

nvm list或nvm ls查看目前已经安装的版本 （ 当前版本号前面没有 \* ， 此时还没有使用任何一个版本，这时使用 node.js 时会报错 ）

![nvm-list1.png](https://gongjv.jun-ye.top/myblog/image/nvm.009.png)

![nvm-list2.png](https://gongjv.jun-ye.top/myblog/image/nvm.010.png)

切换node版本

nvm use版本号 使用指定版本的nodejs （ 这时会发现在启用的 node 版本前面有 \* 标记，这时就可以使用 node.js ）

![nvm-use.png](https://gongjv.jun-ye.top/myblog/image/nvm.011.png)

nvm切换国内镜像

如果下载node过慢或者安装失败，请更换国内镜像源, 在 nvm 的安装路径下，找到 settings.txt，设置node\_mirro与npm\_mirror为国内镜像地址。下载就飞快了~~

root: D:\nvm

path: D:\nodejs

nvm npm\_mirror https://npmmirror.com/mirrors/npm/

nvm node\_mirror https://npmmirror.com/mirrors/node/

或者：

node\_mirror: https://npm.taobao.org/mirrors/node/

npm\_mirror: https://npm.taobao.org/mirrors/npm/

命令行切换(注意：请切换国内镜像后再安装node版本，否则会很慢)

阿里云镜像

nvm npm\_mirror https://npmmirror.com/mirrors/npm/ nvm node\_mirror https://npmmirror.com/mirrors/node/

腾讯云镜像

nvm npm\_mirror http://mirrors.cloud.tencent.com/npm/ nvm node\_mirror http://mirrors.cloud.tencent.com/nodejs-release/

打开链接查看可以node版本：https://registry.npmmirror.com/binary.html?path=node/

NVM For Linux

下载压缩包

cd / wget https://github.com/nvm-sh/nvm/archive/refs/tags/v0.39.1.tar.gz

解压

mkdir -p /.nvm tar -zxvf nvm-0.39.0.tar.gz -C /.nvm

配置环境

vim ~/.bashrc

在~/.bashrc的末尾，添加如下语句：

export NVM\_DIR="$HOME/.nvm/nvm-0.38.0" [ -s "$NVM\_DIR/nvm.sh" ] && \. "$NVM\_DIR/nvm.sh"  # This loads nvm [ -s "$NVM\_DIR/bash\_completion" ] && \. "$NVM\_DIR/bash\_completion"  # This loads nvm bash\_completion

使能配置

source ~/.bashrc

使用NVM安装node v8.16.0

nvm install 8.16.0

切换node版本

nvm use 14.17.3

在 Mac 下安装 nvm 管理 node

在使用 node 的过程中，用 npm 安装一些模块，特别是全局包的时候，由于 Mac 系统安全性的限制，经常出现安装没有权限，或者安装完成使用时出现 Command not found 的情况。

之前我都是通过使用修改权限的方式来解决，但是太麻烦又感觉不太安全，于是我就到网上找解决的方法，发现其实官方也是推荐我们使用 node 的管理工具来解决这个问题的。官方推荐了两个 n 和 nvm，这里我选择的是 nvm。

至于两者的区别可以看一下淘宝团队的一篇文章[管理node版本，选择nvm还是n？](https://fed.taobao.org/blog/taofed/do71ct/nvm-or-n/?spm=taofed.homepage.header.7.7eab5ac8dDRkRS)

Mac 安装

在 Mac 下 nvm 的安装和遇到的问题。

注意：不要使用 Homebrew 安装 nvm，这个在 nvm 的官方文档中有说明。

具体的步骤如下：首先打开终端，进入当前用户的 home 目录中。

` `cd ~

然后使用 ls -a 显示这个目录下的所有文件（夹）（包含隐藏文件及文件夹），查看有没有 .bash\_profile 这个文件。

ls -a

如果没有，则新建一个。

touch ~/.bash\_profile

如果有或者新建完成后，我们通过官方的说明在终端中运行下面命令中的一种进行安装：

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

在安装完成后，也许你会在终端输入 nvm 验证有没有安装成功，这个时候你会发现终端打出 Command not found，其实这并不是没有安装成功，你只需要重启终端就行，再输入 nvm 就会出现 Node Version Manager 帮助文档，这表明你安装成功了。

注意

这里需要注意的几点就是：

第一点 不要使用 homebrew 安装 nvm

第二点 关于 .bash\_profile 文件。如果用户 home 目录下没有则新建一个就可以了，不需要将下面的两段代码写进去，因为你在执行安装命令的时候，系统会自动将这两句话写入 .bash\_profile 文件中。

export NVM\_DIR="$HOME/.nvm" [ -s "$NVM\_DIR/nvm.sh" ] && \. "$NVM\_DIR/nvm.sh"  # This loads nvm [ -s "$NVM\_DIR/bash\_completion" ] && \. "$NVM\_DIR/bash\_completion"  # This loads nvm bash\_completion

网络上我找了好多文章都是说在安装前先手动将下面这两句话写进去，经过测试是不正确的，并且会造成安装不成功，这一点需要注意一下。

export NVM\_DIR="${XDG\_CONFIG\_HOME/:-$HOME/.}nvm" [ -s "$NVM\_DIR/nvm.sh" ] && \. "$NVM\_DIR/nvm.sh"

第三点 保证 Mac 中安装了 git，一般只要你下载了 Mac 的 Xcode 开发工具，它是自带 git 的。
