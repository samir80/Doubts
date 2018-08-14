### tempfile 创建临时目录
```
import tempfile
TEMP = TEMP = tempfile.mkdtemp(suffix='_py', prefix='learn_python_')
print(TEMP)
```
### 运行结果

![Result](https://github.com/samir80/Doubts/blob/master/Program%20Language/Python/Res/tempfile.mkdtemp.png)
suffix:为临时目录后缀; prefix:为临时目录前缀; 中间的名称，类似GUID为随机值；
临时目录的生成目录为TEMP环境指定（如果你没设置的话）
