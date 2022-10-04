# python3

## 基础知识

### 基本数据类型
#### 数字(Number)
- 支持int、float、bool、complex（复数）
- 内置type(a)函数查询数据类型或者isinstance(a,int)
- 数值运算+-*/(除得到浮点数)  //除(得到整数) %(取余) **乘方
- 内置函数
  - abs(x):绝对值
#### 字符串(String)
- 单引号或双引号括起来,反斜杠\转义特殊字符
- 取值 变量[头下标:尾下标]
- 字符串不能改变
- 三引号("""),允许跨多行
- 内置函数
  - capitalize():字符串的第一个字符转换为大写
#### 列表(List)
- 列表是写在方括号 [] 之间、用逗号分隔开的元素列表
- 变量[头下标:尾下标:步长]
- 列表可变
- 内置方法
  - len(list) 列表元素个数
  - max(list) 返回列表元素最大值
  - min(list) 返回列表元素最小值
  - list(seq) 将元组转换为列表
#### 元组(Tuple)
- 元组写在小括号 () 里，元素之间用逗号隔开
- 元组（tuple）与列表类似,元素不能修改
- 内置方法
  - len(tuple) 列表元素个数
  - max(tuple) 返回列表元素最大值
  - min(tuple) 返回列表元素最小值
  - tuple(iterable) 将可迭代系列转换为元组
#### 集合(Set)
- 基本功能是进行成员关系测试和删除重复元素
- 大括号 { } 或者 set() 函数创建集合，注意：创建一个空集合必须用 set() 而不是 { }，因为 { } 是用来创建一个空字典。
#### 字典(Dictionary)
- 字典是一种映射类型，字典用 { } 标识，它是一个无序的 键(key) : 值(value) 的集合
- 键(key)必须使用不可变类型。
- 在同一个字典中，键(key)必须是唯一的
#### 数据类型转换
- 隐式类型转换(较低数据类型
  - （整数）就会转换为较高数据类型（浮点数）以避免数据丢失)
  - 整型和字符串类型运算结果会报错，输出 TypeError,无法隐式转换
- 显式类型转换
  - int(x [,base]) 将x转换为一个整数
  - float(x) 将x转换到一个浮点数
  - complex(real [,imag]) 创建一个复数
  - str(x) 将对象 x 转换为字符串
  - repr(x) 将对象 x 转换为表达式字符串
  - eval(str) 用来计算在字符串中的有效Python表达式,并返回一个对象
  - tuple(s) 将序列 s 转换为一个元组
  - list(s) 将序列 s 转换为一个列表
  - set(s) 转换为可变集合
  - dict(d) 创建一个字典。d 必须是一个 (key, value)元组序列。
  - frozenset(s) 转换为不可变集合
  - chr(x) 将一个整数转换为一个字符
  - ord(x) 将一个字符转换为它的整数值
  - hex(x) 将一个整数转换为一个十六进制字符串
  - oct(x) 将一个整数转换为一个八进制字符串

#### 推导式
- 列表(list)推导式
  - [表达式 for 变量 in 列表] [out_exp_res for out_exp in input_list]
  - [表达式 for 变量 in 列表 if 条件] [out_exp_res for out_exp in input_list if condition]
- 字典(dict)推导式
  - { key_expr: value_expr for value in collection }
  - { key_expr: value_expr for value in collection if condition }
- 集合(set)推导式
  - { expression for item in Sequence }
  - { expression for item in Sequence if conditional }
- 元组(tuple)推导式
  - (expression for item in Sequence )
  - (expression for item in Sequence if conditional )

### 注释
#### 单行注释
- 以 # 开头
#### 多行注释
- 单引号（'''）
- 双引号（"""）

### 运算符

- 算术运算符
- 比较运算符
- 赋值运算符
- 逻辑运算符
- 位运算符
- 成员运算符
- 身份运算符
- 运算符优先级

### 函数
#### 条件控制
- if语句 if cd: elif cd: else:

#### 循环语句
- while循环 while 判断条件: else:
- for语句 for [var] in [seq]:[] else:[]
  - for i in range(5):
  - break continue
  - pass  占位语句,保持程序结构的完整性

#### 迭代器和生成器
- 迭代器 iter() next()
- 生成器 yield

#### 函数
##### 定义一个函数
- def 关键词开头，后接函数标识符名称和圆括号 ()
- 任何传入参数和自变量必须放在圆括号中间，圆括号之间可以用于定义参数
- 函数内容以冒号 : 起始，并且缩进
- return [表达式] 结束函数，选择性地返回一个值给调用方，不带表达式的 return 相当于返回 None
##### 参数传递
- strings, tuples, 和 numbers 是不可更改的对象，而 list,dict 等则是可以修改的对象
- 不可变类型：类似 C++ 的值传递，如整数、字符串、元组。如 fun(a)，传递的只是 a 的值，没有影响 a 对象本身。如果在 fun(a) 内部修改 a 的值，则是新生成一个 a 的对象。
- 可变类型：类似 C++ 的引用传递，如 列表，字典。如 fun(la)，则是将 la 真正的传过去，修改后 fun 外部的 la 也会受影响
- python 中一切都是对象，严格意义我们不能说值传递还是引用传递，我们应该说传不可变对象和传可变对象
- 关键字参数 printme( str = "菜鸟教程")
- 默认参数 def printinfo( name, age = 35 )
- 不定长参数 def functionname([formal_args,] *var_args_tuple ): 加了星号 * 的参数会以元组(tuple)的形式导入，存放所有未命名的变量参数
##### 匿名函数
- lambda [arg1 [,arg2,.....argn]]:expression

##### 强制位置参数
- Python3.8 新增了一个函数形参语法 / 用来指明函数形参必须使用指定位置参数，不能使用关键字参数的形式

### 模块
- import 语句 import module1[, module2[,... moduleN]
- from modname import name1[, name2[, ... nameN]]
- from … import * 语句
- __name__属性 每个模块都有一个__name__属性，当其值是'__main__'时，表明该模块自身在运行，否则是被引入
- dir() 函数 内置的函数 dir() 可以找到模块内定义的所有名称。以一个字符串列表的形式返回

### 输入和输出
  - write()
  - print()
  - 读取键盘输入input()

### 文件系统
- open()打开一个文件，并返回文件对象,注意调用close()
- file对象
  - file.close() 关闭文件
  - file.flush() 刷新文件内部缓冲，直接把内部缓冲区的数据立刻写入文件, 而不是被动的等待输出缓冲区写入
  - file.fileno() 返回一个整型的文件描述符
- OS文件/目录
  - os.access() 检验权限模式
  - os.mkdir(path[, mode]) 以数字mode的mode创建一个名为path的文件夹.默认的 mode 是 0777 (八进制)。

### 错误和异常
- 语法错误 解析错(语法分析器指出了出错的一行)
#### 异常
- 运行期检测到的错误被称为异常
- 异常处理 try/except try/except...else try-finally raise [Exception [, args [, traceback]]]
- 用户自定义异常
- 
### 面向对象
#!/usr/bin/python3
class Parent:        # 定义父类
  def myMethod(self):
      print ('调用父类方法')

class Child(Parent): # 定义子类
  def myMethod(self):
      print ('调用子类方法')

c = Child()          # 子类实例
c.myMethod()         # 子类调用重写方法
super(Child,c).myMethod() #用子类对象调用父类已被覆盖的方法

### 命名空间和作用域

### 标准库概览
#### 操作系统接口 os
#### 文件通配符 glob
#### 命令行参数 sys
#### 错误输出重定向和程序终止 sys
- sys 还有 stdin，stdout 和 stderr 属性，即使在 stdout 被重定向时，后者也可以用于显示警告和错误信息。
#### 字符串正则匹配 re
#### 数学 math
#### 访问 互联网 smtplib
#### 日期和时间 date
#### 数据压缩 zlib
#### 性能度量 Timer
#### 测试模块 unittest

## 进阶知识
### 正则表达式
### CGI编程
### MySQL
### 网络编程
### SMTP发送邮件
### 多线程
### XML解析
### JSON
### 日期和时间
### 内置函数
### MongoDB
### urllib
### uWSGI 安装配置
### pip 
### operator
### math
### requests
### random


## OpenCV