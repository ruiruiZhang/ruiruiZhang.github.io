---
layout: post
author: zhangrui
title: 博客一
category: 技术博文
tag: [aaa]
---
使用jekyll+github搭建博客时遇到的问题

#####1.编辑好文章后调用jekyll serve命令后出现以下错误：
```jekyll 2.5.2 | Error:  undefined method `default_proc=' for "layout:post title:hello world!":String```
	
谷歌之后发现问题出现在博文头信息中：
```
---
layout:post
title:hello world!
---
# test Title   
hello,world!this is a test file write by sublime 	text2 with markdown gramar.
```

在冒号后边需要空一格。所以正确的格式如下：

```
---
layout: post
title: hello world!
---
# test Title   
hello,world!this is a test file write by sublime 	text2 with markdown gramar.
```