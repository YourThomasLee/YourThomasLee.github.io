## 备忘录





## hexo usage

1. hexo的安装

```bash
# 1. 安装node.js
> wget https://nodejs.org/dist/v16.14.2/node-v16.14.2.pkg #node.js
# 2. 安装git
> wget https://git-scm.com/download/mac
# 检查
> node -v & npm -v & git --version
# 设置好github账户
#3. 安装好hexo
> sudo npm install -g hexo-cli
#4. 到指定空的文件夹, 初始化目录
> hexo init
> npm install
# - _config.yml 网站的配置信息;
# - package.json 应用程序的信息
# - scaffolds 模板文件夹
# - source 存放用户资源(_drafts, _posts)
# - themes 主题文件夹
# - public 网站文件
#5. 安装github的部署
> npm install hexo-deployer-git --save --registry https://registry.npm.taobao.org 
#修改_config.yml的配置
# deploy: 
#		type: git
#		repository: git@github.com:用户名/用户名.github.io.git
#		branch: master
#将网站上传部署到github pages
> hexo d
```

2. 依赖包记录

```bash
# markdown 图片
> npm install hexo-renderer-marked --save
```



2. hexo的使用

- 更换主题

```bash
# 下载主题到指定目录
git clone https://github.com/iissnan/hexo-theme-next themes/next
# 修改_config.yml
```



- 编写新的文章

```bash
# 使用hexo生成页面
#		1. 进入博客所在目录
> hexo new "new post"
#		2. 进入source文件夹编写"new post.md"文件
> hexo g #生成页面
> hexo d #部署页面
# 自己生成页面, 文件开头加入如下格式即可
---
title: Hello World # 标题
date: 2019/3/26 hh:mm:ss # 时间
categories: # 分类
- Diary
tags: # 标签
- PS3
- Games
---

摘要
<!--more-->
正文"""
```

- 常用命令

```bash
hexo new "name"       # 新建文章
hexo new page "name"  # 新建页面
hexo g                # 生成页面
hexo d                # 部署
hexo g -d             # 生成页面并部署
hexo s                # 本地预览
hexo clean            # 清除缓存和已生成的静态文件
hexo help             # 帮助
```



