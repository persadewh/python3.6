
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
