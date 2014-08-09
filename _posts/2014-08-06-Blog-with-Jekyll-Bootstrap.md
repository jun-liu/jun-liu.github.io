---
layout: post
title: "一个神奇的网站"
description: "使用Jekyll Bootstrap构建个人主页"
category: tech
tags: [Jekyll Bootstrap, GitHub Pages]
---
{% include JB/setup %}

快速构建一个自己的网站，猛击[这里][jekyllbootstrap].

## 页面配置

### 首页
首页一般是显示最近的1-N篇博文，文章可只显示摘要：

{% highlight ruby %}
    post.content | strip_html | truncate:300 
{% endhighlight %}

### 分页
[JekyllBootstrap][jekyllbootstrap]默认的首页是`index.md`
但是如果需要分页效果的话需要使用的是`index.html`, 并且修改`_config.yml`, 添加一个配置项`paginate: 10`

## 个性化定制

### 评论系统
静态博客要实现评论功能必须依赖第三方评论系统。[JekyllBootstrap][jekyllbootstrap]是使用 Bootstrap 框架的 Jekyll 博客，默认的评论系统是 Disqus，然而 Disqus 在国内访问速度和稳定性并不理想，而且无法和国内的各种社交网站耦合，因此 Disquz 并不适合面向国内用户的网站。在国内也有诸多社会化评论系统，如多说、友言、灯鹭、评论啦等，这些基本都是 Disqus 的本地化版本，功能和 Disqus 非常相似。
定制多说评论系统请参考[liberize](http://liberize.me/)的[这篇博文](http://liberize.me/tech/jekyll-use-duoshuo-comment-system.html)

### 主题
[JekyllBootstrap][jekyllbootstrap]自带twitter和bootstrap主题，并支持快速切换。官网也提供了很多[漂亮的英文主题](http://jekyllthemes.org/)，但都不一定适合中文。博主找了很久也没发现很好的中文主题，推荐有奖...

【完】

[jekyllbootstrap]: http://jekyllbootstrap.com/