---
layout: post
title: pydoc Documentation generator and online help system 
---


### Be helped is the first step 助人先自助
- 学习python也大半年了，发现自己越来越喜欢pythonic的风格了，既然喜欢，那就更深入的了解python的一切吧！
- 首先需要自己看文档，不过文档固然好，是否有更简便的方式来获得文档帮助呢？
- 这里推荐pydoc 是最佳的方式

### pydoc 的使用说明
- 我的操作系统是win7，使用cmder作为console。关于cmder的好处和如何安装cmder可以参考 [cmder github](http://www.amilitalia.it/github.com/bliker/cmder.html),如果需要中文帮助可以直接google或者baidu
- 使用版本为 python3.5

#### 在交互界面
- 直接使用 ``` help(thing) ``` 比如 ``` help("sys")``` 获得 sys模块的帮助信息

#### 在console 中
- 情况一：
- 在码代码的过程中，最常见的一种情况是知道某个函数，或者库，不过不知道具体用法。需要一种方式比直接google还快速而准确。
- 在console 中，只需要 ``` pydoc <function | module> ``` 就可以了 比如 ``` pydoc print ``` 直接输出，可以获得所有使用信息。
- 情况二：
- 有时候我并不知道这个函数的确切名称，希望做一个模糊搜索
- 在console 中，使用，``` pydoc -k <keyword> ``` 这样可以返回单行的包含这个keyword 的所有module，简单的解释可以让你知道所需要的module

#### 浏览器
- 在另一些时候，我们希望用一种简单的方式看看所有module，而不用直接登录 doc.python.org 来获取信息。
- 这个时候，可以在console中，输入 ``` pydoc -p <port> ``` 来做一个server，比如 ``` pydoc -p 1234 ``` 简单讲就是通过端口1234，提供你可以通过html的浏览，这里通常会提示 127.0.0.1: 1234 来获得所有的模块和你可能需要的帮助信息，而且界面比较简单，不用看不必要的各种信息。``` 
- 当然这个命令在 python 3.2之后，可以用 更简单的 ``` podoc -b ``` 来替代，会自动寻找没有使用的端口而不用自设端口号

#### 总结：
- 本文简单汇总了pydoc各种情况下的使用方式
- 本文的资料来源是 [doc.python.org](https://docs.python.org/3/library/pydoc.html)  
- 如果需要进一步帮助，当然我建议最好的方式当然是:
- 进入console 然后  ``` pydoc pydoc ```
- 就是这样！
