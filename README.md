[![Build Status](https://travis-ci.org/nesbox/TIC-80.svg?branch=master)](https://travis-ci.org/nesbox/TIC-80)
[![Build status](https://ci.appveyor.com/api/projects/status/1pflw77cjd8mqggb/branch/master?svg=true)](https://ci.appveyor.com/project/nesbox/tic-80)

![TIC-80](https://tic.computer/img/logo64.png)
**TIC-80微型电脑** - [https://tic.computer/](https://tic.computer/)

# 关于
TIC-80是一个**免费开源**的梦幻电脑，用来制作，运行以及分享小游戏。

使用TIC-80，您可以获得用于开发的内置工具：包括代码，精灵，地图，音效编辑器和命令行，这足以创建迷你复古游戏。

游戏被打包成一个卡带文件，可以很容易地分发。TIC-80适用于所有流行的平台。这意味着你的卡带可以在任何设备上运行。

为了制作复古风格的游戏，创作和运行的整个过程将在一些技术限制下进行：240x136像素显示，16色调色板，256种8x8色彩精灵，4声道音乐等。

![TIC-80](https://user-images.githubusercontent.com/1101448/29687467-3ddc432e-8925-11e7-8156-5cec3700cc04.gif)

### 特性
- 支持多种编程语言: [Lua](https://www.lua.org),
  [Moonscript](https://moonscript.org),
  [Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript),
  [Wren](http://wren.io/)，以及 [Fennel](https://fennel-lang.org).
- 可以使用键盘和鼠标作为输入
- 游戏最多可以有4个控制器作为输入（每个控制器有8个按钮）
- 内置编辑器：用于代码、精灵、世界地图、音效和音乐
- 一个额外的存储区域：可以在游戏运行时从你的卡带中加载不同的资源

# 二进制下载
你可以直接从我们的[发布页](https://github.com/nesbox/TIC-80/releases)上下载主流操作系统的编译版本。

# 高级版
为了支持TIC-80的开发，我们提供了[高级版](https://nesbox.itch.io/tic)。这个版本有一些额外的特性，它的二进制文件只能在我们的[Itch.io](https://nesbox.itch.io/tic)页面上下载

对于那些不能花钱的用户，我们做了一些工作，使得从源代码编译高级版十分容易。

### 高级版特性

- 以文本格式保存\加载卡带, 在您想要的任何编辑器中编写游戏，对版本控制系统也很有用。
- 更多的存储区域: 不仅仅是1个，而是8个。
- 导出不带编辑器的游戏，然后发布到应用商店（待实现）

# 社区
你可以在[tic.computer](https://tic.computer/play)里运行并分享游戏，工具以及音乐。

社区也经常在[Discord chat](https://discord.gg/DkD73dP)上闲聊。

# 贡献
你可以通过在我们的[issues page](https://github.com/nesbox/tic.computer/issues)上提出bug或请求一个新特性来做出贡献。进行讨论时，请牢记我们的[行为准则](https://github.com/nesbox/TIC-80/blob/master/CODE_OF_CONDUCT.md)。

你也可以通过审阅或改进我们的[wiki](https://github.com/nesbox/tic.computer/wiki)来做出贡献。[wiki](https://github.com/nesbox/tic.computer/wiki)包含了TIC-80的文档，代码片段和游戏开发教程。

# 构建说明

## Windows
### Visual Studio 2017
- 安装 `Visual Studio 2017`
- 安装 `git`
- 在`cmd`中运行以下指令
```
git clone --recursive https://github.com/nesbox/TIC-80
cmake -G "Visual Studio 15 2017 Win64"
```
- 打开 `TIC-80.sln` 然后构建
- 完成！ :)

### MinGW
- 安装 `mingw-w64` (http://mingw-w64.org)然后添加 `.../mingw/bin`路径至*系统变量路径*
- 安装 `git`
- 安装 `cmake` (https://cmake.org)
- 在`terminal`中运行以下指令
```
git clone --recursive https://github.com/nesbox/TIC-80
cd TIC-80
cmake -G "MinGW Makefiles"
mingw32-make -j4
```

## Linux 
### Ubuntu 14.04
在控制台中运行以下指令
```
sudo apt-get install git cmake libgtk-3-dev libgles1-mesa-dev libglu-dev -y
git clone --recursive https://github.com/nesbox/TIC-80 && cd TIC-80
cmake . && make -j4
```

安装最新版本的cmake：
```
wget "https://cmake.org/files/v3.12/cmake-3.12.0-Linux-x86_64.sh"
sudo sh cmake-3.12.0-Linux-x86_64.sh --skip-license --prefix=/usr
```

### Ubuntu 18.04

在控制台中运行以下指令
```
sudo apt-get install git cmake libgtk-3-dev libglvnd-dev libglu1-mesa-dev freeglut3-dev -y
git clone --recursive https://github.com/nesbox/TIC-80 && cd TIC-80
cmake . && make -j4
```

## Mac
安装 `Command Line Tools for Xcode` 和 `brew` 包管理器

在控制台中运行以下指令
```
brew install git cmake
git clone --recursive https://github.com/nesbox/TIC-80
cd TIC-80
cmake . && make -j4
```

## iOS / tvOS
你可以在这里找到ios/tvOS的版本
- 0.60.3: https://github.com/brunophilipe/TIC-80
- 0.45.0: https://github.com/CliffsDover/TIC-80
