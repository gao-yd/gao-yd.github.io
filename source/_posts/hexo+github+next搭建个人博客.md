---
title: github+hexo搭建个人博客总结篇
categories: 博客教程
tags:
	- 博客教程
	- hexo
	- next
---

github+hexo搭建个人博客网上的教程已经很多了，但是本小白自己动手搭建时候还是遇到了一些问题，所以综合了网上其他大神的文章写了这一篇总结教程。

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

#### 修改博客配置文件，关联github仓库

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