# 1. python —— for else

```python
用于写文件查找逻辑
x = {"冯昭宇":1,"徐洁":2,"王文烨":3}

for key in x:
    if(key=="冯昭宇"):
    	print("找到冯昭宇了")
else：
	print("没有找到冯昭宇")
```

# 2. python —— 正则化

```python
import re


re.match

re.search

re.findall

re.sub

s = "www.baidu.com;www.google.com"

r = "www\.(.+?)\.com"

print(re.findall(r, s))
```

# 3. python—— fstring

```python
# a = {"a":1, "b":2}

print("a的值为:", a["a"])

d = 4

print(f"a:{1.23:8} b:{1.23:4}")
print(f"a:{1.234:.2} b:{1:02} c:{1:2}")

print(bin(123))
print(hex(123))

print(int(bin(123), base=2))
print(int(hex(123), base=16))

float("1.234")
print(float("nan"))
float("inf")
```

# 4. python —— psutil 查看cpu占用

```python
import psutil
from time import sleep

psutil.Process().cpu_percent()

while True:
    print(psutil.cpu_percent())
    sleep(1)
```

# 5. python—— 工作目录 cwd

```python
工作路径 相对路径

当前文件的绝对路径
DIR_PATH = os.path.dirname(os.path.abspath(__file__))
D:\Document\Study\研一上_项目\05调度平台项目\CommandFront_new\CommandFront\


os.path.abspath(__file__)
D:\Document\Study\研一上_项目\05调度平台项目\CommandFront_new\CommandFront\parseThread_hxq.py


```
# 6. 命令行进入debug模式
https://blog.csdn.net/weixin_48629412/article/details/108822562

```
python -m pdb hello.py
```

```
next:单步跳过
step:单步进
c: 继续执⾏
w: 显⽰当前正在执⾏的代码⾏的上下⽂信息
a: 打印当前函数的参数列表
s: 执⾏当前代码⾏，并停在第⼀个能停的地⽅（相当于单步进⼊）
n: 继续执⾏到当前函数的下⼀⾏，或者当前⾏直接返回（单步跳过）
```

```python
import pdb
def test():
    pdb.set_trace()
    return "test"
print(test())
```

# 7. python 运行

命令行运行

```
& D:/Program/Python/ananconda3/envs/CFPLATFORM/python.exe d:/Document/Study/研一上_项目/00系统智能故障诊断开发环境设备项目/0902版/0821版/General_Platform_for_Falut_Diagnosis/manage.py runserver
```

查看工作路径



# 8. conda命令操作

查看虚拟环境

```
conda env list
```



删除虚拟环境

```
conda remove -n <env name> --all
```



创建虚拟环境

```
conda create -n <your name> python==3.7

```



激活虚拟环境

```
conda activate <your>
```

安装依赖包

```
pip install django

pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
```

### python深拷贝

切片近似于列表赋值 深拷贝

```python
1.赋值
a=b
2.copy()
new = old.copy()
3.列表生成
new = [i for i in old]
4.for循环遍历赋值
for i in range(len(old)):
    new.append(old[i])
5. 切片
new = old[:]
6.深拷贝
new = copy.deepcopy(old)
```

# 9. timeit用法

[使用timeit测试Python函数的性能 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/301041836)

```
import timeit
import random
import arrow

# 本地函数
def stupid1():
    return random.randint(1, 10)

# 依赖其他函数
def stupid2():
    return stupid1()

# 依赖其他包或者模块
def stupid3():
    return arrow.now()

print(timeit.timeit('stupid1()', setup='from __main__ import stupid1'))
print(timeit.timeit('stupid2()', setup='from __main__ import stupid2'))
print(timeit.timeit('stupid3()', setup='from __main__ import stupid3', number=100))


print(timeit.timeit(stmt='a=10;b=10;sum=a+b'))

# 1. ···法
import timeit
import_module = "import random"
testcode = ''' 
def test(): 
    return random.randint(10, 100)
'''
# 2. ying'hao
print(timeit.repeat(stmt=testcode, setup=import_module))
```

# 10. hasattr()函数

用于判断对象是否包含对应的属性

```python
hasattr(object,name)
```



