---
layout:     post
title:      ubuntu 安装jekyll
subtitle:   Ubuntu install jekyll
date:       2020-03-24
author:     xuenhua
header-img: img/post-bg-rwd.jpg
catalog: true
tags:
    - jekyll
    - Ubuntu
    - Linux
    - ruby
---

## 安装ruby

```
# sudo apt-get update
# sudo apt-get install ruby
或者
# sudo apt-get install ruby2.0
#不安装dev安装jekyll会报错
apt-get intall ruby-dev

```
## 安装jekyll是提示需要ruby >2.4,apt安装为2.3，需要从源码安装
```
$ tar zxvf ruby-2.4.0.tar.gz
$ cd ruby-2.4.0
$ ./configure
$ make
$ sudo make install
```
## 查看版本ruby -v如果还是旧版，删除旧版重新安装或者修改链接
如果已经安装了低版本的ruby，默认安装在/usr/bin目录下，若此时执行ruby -v，还是会显示低版本的ruby，若默认使其执行2.4版本的ruby，则可通过软链接的方式实现

```
ruby -v
find /usr -name "ruby"
sudo rm /usr/bin/ruby
sudo ln -s /usr/local/bin/ruby /usr/bin/ruby
ruby -v
```

## 更新国内镜像
https://gems.ruby-china.com
```
$ gem update --system # 这里请翻墙一下
$ gem -v
2.6.3
$ gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
$ gem sources -l
https://gems.ruby-china.com
# 确保只有 gems.ruby-china.com
```

## 你可以用 Bundler 的 Gem 源代码镜像命令。

```
$ bundle config mirror.https://rubygems.org https://gems.ruby-china.com
这样你不用改你的 Gemfile 的 source。
source 'https://rubygems.org/'
gem 'rails', '4.2.5'
...
```

## 安装jekyll

```
$ gem install jekyll bundler
~ $ jekyll new my-awesome-site
~ $ cd my-awesome-site
~/my-awesome-site $ bundle install
~/my-awesome-site $ bundle exec jekyll serve
# => 打开浏览器 http://localhost:4000
```
[![](https://github.com/xuenhua/xuenhua/blob/master/img/ads/ali.jpg?raw=true)](https://s.click.taobao.com/t?e=m%3D2%26s%3D7ngZThCwaCUcQipKwQzePCperVdZeJviEViQ0P1Vf2kguMN8XjClAkIrrC3KoeznlGm4gdHtBuLzb2M2f%2FoaoHRTtLCoLbOHFQZVrNNFjh9uK2ud60h6lE1WovaI4eZxiYWStHE%2B0ceFSvfO0N66nzO5MaXTjVACe2l9FrhMrdPv%2BfHIT3CFRNdvthxiSWPsdnn9YK8Mk5jfleFWJLnarYaVo1qVTQzCfw%2F8dhe%2BNbDGDmntuH4VtA%3D%3D)
