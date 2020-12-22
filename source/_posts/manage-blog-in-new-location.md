---
layout: post
title: 在新位置管理blog
date: 2020-12-17 21:31:51
tags: [blog]
---


# 如何在新的位置部署hexo blog

远程仓库已经设置了hexo为默认分支，且放置了所有必须的文件，比如_config.yml, _config.next.yml, theme/, source/, scaffolds/, package.json, package-lock.json, .gitignore等其他静态文件

## 1. 准备基础环境

本地安装了node(v14.15.3), npm(6.14.9), hexo等, 版本最新最好。

## 2. 安装hexo blog本地依赖

```sh
# pull最新的代码
git clone https://github.com/username/username.github.io.git

cd "username.github.io"

# 安装 package.json中的依赖包
npm install

```
<!-- more -->

## 3. 编辑和创作正式blog

```sh

# 创建markdown文件 `new_blog.md`, 在source/_posts目录下
hexo new "new_blog"


## 编辑blog等工作
```

## 4. 编辑草稿和发布操作

当还没有编辑好正式文档时，可以使用草稿文档。

```sh

hexo new draft "draf"

# 从_draft目录移动到_post目录
hexo publish "draft"

```

## 5. 保存工作到hexo分支
```sh
git add .
git commit -m "info"
git push origin hexo
```


## 6. 本地预览及发布blog

```sh
# 将markdown文件生成html静态文件
hexo generate or hexo g

# 启动本地服务，地址为http://localhost:4000, 本地预览
hexo start

# 发布
hexo deploy or hexo d

# username.github.io可以查看新发布的文章
```







