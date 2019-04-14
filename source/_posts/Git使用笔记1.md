---
title: Git使用笔记１
tags: Git
---

#### Git 简介

Git是一种开源分布式版本控制系统(VCS)，也是Github的核心。Git 具有简单，快速，高效，可扩展性好等优点，所以Git也是目前最受欢迎的 VCS。([Git 简史](https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-Git-%E7%AE%80%E5%8F%B2))

Git提供了多种使用模式，桌面客户端或者是命令行模式，以方便用户进行项目版本管理，以及不同用户之间的协同项目处理。

命令行模式下，用户可以使用所有的命令操作实现 Git 全部功能，相较之下，GUI 模式只是 Git 简化版。

![Git workflow](Git使用笔记1/Git workflow.jpg)

Workspace：工作区  
Index / Stage：暂存区  
Repository：仓库区（或本地仓库)  
Remote：远程仓库

#### 初次安装与配置：

```
# 安装 Git
apt-get install git   # install git on ubuntu

# 设置 Git config 变量
git config --global user.name "xxx"               # 设置 user name 以及 email
git config --global user.email xxx@email.com

# 查看 Git config 信息
git config --list
```
#### 获取仓库 (Repository)：
使用 Git 对项目或者文件进行版本管理时，需要先配置初始化仓库－－repository 以存储各种项目文件．通常有两种方式:

１. 直接从本地文件夹建立repository  
```
git init    # 会在当前文件夹生成　,git文件夹，其中包含了 repository 初始化文件
git add .
git add LICENSE
git commit -m "init project version"
```
２. Clone 已有 repository  
```
git clone  https://github.com/repository
```
