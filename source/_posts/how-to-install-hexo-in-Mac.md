---
title: how_to_install_hexo_in_Mac
date: 2018-11-09 22:59:59
tags:
---
# Mac环境下安装Hexo的步骤
## 前提：安装了xcode
 
1.	Nvm 安装：
```
$ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```
2.	Git 安装：
```
 brew install git
```
	
3.	Node.js安装：
```
nvm install stable
```
4.	Hexo安装
```
npm install -g hexo-cli
```



***
安装的过程遇到：No Xcode or CLT version detected!
解决办法：sudo xcode-select --install

***
到此环境安装好了。接下来，我们开始建app
```
hexo init <dir>
```

