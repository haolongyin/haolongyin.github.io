---
layout: post
title:  "在Github Pages上架设Jekyll!"
date:   2016-08-02 00:01:03 +0800
categories: code
---

这个博客是用Jekyll在Github Pages上搭建了，这里分享记录一下这个过程，我参考的教程有以下几个英文页面：

[Setting up your GitHub Pages site locally with Jekyll](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)

1. 首先，确保你的计算机安装了Ruby和Bundler的环境。

2. 在计算机上建立一个文件夹，在里面建立我们的网站：

{% highlight code %}
$ git init my-jekyll-site-project-name
{% endhighlight %}

3. 在这个文件夹里创建一个包括以下代码的Gemfile

{% highlight code %}
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
{% endhighlight %}

4. 运行Bundle Install安装Jekyll的Gem

{% highlight code %}
$ bundle install
{% endhighlight %}

5. 运行以下代码建立Jekyll网站模版

{% highlight code %}
$ bundle exec jekyll new . --force
{% endhighlight %}

6. 测试运行

{% highlight code %}
$ bundle exec jekyll serve
{% endhighlight %}

7. 在Github建立一个新的Repository，命名为<用户名>.github.io

8. 将本地建立好的Jekyll网站推送到Github的Repository的master branch

{% highlight code %}
$ git remote add origin git@github.com:haolongyin/haolongyin.github.io.git
$ git push -u origin master
{% endhighlight %}

9. 浏览器指向<用户名>.github.io应该能看到网站上线了。

10. 如果要改自己的域名将A纪录的值指向192.30.252.153或192.30.252.154，然后在Setting里添加域名纪录。具体可以参考这篇文章[Setting up an apex domain](https://help.github.com/articles/setting-up-an-apex-domain/)

