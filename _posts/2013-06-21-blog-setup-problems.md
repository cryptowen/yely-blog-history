---
layout: post
title: "建站过程问题汇总"
description: ""
category: 技术
tags: [github, blog, jekyll, markdown]
---
{% include JB/setup %}

折腾了两天的博客，终于初具原型，过程中遇到了很多问题，在此进行汇总说明：

## 中文目录的支持问题

由于默认情况下jekyll搭建的网站是不支持中文目录的，而默认的post路径是：`地址/目录/日期/名字`，因此使用中文目录时生成网站会出现问题。

解决方案：

将`_config_yml`中的`permalink: /:categories/:year/:month/:day/:title`改为`permalink: /:year/:month/:day/:title`，即去掉路径中的目录，就可以支持中文目录了。


## 中文列表显示问题

在开始发布文章的时候，中文列表无法正常显示，后发现是默认markdown引擎不支持的原因，可以通过将默认的`maruku`引擎更换成github使用的引擎`rdiscount`解决

具体参考： [Markdown 中文列表抽风](http://yangzetian.github.io/2012/03/28/markdown/)
