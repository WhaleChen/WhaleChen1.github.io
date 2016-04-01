---
layout: post
title: python syle guide 
---


## 编程规范
- 学习python有大半年了，很喜欢python的风格。不过写程序写多了越发觉得，自己需要一个规范使得自己所写的东西能够被以后的自己快速的阅读。同时也能够被别人快速的阅读。
- [pep8](https://www.python.org/dev/peps/pep-0008/#introduction) 是PEP： Python Enhancement Proposals 中的 0008 号文件。主要针对规范python代码的编写规范指定的。
- pep8 中有一段特别有趣: 翻译过来就是 如果编程没有一致性，就是小智小慧的骗人伎俩。

> A Foolish Consistency is the Hobgoblin of Little Minds

## 可读性为先
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


## 代码布局Code layout:
- 缩进Indentation
	+使用 4个空格

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




