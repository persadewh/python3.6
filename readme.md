
# Python3.6教程

## 虚拟环境和包

### 介绍

有时候应用需要一个特殊的库版本，因此需要为应用准备一个特定的环境。

### 创建虚拟环境

使用下面的命令，会在当前目录下创建tutorial-env目录，此时虚拟环境创建成功

```bat
python3 -m venv tutorial-env
```

激活虚拟环境

Windows:

```bat
tutorial-env\Scripts\activate.bat
```

Linux:

```sh
source tutorial-env/bin/activate
```

验证是否激活

```bat
(tutorial-env) D:\myself\pythonspace\python3.6>python
Python 3.6.0 (v3.6.0:41df79263a11, Dec 23 2016, 08:06:12) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import sys
>>> sys.path
['', 'D:\\myself\\python\\python36\\python36.zip', 'D:\\myself\\python\\python36\\DLLs', 'D:\\myself\\python\\python36\\lib', 'D:\\myself\\python\\python36', 'D:\\myself\\python\\python36\\lib\\site-packages', 'D:\\myself\\python\\python36\\lib\\site-packages\\pip-9.0.1-py3.6.egg', 'D:\\myself\\python\\python36\\lib\\site-packages\\flask-0.12.2-py3.6.egg', 'D:\\myself\\python\\python36\\lib\\site-packages\\markupsafe-1.0-py3.6-win-amd64.egg']
>>>
```

### 使用pip管理包

总原则为参照pip使用规则，不过在python中使用时，需要加上python，例如：

```bat
pip search astronomy
```

```bat
python -m pip search astronomy
```

例：

```bat
python -m pip install novas
```

升级pip

```bat
python -m pip install --upgrade pip
```

## Python

### 调用

```bat
python -c command [args]
```

```bat
python -m module [args]
```

### 参数传递

```python
import sys

print(sys.argv[0])
```

### 编码

```python
# -*- coding: utf8 -*-
```

## 简要介绍

### 数字

```python
>>> 2+2
4
>>> 50-5*6
20
>>>
```

```python
>>> 17/3
5.666666666666667
>>> 17//3
5
>>> 17%3
2
>>> 5*3+2
17
>>>
```

```python
>>> 5**2
25
>>> 2**7
128
>>>
```

### 字符串

使用单引号或者双引号

使用\进行转义

```python
>>> 'spam eggs'
'spam eggs'
>>> 'doesn\'t'
"doesn't"
>>> "doesn't"
"doesn't"
>>> '"yes", he said'
'"yes", he said'
>>> "\"yes\", he said"
'"yes", he said'
```

如果字符中含有转义字符\，则可以在字符串前加r

```python
>>> print('C:\name')
C:
ame
>>> print(r'C:\name')
C:\name
```

字符常量使用"""..."""或者'''...''',可以使用\连接上下两行

```python
(tutorial-env) D:\myself\pythonspace\python3.6\python3.6>strings.py
Usage: thingy [OPTIONs]
    -h              Display this usage message
    -H
```

使用 * 和 + 进行字符串连接

```python
>>> 3*'ll' + ' world'
'llllll world'
>>>
```

字符串索引

```python
>>> word = 'Python'
>>> word[0]
'P'
>>> word[1]
'y'
>>> word[-1]
'n'
>>>
```

```python
>>> word[-1]
'n'
>>> word[0:2]
'Py'
>>> word[0:-1]
'Pytho'
>>> word[2:5]
'tho'
>>> word[:2]
'Py'
>>> word[:2] + word[2:]
'Python'
```

字符串变量不允许对单个字符进行修改，如果需要，则重新创建字符串变量

```python
>>> word[1] = 'J'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>>
```

字符串长度

```python
>>> len(word)
6
```

### 列表

列表中值可以被修改，值类型可以不一样，但一般存放同一种类型的值

```python
>>> list = ['a', 1, 'b', 2, 'c']
>>> list
['a', 1, 'b', 2, 'c']
>>> list[0]
'a'
>>> list[0:]
['a', 1, 'b', 2, 'c']
>>> list[0:3]
['a', 1, 'b']
>>> list[-3]
'b'
>>> list[-3:]
['b', 2, 'c']
>>>
```

列表可直接相加

```python
>>> list = ['a', 1, 'b', 2, 'c']
>>> list1 = ['3', 'd', '4', 'e']
>>> list + list1
['a', 1, 'b', 2, 'c', '3', 'd', '4', 'e']
>>>
```

修改列表值

```python
>>> list1 = ['3', 'd', '4', 'e']
>>> list1[0] = 'A'
>>> list1
['A', 'd', '4', 'e']
```

追加值

```python
>>> list1.append('5')
>>> list1.append('f')
>>> list1
['A', 'd', '4', 'e', '5', 'f']
>>>
```

批量替换

```python
>>> list1
['A', 'd', '4', 'e', '5', 'f']
>>> list1[1:4] = ['W','E','I']
>>> list1
['A', 'W', 'E', 'I', '5', 'f']
```

删除元素

```python
>>> list1
['A', 'W', 'E', 'I', '5', 'f']
>>> list1[1:4] = []
>>> list1
['A', '5', 'f']
>>> list1[:] = []
>>> list1
[]
>>>
```

## 流程控制

### if

### for

### range()

### break,continue 和 else

### pass

### while

```python

```

## 定义函数