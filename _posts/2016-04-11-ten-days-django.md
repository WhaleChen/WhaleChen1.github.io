---
layout: post
title: Ten Days for Django day0  
---

### 缘起
- 开始进入工作准备状态，发现自己需要一个突破口。python web backend engineer是最好的开始。而首先，需要django作为我学习能力的自我测试。在没有django知识的情况下，我希望用django建立一个网站。以此开始转变为程序员之路的第一步。
- 学习范式：由于程序员是一个终生学习的职业，因此在这里，我试图恪守学习记录，并按照范式学习，也为工作之后的我建立良好的工作习惯。

### Day0
- [官网tutorial](https://docs.djangoproject.com/en/1.9/contents/)
- 学习的入口一定是官网，因为这里有几乎我们需要的一切一手最新的知识。
- 通过官网学习，也提供给自己以后工作需要学习新知识的范式
- 我发现Django的 文档真的写得非常好，是特别值得学习的。同时命名规范也遵循pep8，使得学习Django 更如同学习建构一个流行的框架的开发。
- 我学习的记录：由于官网写得非常好，我真的不需要在重复造轮子了，这不符合Django的 精神。我这里通过提示和关键点来给自己学习做一些必要的记录和连接。
    + 提示:  主要是一些关键的布局和 典范。
    + 关键点：主要涉及名词解释和一些比较容易混淆的地方之处自己的理解。

#### Django 的一些提示
- 放置Django 代码的位置：

> Put your code in some directory outside of the document root, such as /home/mycode. 

- [TIME_ZONE](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) 时区在国际上命名和简写是有一套标准的。注意依照这套标准

- [DRY principle('Don't repeat yourself'): ](https://docs.djangoproject.com/en/1.9/misc/design-philosophies/#dry)每一个概念或数据只出现在一个地方。避免冗余。标准化是好的！





#### 关键点Keywords:
- runserver
- app: An app is a Web application that does something
- views
- include() function: Allow referencing other URLconfs. 
- URLconfs: 

>The include() function allows referencing other URLconfs. Note that the regular expressions for the include() function doesn’t have a $ (end-of-string match character) but rather a trailing slash. Whenever Django encounters include(), it chops off whatever part of the URL matched up to that point and sends the remaining string to the included URLconf for further processing.


- models.py: the single definitive source of truth about your data.
- [Field](https://docs.djangoproject.com/en/1.9/ref/models/fields/#django.db.models.Field): Field is an abstract class that represents a database table column. 实际上Field可以认为是一种将数据库和python类连接的接口。 

- [Activating models process](https://docs.djangoproject.com/en/1.9/intro/tutorial02/): (NOTE! Django apps are “pluggable”) Change the INSTALLED_APPS setting.py to include config settings (eg. 'polls.apps.PollsConfig' --> run command $python manage.py makemigrations <appname>

- [template](https://docs.djangoproject.com/en/1.9/topics/templates/) : https://docs.djangoproject.com/en/1.9/misc/design-philosophies/

