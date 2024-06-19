# 环境配置

为了顺利进行导学阶段的实验，为之后正式学习的实验做好准备，需要先进行一些简单的环境配置。

我们推荐在 Linux 环境下完成实验，如果不在 Linux 环境下完成实验可能会遇到部分问题，具体可参考[第三章：如何在非 Linux 环境下完成实验](ch3/ch3-04.md)。

## 配置 Git

实验的最终成绩需要提交到远程 Gitee 仓库进行评测，你需要确保本地拥有 Git。

Ubuntu/Debian 发行版安装 Git：

```shell
sudo apt install git
```

Arch 发行版安装 Git：

```shell
sudo pacman -Syu git
```

Windows 下需要安装 Git for Windows，可从如下链接安装：

https://gitforwindows.org/

在完成 Git 的安装后需要对 Git 进行基本的配置：

```shell
git config --global user.name "你的 gitee 账户名/自定义"
git config --global user.email "你的 gitee 账户默认的邮箱地址/常用邮箱地址"
```



## 配置 C 工具链

导学阶段实验由5到基础的 C 语言语法题组成，为了完成实验以及在本地进行调试，需要配置 C 工具链。

Ubuntu/Debain 发行版配置：

```shell
sudo apt install build-essential gdb #安装 GNU 工具链与调试工具
```

Arch 发行版配置：

```shell
sudo pacman -S base-devel gdb 
```

Windows 需要安装 mingw 等编译工具链。

mingw 官网：https://www.mingw-w64.org/

在完成安装之后，可使用如下指令检测 gcc 是否被正确配置：

```shell
gcc --version
```



至此，导学阶段实验所需要的基本环境配置已完成，接下来，让我们正式进入导学阶段的学习。