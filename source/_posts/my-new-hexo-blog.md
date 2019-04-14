---
title: My New Hexo Blog
tags: Hexo
---

#### 搭建教程：

[macOS环境下利用Github和Hexo部署博客](https://www.jianshu.com/p/1519f22aff24)

[GitHub+Hexo 搭建个人网站详细教程](https://zhuanlan.zhihu.com/p/26625249)

#### Themes:

github 源码: [Hexo-Aircloud-Blog](https://github.com/aircloud/hexo-aircloud-blog)

preview 博客：[niexiaotao.cn](http://niexiaotao.cn/)

#### 主要问题：

使用hexo new page时，生成的md文件中默认有date，会造成hexo generate无法构建新的静态页面。因此，可能会出现部署新的layout页面出现404 not found，以及新post不显示。

#### Hexo Blog使用：

[Hexo 常用命令](https://segmentfault.com/a/1190000002632530)

[Markdown语法](https://www.jianshu.com/p/191d1e21f7ed)

换机更新博客[方法](https://www.zhihu.com/question/21193762/answer/79109280)
主要思路还是将本地Hexo原始文件以及生成的网页静态文件分别放在 github 不同的分支，其中 Hexo 分支设为默认分支。换机更新博客时，首先安装好本地 git 环境，安装nodejs, npm, Hexo，再 git clone Hexo repo至本地。本地更新博客时，先更新上传 Hexo 源文件，再生成网页 static 文件并部署至 github pages (另一分支)。

```
# 将旧机器上博客源文件　git push 至新建的 hexo 分支(github pages repository)

# 新机器上，先 clone 博客源文件至 local
git clone git@github.com:xx/xx.github.io.git

# 安装 nodejs, npm, Hexo
sudo apt-get install nodejs
sudo apt-get install npm
npm install hexo-cli -g

# 上传博客修改的博客源文件
git add .
git commit -m "update blog"
git push

# 生成静态网页文件，并部署至github pages
hexo c
hexo g
hexo d
```



#### 其他比较好看的themes：

Next: [Dandy Xu's Pit](https://dandyxu.me/)（[github](https://github.com/dandyxu/dandyxu.github.io)）

Maupassant: [屠城](https://www.haomwei.com/)（[github](https://github.com/tufu9441/maupassant-hexo)）

TKL: [Kieran's Blog](https://go.kieran.top/)（[github](https://github.com/SuperKieran/TKL)）

Anisina: [Haojen's Blog](http://haojen.github.io/)（[github](https://github.com/Haojen/hexo-theme-Anisina)）

Pure: [Cofess](https://blog.cofess.com/)（[github](https://github.com/cofess/hexo-theme-pure)）

PolarBear: [Frost](https://d2fan.com/)（[github](https://github.com/frostfan/hexo-theme-polarbear)）

....

之前一直在用WordPress，不过并不是很喜欢，所以一直在想自己搭一个blog。虽然心心念念，但拖了很久。对于本人这种选择困难症来说，选theme真是一件痛苦的事情。因为比较喜欢偏简洁一点的风格，所以最后选了这个巨简风aircloud。
