---
layout: post
title: Ten Days for Django day1 database and mysql
---

### 解决问题的姿势
- 在win7下安装mySQL发生了问题，在发生问题的时候，我特别急切希望解决问题，不过这个并非问题解决的最佳姿势。
- 首先，世界上的事情分为两类，一类是有问题，一类是没有问题。如果问题发生，一定是有一个梗，不管是打字错误，还是理解问题，这其实就是一次绝佳的进步机会。如果世界上没有了问题，那么其实智力存在的意义似乎就不大了。
- 另外，我发现如果我急切渴求问题被解决，最后的结果如果是问题被一种我想不到的途径解决了之后，我对于这个问题的描述和同类问题的解决方式并不会变化。同时，我所能够记录的内容大致如：昨天发现问题1，今天解决了。如果任何其他人碰到同类的问题，如果咨询我，我一定无法给出非常好的帮助。因为，太想解决问题，使得我对于问题本身不感兴趣，而对于问题的观察也没有提升。
- 好了，什么问题？当问题出现的时候，首先描述清楚问题要比解决问题更重要。


### 关于在win7系统安装MySQL中出现的问题：
- 系统：win7 
- MySQL 安装版本： [mysql-5.7.11-winx64](http://dev.mysql.com/downloads/mysql/5.7.html)  免安装版本！
- 出现问题描述：
    + 问题一：启动mysql 时候出现: failed to set datadir to C:\mysql-5.7.11-winx64\data\ 无法创建data 文件夹的问题： mysql 没有启动 和 没有初始化.通过百度，这篇文章帮助了我[mysql-5.7.10-winx64免安装版配置时碰到的问题](http://blog.csdn.net/fishernemo/article/details/50629332) 其实问题在于我没有初始化~
        + 解决：[初始化]() 
    + 问题二：ERROR 1045 (28000): Access denied for user 'ODBC'@'localhost' (using password: NO)
        + 现象：初始化之后无法登录， 主要是 需要配置 user  使用
        + 解决:  

```
mysql --user=root
```

### 数据库操作(DDL)
- SHOW: 查看
- CREATE: 创建
- ALTER：修改
- USE：使用
- SELECT: 打开
- DROP

### 数据表操作
- VARCHAR 可变
- ENUM 枚举 一个 / SET 多个
- 使用 SET NAMES GBK; 来应对中文
- unsigned 无符号，正
- zerofill 属于 unsigned

### 存储Engine
- InnoDB：读写效率低空间大，支持外线，并发。
- MyISAM：插入快，不支持事务。
- MEMORY: 数据存在内存，快，不过不稳定。

### Django ORM 对象关系映射

### Databases installation in Django 
- [MySQL](https://docs.djangoproject.com/en/1.9/ref/databases/#mysql-notes)
- [问题一](http://www.cnblogs.com/ldm1989/p/4210743.html)
    +解决：[Microsoft Visual C++ Compiler for Python 2.7 ](https://www.microsoft.com/en-us/download/confirmation.aspx?id=44266)
- [问题二](http://www.tuicool.com/articles/63EjYj)
    +解决：[驱动问题](http://vdisk.weibo.com/s/aBSXQ0shtv7cN?sudaref=www.baidu.com)