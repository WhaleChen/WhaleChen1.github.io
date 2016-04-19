---
layout: post
title: Dragonfly a speech recognition framework in python
---

### Talk with your computer programmer 语音计算机编程
- 用自然语言编程是python最核心的突破，一直以来python在这点上让我激动不已。
- 自然语言的一个特性是听觉，让编程语言能够被述说，这样
- 在[2013 python 大会上 tavisrudd](http://www.csdn.net/article/2013-08-14/2816563-using_voice_to_code) 就展示了这种特别的编程方式
- 我喜欢想象，我就可是想象这种特别的突破，最后是否会使得编程语言真正开始取代自然语言成为真正意义上的世界语？

### 首先需要的是一款Python语音识别扩展库
- [Dragonfly](http://pythonhosted.org/dragonfly/)，是tavisrudd 所使用的。
- 示范代码

```
from dragonfly.all import Grammar, CompoundRule

# Voice command rule combining spoken from and recognition processing
class ExampleRule(CompoundRule):
    spec = "做事"
    def _process_recognition(self, node, extras):
        print "Voice command spoken"

# Create a grammer which contains and loads the command rule
grammar = Grammar("example grammar")
grammar.add_rule(ExampleRule())
grammar.load()
```

- 你会看到需要一个规则，然后开始识别，之后因着这个规则就可以让电脑做事情。

### 用途
- Dragonfly offers a powerful and unified interface to developers who want to use speech recognition in their software.



