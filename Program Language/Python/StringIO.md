```
from io import StringIO
f = StringIO(u'halo\n')
print(f.getvalue())
f.write(u'hello from the other side\n')#overwrite
print(f.getvalue())
```
### 说明
1. python2.7(python3未尝试)环境下，需要在字符串前加'u',否则会报如下错误：
```
TypeError: initial_value must be unicode or None, not str
```
