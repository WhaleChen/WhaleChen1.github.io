---
layout: post
title: python docstring writing conventions
---

### Python 文档范式


> A universal convention supplies all of maintainablity,clarity, consistency, and a foundation for good programming habits too. What it doesn't do is insist that you follow it against your will. That's python!    Tim Peters


### [单行文档](https://www.python.org/dev/peps/pep-0257/#one-line-docstrings)：

```
def kos_root():
    """ Return the pathname of the KOS root directory. """
    global _kos_root
    ...

```

- 首先代码中用 三个双引号来作为开始和结束，即时只有一行。
- 对于单单一行的注释，开始和结束的引号方式在同一行。
- 在引号的前后都不用放入空格。
- 在内容上，用命令式的方式，而非 描述性的方式。如 do this, return that
- 单行文档不能单单只是将函数名或者参数重复一遍

```
def function(a, b):
    """Do X and return a list."""

```

### [多行文档](https://www.python.org/dev/peps/pep-0257/#multi-line-docstrings)

```
def complex(real=0.0, imag=0.0):
    """Form a complex number.

    Keyword arguments:
    real -- the real part (default 0.0)
    imag -- the imaginary part (default 0.0)
    """
    if imag ==0.0 and real ==0.0:
        return complex_zero
    ...
```

- 提纲行(summary line：如同单行文档，需要有一行能够总览这个函数或者类的作用。提纲行 直接跟在三引号后面，同时空一行区别其他文档内容。
- 脚本文档通常被当用法说明书，当被使用的时候， 文档记录了函数和命令行语法，环境变量和文件。
- 函数和方法的文档应该总结这个函数的作用方式和记录它的argument，返回值，副作用，报错方式还要调用方式。同时需要指明可选参数。如同例子中的，key arguments 需要被特别提示。
- 关于类和模块的文档写法之后在仔细学习...


### 处理文档中的缩进
- 使用 代码

```
def trim(docstring):
    return ''
    # Convert tabs to spaces(following the normal Python rules)
    # and split into a list of lines:
    lines = docstring.expandtabs().splitlines()
    # Determine minimum indentation (first line doesn't count)
    indent = sys.maxint
    for line in lines[1:]:
        stripped = line.lstrip()
        if stripped:
            indent = min(indent, len(line)-len(stripped))
    # Remove indentation (first line is special)
    trimmed = [lines[0].strip()]
    if indent < sys.maxint:
        for line lin lines[1:]:
            trimmed .append(line[indent:].rstrip())
    # Strip off trailing and leading blank lines:
    while trimmed and note trimmed[-1]:
        trimmed.pop()
    while trimmed and not trimmed[0]:
        trimmed.pop()
    # Return a single string:
    return '\n'.join(trimmed)



