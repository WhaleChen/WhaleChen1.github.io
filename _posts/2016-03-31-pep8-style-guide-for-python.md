---
layout: post
title: python syle guide and Sublime Text 3 approach 
---
    

## 编程规范
- 学习python有大半年了，很喜欢python的风格。不过写程序写多了越发觉得，自己需要一个规范使得自己所写的东西能够被以后的自己快速的阅读。同时也能够被别人快速的阅读。
- [pep8](https://www.python.org/dev/peps/pep-0008/#introduction) 是PEP： Python Enhancement Proposals 中的 0008 号文件。主要针对规范python代码的编写规范指定的。
- pep8 中有一段特别有趣: 翻译过来就是 如果编程没有一致性，就是小智小慧的骗人伎俩。

> A Foolish Consistency is the Hobgoblin of Little Minds

### 可读性为先
- "Readability counts". 这是python的精华。
- 在我看来，python是一场变革，增加了人们直接阅读和查找代码的可能性。如果我真是这样想的，那么去精确而严谨地遵守一套编程规范就变得非常必要。
- 语言，之所以能够被广为流传，就是因为规范。对于python编写，编程规范是为了一致性，因此，优先级如下：
	+ 一个模块或者函数内的一致性优先；
	+ 其次是一个项目的一致性；
	+ 最后是整体的一致性。 
- 一些可以忽略指南要求的原因：
	+ 如果为了保持项目中的一致性或者向上兼容，重要性优先于pep规范；
	+ 如果使用pep使得程序读起来不容易，那么放下pep；
	+ 如果你周围的代码都并不遵循pep，为了保持一致性可以放下pep；
	+ 如果代码出现的时间先于pep8,那么没有理由要求项目使用pep8.


### 代码布局Code layout:
- 缩进Indentation
	+使用 4个空格
    +sublime使用帮助：tab相对来讲，比较常用在于快速，因此需要设置一下配置，使得tab能够直接出现4个空格，在sublime3 中，可以在Preferences.sublime-settings 中使用代码，具体可以参考 [sublime text3里 修改TAB键为缩进为四个空格](sublime text3里 修改TAB键为缩进为四个空格)

```
    "tab_size": 4,
    "translate_tabs_to_spaces": true,
```


```
# Aligned with opening delimiter
# 对于敞开的分节符
foo = long_function_name(var_one, var_two,
						 var_three, var_four)
# More indentation included to distinguish this from the rest.
# 区别其他部分需要多加一个缩进。

def long_funtion_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)

# Hanging indents should add a level.
# 悬挂式的缩进需要增加一层

foo = long_function_name(
    var_one, var_two,
    var_three, var_four)

#关于if 中条件过长，则建议使用如下：

if (this_is_one_thing
		and that_is_one_thing):
	do_something()

#对于右边封闭符号，建议没有缩进：

result = some_function_that_takes_arguments(
	'a','b','c',
	'd','e','f',
)
```

### 空格或者Tab
- 空格是首选
- Python 3不允许使用混合Tab 和spaces

### 最大行宽
- 限制为79个字符。
- 文本和注释则被限制到72个字符。
- sublime使用帮助: [SublimeLinter-pep8](https://packagecontrol.io/packages/SublimeLinter-pep8)

```
class Rectangle(Blob):


    def __init__(self, width, height,
                color='black', emphasis=None, highlight=0):
        if (width == 0 and height == 0 and
                color == 'red' and emphasis == 'strong' or
                highlight > 100):
            raise ValueError("sorry, you lose")
        if width == 0 and height == 0 and (color =='red' or
                                            emphasis is None):
            raise ValueError("I don't think so -- values are  %s, %s" %
                            (width, height))
        Blob.__init__(self, width, height,
                    color, emphasis, highlight)

```




### Blank Lines 空行
- 最高层的函数和类的定义需要空2行；
- 在类中定义方法空一行；
- 额外空行也可被用在区分不同类型的函数组中，节制使用；
- 额外空行在必要的时候可以用来分割逻辑部分，节制使用；
- Python 接受 control-L 作为空白符，不过因编辑器不同会有差异。

### 源代码 Source File Encoding
- 我是在没有看懂，待补充...

### 引入Imports
- 引入每个模块使用独立行的方式
- 顺序：标准库 第三方库 本地应用或者模块 同时不同类型的引入需要加入一行空行


