<!--/*10.27*/-->

## java语言概述



java之父——James Gosling

### 一、java基础知识图解

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-KtB3Zmzf-1572192537277)(C:\Users\dell\Pictures\Saved Pictures\java3.png)]



### 二、软件开发介绍

#### 1.软件开发

​	软件，即一系列按照特定顺序组织的计算机数据和指令的集合。有系统软件和应用软件之分。

#### 2.人机交互方式

（1）图形化界面(Graphical User Interface GUI)	：这种方式简单直观，使用 者易于接受，容易上手操作。 

（2）命令行方式(Command Line Interface CLI)  ：需要有一个控制台，输 入特定的指令，让计算机完成一些操作。较为麻烦，需要记录住一些 命令。

#### 3.常用DOS命令

dir	：查看当前目录下的文件及目录

cd	：进入目录

​	相对路径：相对当前所在的目录进行目录查找

​	绝对路径：在windows系统下，就是带盘符的路径

cd..	：返回上级目录

cd/	：回到根目录

md  目录路径及名称	创建目录

​	    绝对路径

​	    相对路径

rd     删除目录（绝对路径/相对路径）

del 	删除文件 

echo javase>1.txt    将给定的内容写入指定的文件中（将“javase”写入1.txt，若没有则创建新文件1.txt）

exit  :  退出命令行窗口

#### 4.常用快捷键

​	

- ← →：移动光标
- ↑ ↓：调阅历史操作命令
- Delete和Backspace：删除字符

### 三、java语言主要特征

1.java语言是易学的

2.java语言是强制面向对象的。

3.分布式的。

4.健壮的。

5.安全的。

6.体系结构中立的。

7.解释型的。

8.性能略高的。

9.原生支持多线程的。

### 四、java语言的特点

- 面向对象
- 健壮性
- 跨平台性

### 五、java开发体验

#### 1.步骤一：编写

记事本敲入代码：

```
public class helloworld{
	public static void main(String args[]){
		System.out.println("hello world!");
	}
}
```

将文件保存为helloworld.java。（此为源文件）

#### 2.步骤二：编译

- [ ] “win键+R” 调出运行框，输入cmd，回车，调出命令行；
- [ ] DOS命令行中进入,java文件所在目录；
- [ ] 键入“javac helloworld.java”

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-NzlNFAeI-1572192537278)(C:\Users\dell\Pictures\Saved Pictures\java4.png)]



- [ ] 结果：产生helloworld.class文件[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-TAHdKf5C-1572192537278)(C:\Users\dell\Pictures\Saved Pictures\1572158381133.png)]

#### 3.步骤三：运行

- [ ] 有了可执行的java程序（.class字节码文件）
- [ ] 通过运行工具java.exe对字节码文件进行执行
- [ ] 结果：

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-zszJY143-1572192537279)(C:\Users\dell\Pictures\Saved Pictures\1572158854264.png)]

#### 注意事项：

- 当类前边有public修饰的时候 此时要求类名称必须和文件名保持完全一致 

- String后的参数可以任意定义

- 在代码中所使用的所有的表单符号，都必须是英文状态的符号

- 代码中的括号（大、中、小）必须成对出现

- 执行java指令时，直接写类名，而不是文件名。

- 当源文件被修改之后，必须重新编译。

- 主类：
  - 在一个.java文件中，使用public修饰的类，就称为主类。在一个 .java文件中，至少包含一个使用public修饰的类，并且只能有一个主类。
  - 在一个java文件中只能存在一个主类，其他类可以任意存在。
  - 编译后每一个类会生成一个class。

- java中注释

  作用：

  ​	对类、方法、语句、变量、常量等做一个解释，只是为了方便我们在阅读代码时能够快速的理解程序。

  种类：

  （1）// 单行注释：一般用在语句之后，常量、变量等，一般写在语句之后或者语句的上一行

  （2）多行注释/***/：

  ​	/*

  ​	* 多行注释一般用在需要进行详细说明，说明性的描述比较多的情况

  ​	*/

  ​	

  /**

  *称为文档注释，其中注释的内容可以在后期直接使用avadoc命令来生成当前类的帮助文档

  *可以用在类上，也可以用在方法上

  */ 

  

  ------

  ​	

  ​	以前写java用eclipse和Intellij IDEA，但是为了便于一步一步仔细理解java编程的原理和乐趣，之前使用记事本，现在安装EditPlus，这个高级记事本能更直观地感受java的原理。这里介绍一下EditPlus的配置。

### 六、配置EditPlus

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-5gpBAzKo-1572192537279)(C:\Users\dell\Pictures\Saved Pictures\ed.png)]





[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-AS24d9mx-1572192537280)(C:\Users\dell\Pictures\Saved Pictures\21209.png)]



[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-F1x71SHj-1572192537281)(C:\Users\dell\Pictures\Saved Pictures\21215.png)]





[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-koaRrWl9-1572192537281)(C:\Users\dell\Pictures\Saved Pictures\21212.png)]



[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-8IkRzsLl-1572192537282)(C:\Users\dell\Pictures\Saved Pictures\21213png)]



### 七、java的基本语法

##### 标识符

###### 	1.定义合法标识符规则： 	

- 由26个英文字母大小写，0-9 ，_或 $ 组成
- 数字不可以开头。
- 不可以使用关键字和保留字，但能包含关键字和保留字。
- Java中严格区分大小写，长度无限制。
- 标识符不能包含空格。

###### 2.Java中的名称命名规范： 

- 包名：多单词组成时所有字母都小写：xxxyyyzzz 以公司域名的逆序作为基础包名
- 类名、接口名：多单词组成时，所有单词的首字母大写：XxxYyyZzz
- 变量名、方法名：多单词组成时，第一个单词首字母小写，第二个单词开始每个 单词首字母大写：xxxYyyZzz
- 常量名：所有字母都大写。多单词时每个单词用下划线连接：XXX_YYY_ZZZ

###### 注意

>  注意1：在起名字时，为了提高阅读性，要尽量有意义，“见名知意”。 

>  注意2：java采用unicode字符集，因此标识符也可以使用汉字声明，但是不允许使用。

> 变量的概念：

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-9czjqYw7-1572192537283)(C:\Users\dell\Pictures\Saved Pictures\21222.png)]

- 内存中的一个存储区域
- 该区域的数据可以在同一类型范围内不断变化
- 变量是程序中最基本的存储单元。包含变量类型、变量名和存储的值

> 变量的作用： 用于在内存中保存数据

###### 3.使用变量注意： 

- Java中每个变量必须先声明，后使用
- 使用变量名来访问这块区域的数据
- 变量的作用域：其定义所在的一对{ }内
- 变量只有在其作用域内才有效
- 同一个作用域内，不能定义重名的变量

###### 4、声明变量 

> > 语法：<数据类型> <变量名称>

> > 例如：int var; 

###### 5、变量的赋值 

> >  语法：<变量名称> = <值>

> >  例如：var = 10; 

###### 6、声明和赋值变量 

> > 语法： <数据类型> <变量名> = <初始化值>

> > 对于声明在方法内的变量 必须在使用之前至少有一次赋值操作

​	

Java是强类型语言 ，意味着所有的变量都必须有一个明确的类型。

类型的作用就是决定变量在内存中分配的空间大小



###### 7.变量声明的位置：

局部变量：声明在方法上或方法内的变量

成员变量：声明在类的内部，方法外的变量

作用范围：

> 成员变量得作用范围是整个类  

> 局部变量的作用范围是整个方法内

初始化：

局部变量：在使用之前必须有一次赋值操作

成员变量：可以在使用之前不赋值   在于他有默认值

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-pRF6EK4l-1572192537284)(C:\Users\dell\Pictures\Saved Pictures\21224.png)]

> 8 基本数据类型

> 8.1整数类型：byte、short、int、long

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-RMIasngi-1572192537285)(C:\Users\dell\Pictures\Saved Pictures\21223.png)]

声明整型变量时  针对不同的类型 应进行合理赋值  不要超出期表示范围

对于long类型来说  数据末尾需要加L/l进行标记

浮点型

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-Fv9rUP0R-1572192537286)(C:\Users\dell\Pictures\Saved Pictures\21225.png)]

浮点型数据默认类型时double

如果使用float来表示浮点型数据 需要在数据的末尾加F/f

> 8.2字符类型：char

- char 型数据用来表示通常意义上“字符”(2字节)
- 字符在Java中采用单引号 使用双引号引起来的叫字符串
- 字符就是单个字母 或汉字 或数字
- 字符型变量的三种表现形式：

[外链图片转存失败,源站可能有防盗链机制,建议将图片保存下来直接上传(img-JUfmT5Vz-1572192537287)(C:\Users\dell\Pictures\Saved Pictures\21226.png)]

- 字符常量是用单引号(‘ ’)括起来的单个字符。例如：char c1 = 'a'; char c2 = '中'; char c3 = '9';
- Java中还允许使用转义字符‘\’来将其后的字符转变为特殊字符型常量。 例如：char c3 = ‘\n’; // '\n'表示换行符
- 直接使用 Unicode 值来表示字符型常量：‘\uXXXX’。其中，XXXX代表 一个十六进制整数。如：\u000a 表示 \n。

 

------

/*2019.10.27

*@author：秀才恶霸dxq

*java学习002

种表现形式：

[外链图片转存中...(img-JUfmT5Vz-1572192537287)]

- 字符常量是用单引号(‘ ’)括起来的单个字符。例如：char c1 = 'a'; char c2 = '中'; char c3 = '9';
- Java中还允许使用转义字符‘\’来将其后的字符转变为特殊字符型常量。 例如：char c3 = ‘\n’; // '\n'表示换行符
- 直接使用 Unicode 值来表示字符型常量：‘\uXXXX’。其中，XXXX代表 一个十六进制整数。如：\u000a 表示 \n。


## 附上三个代码及运行结果
1.HelloJava.java

```
public class HelloJava  {	//主类名
	public static void main(String[] args)	//String后面的参数（args）可以任意定义
	{
		System.out.println("Hello Java!");	//输出语句
	}
}

```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191028002728877.png)

2.Test.java
```
public class Test {

	static int b;
	public static void main(String[] args) {
		int a=10;
//		int b;	//局部变量必须赋值才能输出，否则报错
		boolean aa=true;
		System.out.println(a);
		System.out.println(b);
		System.out.println(aa);
	}
}

```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191028002705365.png)
3.Heart.java

```
public class Heart{
	public static void main(String[] args) {
		System.out.println("\t*\t\t\t\t\t\t\t\t\t\t\t\t*\n\n");	//第一行
		System.out.println("*\t\t\t*\t\t\tI Love Java  \t\t\t*\t\t\t*\n\n");
		System.out.println("\t*\t\t\t\t\t\t\t\t\t\t\t\t*\n\n");
		System.out.println("\t\t*\t\t\t\t\t\t\t\t\t\t*\n\n");
		System.out.println("\t\t\t*\t\t\t\t\t\t\t\t*\n\n");
		System.out.println("\t\t\t\t*\t\t\t\t\t\t*\n\n");
		System.out.println("\t\t\t\t\t*\t\t\t\t*\n\n");
		System.out.println("\t\t\t\t\t\t*\t\t*\n\n");
		System.out.println("\t\t\t\t\t\t\t*");
	}
}
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191028002637761.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

------------------------------------------------------------------------------------------------------------------------------------------------------------------

/*2019.10.27

*@author：秀才恶霸dxq

*java学习002

*/
