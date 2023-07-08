---
layout: post
title: Python - Best Practices
description: What are the best ways to use Python
tags: ["generative-models", "maths"]
---

### Tips and tricks

#### How to use "." to access members of a dictionary?
By default, if you use a python `dict()`, to access members of the dictionary you have to do so via `dict[key]` notation. I would prefer to do it with dict.key notation. 
The best way to do it is via `easydict` or `DotMap`.

**dotmap**

To install `dotmap`, 
```
pip install dotmap
```

To use dotmap

``` python
from dotmap import DotMap

m = DotMap()
m.hello = 'world'
m.hello
m.hello += '!'
# m.hello and m['hello'] now both return 'world!'
m.val = 5
m.val2 = 'Sam'
```

**easydict**

To install easydict

```
pip install easydict
```

To use easydict

```
>>> from easydict import EasyDict as edict
>>> d = edict({'foo':3, 'bar':{'x':1, 'y':2}})
>>> d.foo
3
>>> d.bar.x
1
>>> d = edict(foo=3)
>>> d.foo
3
```



