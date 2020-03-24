---
layout: category
title: 搭建jeklly网站的经验总结
excerpt_separator: "<!--more-->"
date: 2019-07-03
categories: 
  - 学习笔记
image: /assets/images/学习笔记.jpg
---
此文章是在搭建jeklly时遇到的问题以及解决方案。
<!--more-->
### 写的文章无法链入网页，是什么原因呢？
当我们在`_post`里面写的文章无法链入网页时，我们需要检查一下我们的`layout、title、categories`
```
layout: category
title: 搭建jeklly网站的经验总结
excerpt_separator: "<!--more-->"
date: 2019-07-03
categories: 
  - 学习笔记
```
当你检查完上面的内容都无错误出现时，我们就得检查一下`_post`里面的文章命名。
因为Jekyll对于文章的文件名是有要求的，系统会根据文件名来生成每篇文章的链接地址。具体的格式为：``YYYY-MM-DD-文章标题.md``,其中YYYY为4位年份，MM是两位的月份，DD是两位的日期。

### 如果网页部署完呈现404，应该怎么办呢？
当部署完的页面出现404，你就得检查在部署前的操作步骤，是否忘记加空格，是否没有用英文的标点符号。

### 部署失败，应该怎么办？
记得检查分支，以及是否忘记加空格。我之前在`_config.yml`修改了name之后，就出现了部署失败的界面，于是我在填入的信息前加了空格，就部署成功了。

### 如何修改fork的jeklly域名呢？
* 打开gitee的管理，会出现以下内容。
<img src="/assets/images/yuming.png" alt="yuming" width="600px" height="550px">

我们需要修改仓库名称以及路径，把它改成自己的gitee名称。
* 修改`_congfig.yml`的baseulr和url，把它换成自己的jeklly名字以及url。
* 重新部署。

### 搭建jeklly网站的图片，应该放在哪呢？
搭建jeklly用到的图片，我们应该放在`assets`里面，再新建一个`images`文件夹，里面放我们的图片。

### 当要链入照片的url时，照片无法显示怎么办？
当我们选择以相对路径链入图片而图片无法显示时，我们要检查我们的url，我之前错误输入的url为`assets/images/xxx.jpg`,正确的url应为`/assets/images/xxx.jpg`。