**我的学习笔记[tj]**
================
`记录我的学习过程，好记性不如烂笔头`

在之前的工作学习中，我发现一些基本的常用知识一段时间没用，会忘记，虽然我们可以百度，但是上面搜出来的内容五花八门，想到这里，我从这里入手，想着整理一下，方便自己，同时也希望对其他人提供一点小小的帮助。@。@  


**目录**
 
+ [java](#java)
	+ [java基础](#java基础)
	+ [java容器](#java容器) 
	+ [io流](#io流)
	+  [线程](#线程)
	+ [反射](#反射)
	+ [servlet](#servlet)
	+ [框架](#框架)
	+ [服务器tomcat](#服务器tomcat)
	+ [idea编程工具相关](#idea编程工具相关)

+ [python](#python)

+ [前端](#前端)

+ [数据库知识](#数据库知识)

+ [Linux](#linux)



**java**
====
### java基础
1.很多代码中涉及到金额等需要精确度的数据时，我们可以使用math中的BigDecimal去处理，它是一个对象，不能进行传统的+-*%，有自己的计算[点我看百度百科](https://baike.baidu.com/item/BigDecimal/5131707?fr=aladdin)
	 我之前有一个错误，在进行了计算之后，记得用对象去接受计算后的结果，和a+=b一样，不要换了一种方式就错乱了。
		2.在做分页的时候，用PageHelper，遇到一个问题，明明代码没有任何问题，但是分页会出错，才发现，是使用PageHelper的时候，当调用PageHelper.offsetPage(paging.getStart(), paging.getLimit())方法的时候，会对紧跟的一个sql起作用，所以涉及到其他的业务室，需要做好处理。
### java容器
java容器相关的内容
### io流
io流相关的内容
### 线程
线程相关的内容
### 反射
反射相关的内容
### servlet
相关的内容
### 框架
框架相关的内容
### 服务器（tomcat）
tomcat服务器相关的内容
### idea编程工具相关
1.使用eclipse的时候我们打包，可能大家都会，导出，选择需要导出的文件类型，就可以了。之后在使用idea的时候，当一个工程里面引用其他工程的类以及方法，打包总是失败，需要在被引用的工程中在maven的操作中点击install，之后再需要打包的工程中点击package，会在你配置的路径中打成一个war包，一般默认的是在项目的target目录下面。
## python
python相关内容

## 前端
前端相关内容

## 数据库知识
orcale：
	1.在使用orcale的时候数据的操作是一些和金钱等一些带有小数的数据时，会去掉小数点之前的0（比如0.01，得到.01），处理这个问题：to_char(小数，'fm999990.99')
	2.由于我之前使用的是mysql数据库，mysql数据库有一个可以自增的特性，在之后使用orcale时，没有这个特性，造成数据的插入无法得到一个主键索引，我们需要手动的自己添加，方式如下：Create Sequence SEQ_`表名`Increment By 1 Start With 1 Minvalue 1 Nomaxvalue Cache 50 Noorder Nocycle;
	
## Linux
1.tail -fn 行数 日志文件名，可以自动刷新日志，在进行问题查找时方便。