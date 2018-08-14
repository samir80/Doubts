## pass语句作用

1. 空语句 do nothing
2. 保证格式完整
3. 保证语义完整

*以if语句为例，在c或c++/java中：
```
if(true)
;    //do nothing
else
{
    //do something
}
``





*对应于python就要这样写：
```
if true:
    pass #do nothing
else:
    #do something
```

1. pass语句在函数中的作用
当你在编写一个程序时，执行语句部分思路还没有完成，这时你可以用pass语句来占位，也可以当做是一个标记，是要过后来完成的代码。比如下面这样：
```
def iplaypython():
    pass
```

定义一个函数iplaypython，但函数体部分暂时还没有完成，又不能空着不写内容，因此可以用pass来替代占个位置。

2. pass语句在循环中的作用
pass也常用于为复合语句编写一个空的主体，比如说你想一个while语句的无限循环，每次迭代时不需要任何操作，你可以这样写：
```
while True:
    pass
```

以上只是举个例子，现实中最好不要写这样的代码，因为执行代码块为pass也就是空什么也不做，这时python会进入死循环。
