---
title: 使用Hexo+pure主题创建个人博客
date: 2019-05-06 21:12:58
tags:
  - Hexo
---

## Clone

``` cmd
cd "D:\Projects\Blog"
git clone git@github.com:GerryGe/gerryge.github.io.git gerryge
cd gerryge
git branch -a  列出所有远程分支


$ git checkout -b dev origin/dev
Switched to a new branch 'dev'
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
git checkout master 切换到master分支
```

## 接下来是在gerryge目录还原包

``` cmd
npm install

hexo clean
hexo g
hexo d
hexo s
```

## Creates a new article

```cmd
hexo new [layout] <title>
```

Creates a new article.  If the title contains spaces, surround it with quotation marks.

## git提交代码

```cmd
git add .
git status
git commit -m "add beian info"
git push origin dev
```

## 发布文章

```cmd
hexo deploy
```
执行这个命令会直接上传到_config.yml配置文件中配置的github仓库中

> #### Docs: https://hexo.io/docs/commands#deploy
> deploy:
>  type: git
>  repo: https://github.com/GerryGe/gerryge.github.io.git
>  branch: master