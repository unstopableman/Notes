---
typora-root-url: pic
---

# 昨日回顾

## 数据类型

​	byte	short	char—>int—>long—>float—>double	boolean不能转换

​	强制转换：由大范围到小范围，会有精度损失

## 进制

​	二进制

​	八进制

​	十六进制

​	十进制

## 运算符

​	算术运算符

​	+	- 	*	/	%	++	--

```
	public static  void  main(String[] args){
		int i = 10;
		i = i++;
		System.out.println(i);
		i = ++i;
		System.out.println(i);
	}
```

​		上述代码中，特殊性情况，应避免此种用法。

​		***在一条语句中，应尽量避免对同一变量的多次运算操作。***

​	赋值运算符

​	=	+=	-=	*=	/=	%=

​		这几种运算符在进行运算时，会进行数据类型的强制转换。

​		

```
 byte b = 20;
		 	byte sum = 0  ;
		 // sum = b + 1;//编译不通过  因为用int到byte 会有精度损失 
	
			sum += 1; //编译通过 正常运行 其中会默认进行强制类型转换
```

​	逻辑运算符

​	&	|	！	&&	||	^



​	比较运算符

​	位运算

![img](/../assets/clipboard-1572419188212.png)



​		位运算	是针对二进制数据中的每一位进行运算。

![img](/../assets/clipboard-1572419333347.png)

​		>>>	无符号右移，也叫逻辑右移

​		位运算效率最高：位运算是对机器码二进制进行操作。

#### 面试题：使用最高效的算法计算2的三次方

​	计算2 的n次方	2<<(n-1)



​	三元运算符（三目运算符）

​	结构	关系运算？结果1 ： 结果2;

​	

```
int a = 4;
	 int b = 8;
	 int c = a > b ? a : b;
	System.out.println(c);
	String s = a > b ? "大于" : "小于";
	System.out.println(s);
```

​	三元运算符通常可以转换为 if 	else



例：获取三个数中的最大数

```
public static  void  main(String[] args){
	 int a = 6;
	 int b = 2;
	 int c = 9 ;

	 int d = (a > b ?a : b ) > c ?(a > b ?a : b ) :c;
	 System.out.println(d);
	}
```



例：不使用中间变量 交换两个整型变量的值

```
// 不使用中间变量 交换两个整型变量的值  方式一
		int a = 6;
		int b = 2 ;
		a = a + b; // a = 8;
		b= a- b; // b = 6;
		a = a - b ;
		System.out.println(a +"---"+b);
```

```
 // 不使用中间变量 交换两个整型变量的值  方式二
		int a = 6;//0000 0110
		int b = 2;//0000 0010
		a = a ^ b;//0000 0100
		b = a ^ b;//0000 0110
		a = a ^ b;//0000 0010

		System.out.println(a +"---"+b);
```

​	运算符的优先级		

- 优先级就是表达式运算中的运算顺序：从高到低。

- 只有单目运算符、三目运算符、赋值运算符是从右往左运算的。

​	 

![img](/../assets/clipboard-1572421445742.png)



# 一、流程控制

​	

流程控制语句是用来控制程序中各语句执行顺序的语句，可以把语句组合成能完成一定功能的小逻辑模块。 

## 1.	三种基本流程结构 

### 1.1.1顺序结构

自上而下，逐句执行。

java中定义成员变量时采用合法的前向引用，如：

```
int a  = 20;
		int sum = 0 ;
		int b =2;//正确顺序
		sum = a + b;
		//int b =2;//错误  编译不通过
		System.out.println(sum);

```

### 1.1.2分支结构

- 根据条件，选择性地执行某段代码。 
- 有if…else和switch-case两种分支语句。

![img](/../assets/clipboard-1572422477811.png)

![img](/../assets/clipboard-1572422493959.png)



### 1.1.3循环结构

- 根据循环条件，重复性的执行某段代码。 
- 有while、do…while、for三种循环语句。 
- 注：JDK1.5提供了foreach循环，方便的遍历集合、数组元素。



## 二、详细及相关代码

## 1.概念

​	表达式：将数据  变量 使用运算符 按照一定的规则拼接起来  形成的就是表达式 。

​	表达式类型：表达式计算之后结果的类型

```
 int age = 23;
		 //假定人的年龄的合法值位0---100 
		 if(age > 0 && age < 100)
			System.out.println("年龄合法");
		 else
			System.out.println("年龄不合法");
```

如果if  else其后有且只有一条需要执行的语句，则if  else后的大括号可以省略 。但是仅限于其后有且仅有一条语句 。



## 2.相关代码

```
import java.util.Scanner;
public class Demo1{
	/*
		岳大鹏参加Java考试，他和父亲岳不群达成承诺： 
		如果： 成绩为100分时，奖励一辆BMW； 
		成绩为(80，99]时，奖励一台iphoe xs max； 
		当成绩为[60,80]时，奖励一个 iPad； 
		其它时，什么奖励也没有。 
		请从键盘输入岳小鹏的期末成绩，并加以判断
	*/
	public static void main(String[] args) {
		 Scanner sc = new Scanner(System.in);
		 System.out.println("请输入您的Java考试成绩：");
		 int score = sc.nextInt();
		 if(score < 0  ||  score > 100 100){
			 System.out.println("输入的成绩不合法，请查证后重新输入。。。。");
		 }else{
			if(score == 100 ){
				 System.out.println("奖励一辆BMW");
			}else if(score > 80 && score <= 99){
				System.out.println("奖励一台iphoe xs max");
			}else if(score >= 60 && score <= 80){
				System.out.println("奖励一台iPad");
			}else{
				System.out.println("无奖励");
			}	
		 }
	}
}
```



```
import java.util.Scanner;
public class Demo1{
	/*
		编写程序：由键盘输入三个整数分别存入变量num1、num2、num3， 
		对它们进行排序(使用 if-else if-else),并且从小到大输出。
	*/
	public static void main(String[] args) {
		 Scanner sc = new Scanner(System.in);
		 System.out.println("请输入第一个整数：");
		 int num1 = sc.nextInt();

		System.out.println("请输入第二个整数：");
		 int num2 = sc.nextInt();

		System.out.println("请输入第三个整数：");
		 int num3 = sc.nextInt();
		// 将第一个数和第二数进行比较  对他们进行交换位置 将较小者放在第一位  较大者放在第二位

		// 在用第三个数和第二个数进行比较  交换位置

		// 此时比较第一个和第二个数 

		if(num1 > num2){
			int temp = 0 ;
			temp = num1;
			num1 = num2;
			num2 = temp;
		}
		if(num2  > num3){
			int temp = 0 ;
			temp = num2;
			num2 = num3;
			num3 = temp;
		}
		if(num1 > num2){
			int temp = 0 ;
			temp = num1;
			num1 = num2;
			num2 = temp;
		}
		System.out.println(num1 +"---"+ num2+"---"+num3);
	}
}
```



```
import java.util.Scanner;
public class Demo1{
	/*
		我家的狗5岁了，5岁的狗相当于人类多大呢？其实，狗的前两年每 一年相当于人类的10.5岁，
		之后每增加一年就增加四岁。那么5岁的狗 相当于人类多少年龄呢？
		应该是：10.5 + 10.5 + 4 + 4 + 4 = 33岁。 
		编写一个程序，获取用户输入的狗的年龄，通过程序显示其相当于人 类的年龄。
		如果用户输入负数，请显示一个提示信息。
	*/
	public static void main(String[] args) {
		 Scanner sc = new Scanner(System.in);
		 System.out.println("请输入狗的年龄整数：");
		 double dogAge = sc.nextDouble();
		 if(dogAge > 0){
			 if(dogAge <= 2 ){
				dogAge *= 10.5;
			}else{
				dogAge = (dogAge-2) * 4 + 2 * 10.5;
			}
			System.out.println(dogAge);
		 }else{
		 System.out.println("狗的年龄不能为负数：");
		 }
		
	}
}
```

