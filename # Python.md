# Python

*****
## 心得
### 善于利用len()//比如在循环中等，十分好用
*****
*****
## 基础语法
### input()
#### 就是输入，然后里面可以加文字的，不影响程序运行               

```
temp = input("请输入一个数字：")
```
*****
### 字符串拼接
#### 直接用+号可以连接两个字符串
*****
### 字母大小写是完'全不同两个变量
### 字符串可用''和""都可
### 多行字符串可用"""引号括起来
*****
### 重点                            （'let's go'）(错误)                此时需要\把'进行转义，从而进行正常输出Let|'s go
*****
### 原始字符串        原始字符串是Python中一类比较特殊的字符串，以大写字母R或者小写字母r开始。在原始字符串中，字符“\” 不再表示转义字符的含义。（主要用来方便表示Windows系统下的路径）           比如：直接print一个（C:\now）\会和n合在一起，从而不能正确输出这一内容，如在输出语句分号前加个   R或者r即可解决这一问题
*****
### if else       万能哒                不同的是if else 后面要跟个：
*****
### s 为字符串

#### s.isalnum()  所有字符都是数字或者字母，为真返回 True，否则返回 False。

#### s.isalpha()   所有字符都是字母，为真返回 True，否则返回 False。

#### s.isdigit()     所有字符都是数字，为真返回 True，否则返回 False。

#### s.islower()    所有字符都是小写，为真返回 True，否则返回 False。

#### s.isupper()   所有字符都是大写，为真返回 True，否则返回 False。

#### s.istitle()      所有单词都是首字母大写，为真返回 True，否则返回 False。

#### s.isspace()   所有字符都是空白字符，为真返回 True，否则返回 False。
         
```
例如：
>>> s = 'I LOVE FISHC'
>>> s.isupper()
>>> True
         
例如：
>>> s = 'I LOVE FISHC'
>>> s.isupper()
>>> True
```
### random模块
#### randint()   Ta会返回一个int整数的随机数
```
import random
//import 就是让random模块包含进入这个函数里面
secet = random.randint(1,10)
```
### type()
#### 判断数据类型
### isinstance()
```
a='xd'
isinstance(a,str)
返回值为true
```
### 本质上也是判断类型。
*****
### 算术操作符
#### 3**2=9
#### // 是做取舍的除法
#### /是真实的，带小数的
*****
### 优先级          (幂运算**> 正负号>算术操作符>比较操作符>逻辑运算符)
#### 单目运算符的左侧单目运算符是比它本身的优先级高的   另一侧相反
*****
### 逻辑操作符
#### and 并且
#### or 或者
#### not not 0 = true
*****
### 分支与循环
*****
### 三元操作符（有多少操作数）
```
small = x if (x < y and x < z) else (y if y < z else z)
```
### assert(自爆语句)
#### 如果错误程序直接自爆\
##### assert：断言格式：
##### assert 表达式 [, 参数]
##### 当表达式为真时，程序继续往下执行；
##### 当表达式为假时，抛出AssertionError错误，并将  参数  输出
##### assert这个关键字我们称之为“断言”，当这个关键字后边的条件为假的时候，程序自动崩溃并抛出AssertionError的异常。当我们在测试程序的时候就很好用，因为与其让错误的条件导致程序今后莫名其妙地崩溃，不如在错误条件出现的那一瞬间我们实现“自爆”。一般来说我们可以用Ta再程序中置入检查点，当需要确保程序中的某个条件一定为真才能让程序正常工作的话，assert关键字就非常有用了。
```
```
//快速将三个变量的值互相交换
  x, y, z = z, y, x
```
语法格式如下：

assert expression
等价于：

if not expression:
    raise AssertionError
assert 后面也可以紧跟参数:

assert expression [, arguments]
等价于：

if not expression:
    raise AssertionError(arguments)
```
### 成员资格运算符(成员资格运算符：in，用于检查一个值是否在序列中，如果在序列中返回 True，否则返回 False。)
```
>>> name = '金鱼'
>>> '鱼' in name
True
>>> '黑鱼' in name
False
```
*****
### range()
#### range(5)       和FOR循环共同使用，为循环几次
```
range(stop)
range(start, stop[, step])
/*start: 计数从 start 开始。默认是从 0 开始。例如range（5）等价于range（0， 5）;
stop: 计数到 stop 结束，但不包括 stop。例如：range（0， 5） 是[0, 1, 2, 3, 4]没有5
step：步长，默认为1。例如：range（0， 5） 等价于 range(0, 5, 1)*/
```
### 循环语句        for...in...
```
 
for letter in 'Python':     # 第一个实例
   print("当前字母: %s" % letter)
 
fruits = ['banana', 'apple',  'mango']
for fruit in fruits:        # 第二个实例
   print ('当前水果: %s'% fruit)

for循环一行两个元素输出的方法
方法一：
count = 0
length = len(member)
while count < length:
    print(member[count], member[count+1])
    count += 2

方法二：    
    
for each in range(len(member)):
    if each%2 == 0:
        print(member[each], member[each+1])

list1 = [x**2 for x in range(10)]
list1
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

list1 = []
for x in range(10):
    list1.append(x**2)
```
*****
*****
## 列表
### 普通列表
#### member['A','s'....]
### 混合列表
#### mix['可以'，'a','1','[1234]']
### 空列biao
```
 empty[]
```
### 向列表(插入)
#### 对象.方法
##### append
```
mix.append('aaa')//只能添加一个，参数是元素
```
##### extend
```
mix.extend(['222','123'])
//因为是往里面加大于一个的数据，所以就相当于延长列表长度，所以加入的应该是一个完整的列表。
```
##### insert (可以排在任意的位置)
```
mix.insert(1,'abc')
```
### 从列表中索引获取一个元素（从零开始）
#### mix[1-...]
### 删除元素用
#### remove
```
 mix.remove('a')
 ```
 #### del(delete)
 ```
 del member[1-...]
 ```
#### pop(删除最后一个元素)
```
member.pop(1)
```
### 列表分片
```
member[1:3]（）
//3不包括    分出mumber中第一个第二个元素使其成为一个新列表
member[:3]// 从零开始到二结束
member[:]// 从头到尾（可用来复制一个列表）

1 之前提到的“简洁”分片操作在这里有效：
>>> list1[::2]
[1, 2, 7]


2 步长不能为0，要不就走不动了：
>>> list1[::0]
Traceback (most recent call last):
  File "<pyshell#11>", line 1, in <module>
    list1[::0]
ValueError: slice step cannot be zero


3 步长可以是负数，改变方向（从尾部开始向左走）：
>>> list1[::-2]
[8, 9, 3]



```
### 列表的一些常用操作符
#### 比较操作符
```
list1=[122,456]
list2=[234,123]
list1>list2
false
//只比较第一个元素，后面就不看了
```
#### 逻辑操作符（也是只比较第一个元素）
```
'122' not in list1
False

'122' in list1
True

'122' in list1[0]
True

//提取列表中的列表
list[1][1]
//提取第一个元素中的第一个元素
```
#### 连接操作符
```
list4 = list1 + list2
//只能列表加列表
```
#### 重复操作符
```
list1*=3
```
### 列表中的其他
#### count
```
list.count(122)
返回值为1//意为出现一次
```
#### index
```
list1.index(122)
0

//查找列表中重复的数据
list(122,3,7)
从第四个元素开始到第八个元素
第一个出现122这一个元素的位置

```
#### reverse（反转）
```
list1.reverse()
list1
[456,122]
//类似C中的数组的反序
```
#### sort
```
list3=[4,2,6,3,44]
list3.sort()
返回list=[2,3,4,6,44]
//与reverse 可搭配变为从大到小排
list3.sort(reverse=True)
```
#### *重要的一些区别*
##### copy的两种用法
```
list4=list6   （一）
list5=list6(:)  （二）
// 第一种方法当list6改变以后，4会跟着改变
// 而第二种方法是copy其中的元素，6改变，5不会跟着变
```
### 总结
```
append()
按特定的顺序排序（从小到大)
extend()
寻找并返回参数的索引值
count()
拷贝一个副本
remove()
原地翻转所有的数据
pop()
在最后增加一个元素
sort()
清空所有元素
insert()
删除一个元素
copy()
扩展列表（用另一个列表)
clear()
计算并返回指定元素的数量
reverse()
在指定位置插入一个元素
index()
删除并返回最后一个元素
```

*****
*****
## 元组
### 元组与列表区别
#### 元组与列表相同，也是容器对象，可以存储不同类型的内容。元组与列表有两个不同点。第一个不同点是元组的声明使用小括号，而列表使用方括号，当声明只有一个元素的元组时，需要在这个元素的后面添加英文逗号；第二个不同点是元组声明和赋值后，不能像列表一样添加、删除和修改元素，也就是说元组在程序运行过程中不能被修改。     用于列表的排序、替换、添加等方法也不适用于元组，适用于元组的主要运算有元组的合并、遍历、求元组的最大值和最小值等操作方法。
### 元组的创建
```
tuple1 = (1,2,3,4,5,6,7,8)
//注意是小括号，逗号是关键
```
### 更新和添加元组
```
temp = ('皮', '杀','是')
temp = temp[:1] + ('牛的') + temp[1:]
```
*****
### 字符串
####  capitalize(把字符串的第一个字符改为大写)
```
list1 = 'xiaoxie'
list1.capitalize 
Xiaoxie
```
#### casefold(全变为小写，注意是返回一个新的字符串，原本的还是那样)
```
list1 = 'XIAOXIE'
list1.casefold
xiaoxie
```
#### center(width)
```
list1 = 'xiaoxie'
list1.center(40)
返回值：'           xiaoxie             '
```
#### count(sub[,start[,end]])
```
list1.count('xi')
返回值：2
```
#### encode(encoding=)
(zanding)
#### endswith(sub[,start[,end]]) //检查结尾是否为该字符，返回True False
```
list1.endwith('xi')
返回值：false
```
#### expandtabs([tabsize=8]) // 将字符串的tab符号（\t）变为空格，默认为八个字节一个循环
```
list1 = ' x\tiaoxie\t'
list1.expandtabs()
'x       (七个空格)iaoxie(两个空格)'

```
#### find(sub[,start[,end]])(检测sub是否在字符串中，如果在则返回索引值，否则返回-1)
```
list.find('xie')
返回值：4
```
####  isdecimal()//如果字符串只包含十进制数字则返回True,否则返回False
#### isspace()//如果字符串中只包含空格，则返回true,否则返回False
#### istitle()//如果字符串均已大写开头小写字母，则返回true,else False
#### isupper()//如果有大写字母的小写字符串，返回true,else False
#### lstrip()//去掉字符串左边的空格
#### partition(sub)//找到子字符串sub,把字符串分成一个三元组（pre_sub,sub,fol_sub）
#### replace(old,new[,count])//把字符串中的old子字符串换成new字符串，如果count指定，则替换不超过 count
#### rfind(sub[,start[,end]])(检测sub是否在字符串中，如果在则返回索引值，否则返回-1)//同find一样，但是是从右往左find
#### rindex(sub[,start[,end]]) //从右边开始的index
#### rjust(width)//返回一个右对齐的字符串，并使用空格填充至长度为width的新字符串
#### rpartition(sub)//类似于partition(),不过从右边开始查找
#### rstrip()//删除字符串末尾的空格
#### split(sep=None,maxsplit=-1)//不带参数默认是以空格为分隔符切片字符串，如果maxsplit参数有设置，则仅分隔maxsplit个子字符串，返回切片后的子字符串拼接的列表。
#### splitlines((lkeepends]))//按照‘1n’分隔，返回一个包含各行作为元素的列表，如果keepends参数指定，则返回前keepends行。
#### startswith(prefix[,start[,end]]) //检查字符串是否以prefix开头，是则返回True，否则返回False。**start和**end参数可以指定范围检查，可选。
#### strip([chars])//删除字符串前边和后边所有的空格，chars参数可以定制删除的字符，可选。
#### swapcase0 翻转字符串中的大小写。
#### title()//返回标题化(所有的单词都是以大写开始，其余字母均小写)的字符串。
#### translate(table)//根据table的规则（可以由str.maketrans( 'a’ , ‘b’)定制）转换字符串中的字符。
#### upper) //转换字符串中的所有小写字符为大写。
#### zfill(width)//返回长度为width的字符串，原字符串右对齐，前边用0填充。
*****
## 序列
### 1.列表、元组和字符串的共同点-都可以通过索引得到每一个元素一默认索引值总是从0begin2.一可以通过分片的方法得到一个范围内的元素的集合一3.有很多共同的操作符（(重复操作符、拼接操作符、成员关系操作符）
#### list([iterable]) 把可迭代对象转换为列表
#### tuple([iterable]) 把可迭代对象转换为元组
#### str(obj)  把对象转换为字符串
补十六章节笔记（3.2）
