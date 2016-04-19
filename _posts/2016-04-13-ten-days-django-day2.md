---
layout: post
title: Ten Days for Django day2 template 
---

### 问题一： 对于问题的高效解决
- 切问题： 如何

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


### [http404 error的两种显示方式](https://docs.djangoproject.com/en/1.9/intro/tutorial03/#raising-a-404-error)
- try except 的方式自然是最普通的方式，注意需要引入 django.http.Http404 
- django 的好处就是有众多的shortcuts，就如同cheetsheet一样。django.shortcuts.get_object_or_404 这个方法就可以直接取代get方法，并附带一个404报错
- [get_object_or_404](https://docs.djangoproject.com/en/1.9/topics/http/shortcuts/#django.shortcuts.get_object_or_404) 你会发现注释用途为:
- "Calls get() on a given model manager, but it raises Http404 instead of the model’s DoesNotExist exception." 这是很有趣的！

###  Cross Site Request Forgery(CSRF) 跨站请求伪造 防护
- django 用一个标签来解决这类问题 [{% csrf_token %} ](https://docs.djangoproject.com/en/1.9/ref/templates/builtins/#std:templatetag-csrf_token)
- all POST forms that are targeted at internal URLs should use the {% csrf_token %} template tag. 简单讲，如果post forms 的连接是内部连接，那么必须使用 这个标签。
