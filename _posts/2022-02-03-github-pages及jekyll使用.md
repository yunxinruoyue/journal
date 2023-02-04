---
title: github-pages 及 jekyll 的使用
author: yunyue
date: 2023-02-03 15:00:00 +0800
categories: [github, jekyll]
tags: [github]     # TAG names should always be lowercase
img_path: /assets/img/posts/01
---
## jekyll安装

### 获取安装信息

查看jekyll官网。得知其安装依赖为ruby、rubyGem、gcc。

![jekyllDependencies](jekyllRequiredDependencies.png){: width="600" height="400" .shadow}

### ruby安装

在搜索引擎中键入关键字ruby并在结果中寻找ruby官网。中国区地址为http://www.ruby-lang.org/zh_cn/。点击下载进入安装页面，了解安装过程后进行环境安装。本人使用的是windows installer。该安装包自动安装gem包管理工具及gcc编译器。具体过程如下所示：

![search](searchRubyWebsite.png){: width="600" height="400" .shadow}


![download](rubyDownload.png){: width="600" height="400" .shadow }

### jekyll安装

* 使用gem命令安装jekyll

```ruby
    gem install jekyll

```

## github-pages 使用

进入github官网help页面，查看github-pages使用教程。

![githubHelp](github-pagesHelp.png){: width="600" height="400" .shadow }

### 创建代码库

* 首先，创建用于github-pgaes的代码库。

![githubHelp](create-repository.png){: width="600" height="400" .shadow }

* 打开settings，点击pages标签进行相应配置。整个流程如下

![githubHelp](pages-settings.png){: width="600" height="400" .shadow }

### 创建站点
这里本人使用的是jekyll。使用ruby开发的静态博客生成器。

* 创建文件夹并使用jekyll命令生成本地站点

```ruby

    mkdir xxx //创建文件夹
    cd xxx //进入文件夹
    jekyll new --skip-bundle //创建jekyll站点

```

* 编辑_config.yml文件进行站点配置

### 提交可公开内容到代码库

1. 编辑自己想公开展示的内容如博客文章、样式等。然后push到github远程代码库中。 

2. 将编辑好的内容push到创建好的库中。当push完成时会自动触发构建和发布。

3. 打开浏览器输入your_github_name.github.io（若无配置project_name）

## 注意事项

* 如果使用样式不在官方支持列表中时，使用remote_theme代替theme。值为你使用的主题的github库作者账户名+主题名如：

![githubHelp](remoteTheme.png){: width="600" height="400" .shadow }
