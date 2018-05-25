---
title: 使用hexo建立信息发布平台
tags: ['文档']
date: 2018-04-11
---

[Hexo](https://hexo.io/zh-cn/)是一个快速、简洁且高效的博客框架，基于Node.js，适合用于维护静态内容的网站，并且集成了本地调试服务器、Github Page发布等功能，推荐用于维护项目课题的主页。

<!--more-->

相关文档的链接：
* [Git](http://git-scm.com/book/zh/v2)
* [GitHub](https://github.com/)
* [GitHub Pages](https://pages.github.com/)
* [Hexo](https://hexo.io/zh-cn/)
* [Markdown](http://www.appinn.com/markdown/#autoescape)

## GitHub Pages 仓库

在GitHub账号下创建一个新的仓库，命名为username.github.io（username 为 Github 账号，例如本项目的账号为`growinware-nju`)。

GitHub Pages有两种类型：User/Organization Pages 和 Project Pages，而这里使用的是 User/Organization Pages。

简单来说，User Pages 与 Project Pages的区别是：
1. User Pages 是用来展示用户的，而 Project Pages 是用来展示项目的。
2. 用于存放 User Pages 的仓库必须使用username.github.io的命名规则，而 Project Pages 则没有特殊的要求。
3. User Pages 将使用仓库的 master 分支，而 Project Pages 将使用 gh-pages 分支。
4. User Pages 通过 http(s)://username.github.io  进行访问，而 Projects Pages通过 http(s)://username.github.io/projectname 进行访问。

因此，这里使用 User/Organization Pages 的主要目的是得到一个能够直接访问的域名(`https://growinware-nju.github.io`)。

[GitHub Pages Basics / User, Organization, and Project Pages](https://help.github.com/articles/user-organization-and-project-pages/)。

## 安装与配置Git

相关文档：

* [安装 Git](http://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git)
* [配置 Git](http://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%88%9D%E6%AC%A1%E8%BF%90%E8%A1%8C-Git-%E5%89%8D%E7%9A%84%E9%85%8D%E7%BD%AE)

注意在安装完Git后，必须设置用户名和电子邮件才能进行`commit`：

```bash
$ git config --global user.name "你的用户名"
$ git config --global user.email "你的邮件地址"
```

## 使用 Hexo

### 安装

在安装 Hexo 之前，首先确保已经安装 Node.js 和 Git，然后只需在命令行中使用`npm`安装 Hexo 即可：
```bash
$ npm install -g hexo-cli
```

### 建立网站

在任意目录中，输入

```bash
$ hexo init
$ npm install
```

则会自动完成网站的建立。建立完网站后可以使用`hexo server`(或简写为`hexo s`)启动本地的调试服务器，更多内容请参考 [Hexo 官方文档](https://hexo.io/zh-cn/docs/)

### 关联Github Page

为了能够使Hexo部署到GitHub上，需要安装一个插件：

```bash
$ npm install hexo-deployer-git --save
```

然后，**我们建立的是 User/Organization Github Page**，根据 Github Pages 的约定，在`master`分支存放博客的实际内容，在另一个(任意)的分支中存放源代码。我们不妨将源代码保存在`hexo`分支中 (源代码的保存非常重要，用于实现信息聚合)，修改`_config.yml`中的部署配置：

修改后的_config.yml：
```bash
deploy:
  type: git
  repo: 对应的Github仓库地址
  branch: 分支 (因为我们建立User/Organization Page，因此目标分支是master，如果是项目的Github Page，则是gh-pages)。
```

然后，执行下列指令即可完成部署：

```bash
$ hexo clean
$ hexo generate
$ hexo deploy
```

如果一切配置正常，稍等片刻github.io就能完成更新了(自动生成内容并上传到master分支)。同时也不要忘记将源代码提交到Github的远程仓库中。

更多的文档请参考[Hexo官网](https://hexo.io/zh-cn/)。