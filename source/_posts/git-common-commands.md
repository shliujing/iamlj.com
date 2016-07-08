---
title: Git常用命令
categories: Tech
tags: [Git,Command]
date: 2016-07-08 08:51:54
---

## 常用操作

Git的通用操作，可以在本地做好版本控制后，push到`Git的服务器`,可以是`Github`、`Gitlab`

### Create a new repository on the command line

``` git
git init 
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/yourId/repoName.git
git push -u origin master
``` 

### Push an existing repository from the command line

``` git
git remote add origin https://github.com/yourID/repoName.git
git push -u origin master
``` 

<!--more--> 
