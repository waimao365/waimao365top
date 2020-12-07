# Hugo文章格式和固定链接

## hexo文章格式
```
---
title: 文章标题
date: 2020-11-23 22:33:32
categories:
  - hugo
  - 分类
  - 博客
tags:
  - hugo
  - 标签
  - 博客
abbrlink: 25
slug: 25
---
```


## hugo文章格式
```
---
title: "文章标题"
date: 2020-11-23T22:33:32+08:00
categories: ["category","category2","category3"]
tags: ["tag","tag2","tag3"]
abbrlink: 25
slug: 25
---
```

##  hexo和hugo统一固定链接，方便互转
显示链接如下
https://163168.xyz/posts/25.html/

在文章头部加入

abbrlink: 25是指hexo的固定链接

slug: 25是指hugo的固定链接

###  hugo主题even在站点配置文件里适当的位置加上下面的代码

```
---
[permalinks]
  posts = "/posts/:slug.html"
---
```
### hugo主题LoveIt 搜索Permalinks 改成下面这样就可以了
```
---
[Permalinks]
  # posts = ":year/:month/:filename"
   posts = "/posts/:slug.html"
---
```
###  hexo固定链接

查找 

permalink: :year/:month/:day/:title/

修改成

permalink: archives/:abbrlink.html 

写文章加上 abbrlink: 1（数字越大的，就是越新的文章）

### 我这种固定链接文章合适好像是通用的，没有改任何头部文件，暂时没有发现什么问题
