---
layout: post
title: python3 cook 
---

### python 是我最喜欢的语言
- 这里是我深耕的自留地


### Python 字典推导式
- 不单单有列表推导式,还要字典推导式

```
 d = {key: value for (key, value) in iterable}
```

### *args and **kwargs
- 前者是传递多个参数，后者是传递多个键值；
- 当你不确定你的函数里将要传递多少参数时你可以用*args；
- **kwargs允许你使用没有事先定义的参数名。

```
def print_everthing(*args):
    for count, thing in enumerate(args):
        print '{0}. {1}'.format(count, thing)
print_everthing('apple','banana','cabbage')
```

### 函数的multimethods：

```
def foo(a,b)：
    if isinstance(a,int) and isinstance(b,int):
        pass
    if isinstance(a, float) and isinstance(b, float):
        pass
    if isinstance(a, str) and isinstance(b, str):
        pass
    else:
        raise TypeError("unsupported argument types ({0}, {1})".format(type(a),type(b)))
```