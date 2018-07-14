# 		Java自学笔记

## 一、Java语言概述

### 1.Java的特点

​	1.平台无关性

​	2.面对对象

​		（1）封装

​		（2）继承

​		（3）多态

​	3.多线程

​	4.安全

​	5.动态

### 2.Java程序开发

​	一个Java应用程序必须有一个类含有public static void main(String args[])方法。这个类称应用程序的主类。args[]是main方法的一个参数，是一个字符串类型的数组。

​	源文件的命名规则：

​	（1）如果源文件中有多个类，那么只能有一个类是public类。

​	（2）如果有一个类是public类，那么源文件的名字必须与这个类的名字完全相同，拓展名为  .java

​	（3）如果源文件没有public类，那么源文件的名字只要与某个类的名字相同，并且拓展名是 .java 就可以了

Java语言是区分大小写的。

## 二、基本数据类型和数组

### 1.标识符和关键字

#### 	1.标识符

​	Java语言规定标识符由字母、下划线、美元符号和数字组成，并且第一个字符不能是数字。

​	（1）长度不受限制

​	（2）第一个字符不能是数字

​	（3）标识符不能是关键字

​	（4）标识符不能是true、false、和null

​	（5）标识符中的字母是区分大小写的

#### 	2.关键字

​	关键字就是Java语言中已经被赋予特定意义的一些单词，它们在程序上有着不同的用途，不可以把关键字作为			  名字来用。以下是Java的50个关键字：

abstract    assert   boolean   break   byte   case   catch   char   class   const   continue   default   do   double   else  enum   extends   final   finally   float   for   goto   if   implements   import   instanceof   int   interface   long   native   new  package   private   protected   public   return   short   static   strictfp   super   switch   synchronized    this   throw   throws   transient     

try   void   volatile   while

### 2.基本数据类型

​	也称简单数据数据类型，Java语言有8种简单数据类型：boolean，byte，short，int，long，float，double，char。这8种数据类型习惯上被分为四大类型：

​	（1）逻辑类型：boolean

​	（2）字符类型：char

​	（3）整数类型：byte，short，int，long

​	（4）浮点类型：float，double

转义字符：   \n（换行）        \b（退格）        \t（水平制表）           \\' （单引号）      \\"（双引号）

### 3.基本数据类型的转换

​	下列基本类型会涉及数据转换，不包括逻辑类型和字符类型。将这些类型按精度从低到高排列了顺序：

​	byte	<	short <	int	<	long  <	float  <	double.

当把级别低的变量的值付给级别较高的的变量时，系统自动完成数据类型的转换，如

​		float x=100;输出x的值，结果是100.0

当把级别高的变量的值付给级别较低的变量时，必须使用显示类型转换运算（强制类型转换）。格式如下：

​	（类型名） 要转换的值；

​	例如：int  x=（int）34.89，如果输出x的值将是34.

当把一个整数赋值给一个byte、short、int或者long类型变量时，不可以超出这些变量的取值范围，否则必须进行类型转换运算。例如：

​	byte a=(byte)128;  那么a的值就是-128

### 4.数据的输入和输出

#### 	1.数据输出System.out.printf

​	System.out.printf的功能完全类似C语言中的printf函数，其一般格式如下：

​		printf（格式控制部分，表达式1，表达式2，...，表达式n）;

​	（1）%md——输出的int类型数据占m列；

​	（2）%m.nf——输出的float类型数据占m列，小数点保留n位；

​	（3）Java提倡用%n表示回行

#### 2.数据的输入Scanner

​	Scanner实在JDK1.5新增的一个类（在java.util包中），可以使用该类创建一个对象：

​		Scanner reader  =   Scanner（System . in）；

然后reader对象调用下列方法（函数），读取用户在命令行输入的各类数据：

​		nextByte(),  nextDouble(),  nextFloat(),  nextInt(),  nextLine(),  nextLong(),  nextShort()

上述方法执行时都会堵塞，等待用户在命令行输入数据回车确认。

例:           import java.util.*;

​		public class Example{

​			public static void main(String args[])

​			{

​				Scanner reader = new Scanner(System.in);

​				double sum= 0;

​				int m=0;	

​				while(redaer.hasNextDouble())

​				{

​					double x=reader.nextDouble();

​					m+=1;

​					sum+=x;

​				}

​				System.out.printf("%d个数的和为：%f\n",m,sum);

​				System.out.printf("%d个数的均值为：%f\n",m,sum/m);

​			}

​		}

### 5.数组

​	与C语言不同的是，Java允许使用int类型变量指定数组的大小。例如：

​			int  size = 30;

​			double num[] = new double[size];

​	与C/C++语言不同，Java不允许在声明数组中

## 三、运算符、表达式和语句

## 四、类和对象

## 五、继承、接口和泛型

## 六、字符串和正则表达式

## 七、常用实用类

## 八、线程

## 九、输入流和输出流

## 十、图形用户界面设计

## 十一、Java中的网络编程

## 十二、Java数据库操作

## 十三、Java Applet

