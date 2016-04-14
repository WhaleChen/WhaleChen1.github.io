---
layout: post
title: Ten Days for Django day2: template 
---

### 问题一： 对于问题的高效解决
- 切问题：
- 

### [url](https://docs.djangoproject.com/en/1.9/topics/http/urls/#naming-url-patterns):
- url 可以匹配，同时可以传参数
- 有两种形式，一种简单的形式：

```
from django.conf.urls import url

from . import views
# simple URL conf：
url(r'^articles/([0-9]{4})/([0-9]{2})/$', views.month_archive)， 
# named groups：
url(r'^articles/(?P<year>[0-9]{4})/(?P<month>[0-9]{2})/$', views.month_archive) 

```

- 这两种形式都可以接受 如 /articles/2015/03 第一种，简单形式传入 views.month_archive(request, '2005', '03'), 后一种则是 views.month_archive(request, year='2005', month='03')