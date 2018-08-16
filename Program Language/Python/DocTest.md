```
#mydict.py

class Dict(dict):
    '''
    Simple dict also support access as x.y style
    >>> d1 = Dict()
    >>> d1['x'] = 100
    >>> d1.x
    100
    >>> d1.y = 200
    >>> d1['y']
    200
    >>> d2 = Dict(a = 1, b = 2, c = '3')
    >>> d2.c
    '3'
    >>> d2['empty']
    Traceback (most recent call last):
        ...
    KeyError: 'empty'
    >>> d2.empty
    Traceback (most recent call last):
        ...
    AttributeError: 'Dict' object has no attribute 'empty'
    '''
    def __init__(self, **kw):
        super(Dict, self).__init__(**kw)
    def __getattr__(self, key):
        try:
            return self[key]
        except KeyError:
            raise AttributeError(r"'Dict' object has no attribute '%s'" %key)
    def __setattr__(self, key, value):
        self[key] = value
if __name__ == '__main__':
    import doctest
    doctest.testmod()
```

###使用doctest模块进行文档测试
----
1. 文档注释使用多行注释'''___'''
2. \>\>\> 和命令需要有空格
3. 使用python mydict.py运行脚本，如果没有错误，则没有输出，
   否则会输出当前的期望值和错误值
