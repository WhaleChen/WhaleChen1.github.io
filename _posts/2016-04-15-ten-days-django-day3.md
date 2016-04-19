---
layout: post
title: Ten Days for Django day3 generic views and testing
---

### Generic views 通用视图: Less code is better
- Django用一种通用的方式来使得views中的代码变得简单
- 在url中需要改为通配的url ```url(r'^(?P<pk>[0-9]+)/$', views.DetailView.as_view(), name='detail') ```
- 第二步在views.py中需要引入 django.views.generic 建立继承 generic.ListView 和 generic.DetailView 的子类。

> “Code without tests is broken by design.” --Jacob Kaplan-Moss 

### Testing strategies
- [test-driven development](https://en.wikipedia.org/wiki/Test-driven_development): 
- Testing 是越多越好：in testing redundancy is a good thing.



