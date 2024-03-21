---
title: 输出语句
---

返回[**编程学习历程**](编程学习历程.md)

#print#

```python
{
	print ('Hello Python')#--->print的含义是输出括号内的内容
	print (value,…,sep='',end='\n',file=None)
	# value为需要输出的值    可以用','来输出多个
	# sep在输出结束后会自动换行  这是由end的'\n'决定的(暂时不是很懂'\n'的含义)
	# file决定了你可以把内容输出到文件当中
}

#记录Ascll码的对应数字：
	中文编码的范围是从<u4e00-u9fa5>
	暂时还不知道是什么作用，等知道了再补上
```

#chr# #ord#
[通过 Unicode 编码来确定 Ascll 编码的数值]:-

```python
#使用中文的Unicode编码来获取Ascll编码的对应数字来进行输出
{
	print(ord('久'))#--->对应下面的20037
	print(ord('影'))#--->对应下面的24433
	print(chr(20037),(chr(24433)))#通过,使其在同一行输出
}
```

#open#
[不指定绝对路径就会在当前目录创建]:-

```python
{
     jy=open("jy.txt","w") #--->"W指的是"write"，即写入模式
     print("Hello,I'm JY!",file=jy) #--->将文件打开，并写入内容
     jy.close()#--->关闭文件
}
```

#end#

```python
{
	 print('jiu',end='--->')
	 print('yingshi') # 因为没有修改end参数，所以默认"print"之后会换行
}
```

#input#

```python
{
	name=input('请输入你的姓名：') #--->定义一个输入语句为"name"
	print("你的姓名是："+ name) #--->输出反馈的"name"含义
}
```

#int#

```python
{
	num=input('请输入你的数字ID：')
	print("你的数字ID是："+ num) #--->此时的num为字符串类型
	num=int(num) #--->使用内置函数"int"将字符串类型转换为整数类型
	print('你的数字ID是：',num) #--->此时的num为整数类型
}
```

#注释#

```python
	# coding: utf-8
	#这个是中文声明注释
	#可以确保另存文件时的编码格式
	#他必须要写在文件的第一行
```

## #保留字#

> 指在 Python 中被赋予了特定意义的单词，开发程序时不建议把这些单词作为变量、函数、类、模块和其他对象的名称来使用。

|   and    |   as   | asert | break  |  class  | continue |  def   |
| :------: | :----: | :---: | :----: | :-----: | :------: | :----: |
|   del    |  elif  | else  | except | finally |   for    |  from  |
|  false   | global |  if   | import |   in    |    is    | lambda |
| nonlocal |  not   | None  |   or   |  pass   |  raise   | return |
|   try    |  true  | while |  with  |  yield  |  await   | async  |

```Python
{
	import keyword #--->'keyword'是Python的内置模块，用于检查是否为关键字。
	print(len(keyword.kwlist)) #--->'len()'打印关键字的数量。
	print(keyword.kwlist)
}
```

#type# #Python# 的性质

```Python
{
	luck_number=9 #--->'int'类型
	name='HS'#--->'str'类型
	print('luck_number的数据类型是:',type(luck_number)) #--->内置函数type()，检查输出数据的类型
	print(name,'的幸运数字是：',luck_number)
	luck_number='JiuYing'
	print('luck_number的数据类型是:',type(luck_number)) #--->通过这条输出信息，证明Python是动态修改变量的类型
}
```

#id# #Python# 允许多个变量指向同一值

```Python
{
	no=number=first=1
	print(no,number,first)
	print(id(no)) #--->通过内置函数'id()'查看对象的内存地址
	print(id(number)) #--->三个的内存地址都相同说明赋值的是同一个对象
	print(id(first))
}
```
