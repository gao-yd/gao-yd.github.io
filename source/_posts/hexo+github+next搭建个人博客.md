---
title: github+hexo搭建个人博客总结篇
categories: 博客教程
tags:
	- 博客教程
	- hexo
	- next
---

> github+hexo搭建个人博客网上的教程已经很多了，但是本小白自己动手搭建时候还是遇到了一些问题，所以综合了网上其他大神的文章写了这一篇总结教程。

<!--more-->

## 前期准备

此教程需要具备一下基础知识：

- git与github
- markdown相关语法
- npm

1.下载并安装node.js   //具体过程就不再详细描述，网上教程很多
2.安装git
3.准备一个文本编辑器，最好支持markdown语法。	//个人比较推荐sublime
4.注册一个github账号
5.新建一个文件夹，我们将在这个文件夹下进行本地搭建。 

## 开始搭建

首先声明的我的配置环境是windows10.

#### 使用npm安装所需要的插件

1.打开命令行，并切换到刚刚新建的文件夹下,输入命令`npm init`。
2.输入`npm install hexo --save`。	//安装hexo
3.输入`npm install hexo-deployer-git --save`。	//安装hexo自带的代码提交插件

#### 初始化博客

1.输入`hexo init`	//初始化博客，生成博客目录
2.输入`hexo generate`	//生成静态html文件
3.输入`hexo server`		//启动本地博客预览服务，默认端口4000

以上命令按照循序输入，并且正常执行完成之后，打开浏览器，输入`localhost:4000`应该就能预览你的博客了。至于报错的，请自行百度。

#### 修改博客配置文件，测试并关联github仓库

1.新建一个github仓储
	建立仓储的命名规则：`[你的github账户名].github.io`
	例如我的就是`gao-yd.github.io`

2.修改博客的配置文件，其实主要也就是修改根目录下的`_config.yml`文件.

在博客根目录找到`_config.yml`文件，使用编辑器打开。
当前需要修改的主要是两个部分
第一个是`site`下的，也就站点信息。如下：

```
	# Site
	title: MX Blog    #博客标题
	subtitle:         #博客的副标题
	description:      #博客描述
	author: mx        #作者
	language: zh-Hans #语言
	timezone:         #时区

```
**修改注意事项：字段的冒号后面一定要有一个空格！！**

第二个是修改`Deployment`配置。
找到`#Deployment`一般是在配置文件的最后，修改其中的`deploy`。如下：

```
	deploy:
	    type: git
	    repo: https://github.com/gao-yd/gao-yd.github.io.git      #这个写刚刚新建的那个仓储的提交路径
	    branch: master

```

3.测试本地环境
	
在命令行窗口依次输入以下命令

	- hexo clean	//清楚历史生成的静态资源（也就是public文件夹）
	- hexo g		//hexo generate的简写，生成静态页面至public目录
	- hexo s 		//hexo server的简写，开启预览访问端口（默认端口4000，'ctrl + c'关闭server）

然后一些正常的情况下就能在`localhost:4000`的地址看到你修改过的博客了

4.关联github仓储，提交博客的静态html文件到github.


#### 一些常用命令：

- hexo new"postName" 	//新建文章

- hexo new page"pageName" 	//新建页面

- hexo generate 	//生成静态页面至public目录

- hexo server 	//开启预览访问端口（默认端口4000，'ctrl + c'关闭server）

- hexo deploy 	//将.deploy目录部署到GitHub

- hexo help 	//查看帮助

- hexo version 	//查看Hexo的版本

## next主题的安装与配置

## 添加常用功能

## 正在更新，稍安勿躁。