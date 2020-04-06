---
layout:     post
title:      jekyll地址绑定127.0.0.1导致其他机器无法访问
subtitle:   jekyll can't be accessed because of binding 127.0.0.1
date:       2020-04-06
author:     xuenhua
header-img: img/post-bg-rwd.jpg
catalog: true
tags:
    - jekyll
    - 树莓派
    - Raspberry PI

---

## 树莓派启动jekyll服务后本地可以访问，其他电脑不能访问
排查了iptables或其他防火墙设置没有问题，但是仍然无法访问，是由于jekyll绑定了默认ip 为127.0.0.1，
解决方法：启动脚本增加--host参数
```
bundle exec jekyll serve --host=0.0.0.0 
```

[![](https://github.com/xuenhua/xuenhua/blob/master/img/ads/ali.jpg?raw=true)](https://s.click.taobao.com/t?e=m%3D2%26s%3D7ngZThCwaCUcQipKwQzePCperVdZeJviEViQ0P1Vf2kguMN8XjClAkIrrC3KoeznlGm4gdHtBuLzb2M2f%2FoaoHRTtLCoLbOHFQZVrNNFjh9uK2ud60h6lE1WovaI4eZxiYWStHE%2B0ceFSvfO0N66nzO5MaXTjVACe2l9FrhMrdPv%2BfHIT3CFRNdvthxiSWPsdnn9YK8Mk5jfleFWJLnarYaVo1qVTQzCfw%2F8dhe%2BNbDGDmntuH4VtA%3D%3D)
