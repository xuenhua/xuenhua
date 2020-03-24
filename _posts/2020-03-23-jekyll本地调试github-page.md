---
layout:     post
title:      解决本地调试Github Page报错
subtitle:   Github Page
date:       2020-03-23
author:     xuenhua
header-img: img/post-bg-rwd.jpg
catalog: true
tags:
    - jekyll
    - githubpage
---

## 本地调试HX Blog报错解决方法
```
 Dependency Error: Yikes! It looks like you don't have jekyll-paginate or one of its dependencies installed. In order to use Jekyll as currently configured, you'll need to install this gem. If you've run Jekyll with `bundle exec`, ensure that you have included the jekyll-paginate gem in your Gemfile as well. The full error message from Ruby is: 'cannot load such file -- jekyll-paginate' If you run into trouble, you can find helpful resources at https://jekyllrb.com/help/! 
                    ------------------------------------------------
      Jekyll 4.0.0   Please append `--trace` to the `serve` command 
                     for any additional information or backtrace. 
                    ------------------------------------------------
```
修改Gemfile，添加
```
source "https://rubygems.org"

gem "jekyll"
gem "jekyll-paginate"
```

[![](https://github.com/xuenhua/xuenhua/blob/master/img/ads/ali.jpg?raw=true)](https://s.click.taobao.com/t?e=m%3D2%26s%3D7ngZThCwaCUcQipKwQzePCperVdZeJviEViQ0P1Vf2kguMN8XjClAkIrrC3KoeznlGm4gdHtBuLzb2M2f%2FoaoHRTtLCoLbOHFQZVrNNFjh9uK2ud60h6lE1WovaI4eZxiYWStHE%2B0ceFSvfO0N66nzO5MaXTjVACe2l9FrhMrdPv%2BfHIT3CFRNdvthxiSWPsdnn9YK8Mk5jfleFWJLnarYaVo1qVTQzCfw%2F8dhe%2BNbDGDmntuH4VtA%3D%3D)
