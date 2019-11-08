# 包

### 1.作用：就是为了将类进行分目录管理

​	包就是我们磁盘上的目录

### 2.命名规则

​	包名所有的字母都小写

​	包名采用公司域名的逆序



# 访问权限

![访问权限](assets/1573210183275.png)

对于class的权限修饰只可以用public和default（缺省）。

- public类可以在任意地方被访问
- default类只可以被同一个包内部的类访问

**访问修饰符** 定义了类的成员的访问的范围



# 面向对象的三大特征

​	封装	继承	多态

## 封装的广义

​	方法封装的体现。

​	类也属于封装

## 封装：

​	将成员属性私有化，同时对外提供公共的访问方法。

程序设计追求——高内聚、低耦合

- 高内聚 ：类的内部数据操作细节自己完成，不允许外部干涉；
	 低耦合：仅对外暴露少量的方法用于使用。	

## 构造方法

### 	作用：用来创建对象

### 	构造方法语法格式：

```
访问修饰符	此处无返回值（void也不写） 方法名就是类名(参数列表){
 
}
```

```
	/*
	 * jvm会帮助我们为每个定义的类提供一个构造方法  该方法没有参数  称为无参构造
	 */
	public Person() {
		System.out.println("构造方法执行");
	}
```

​	构造方法是在创建对象时 jvm帮助我们调用。

​	每创建一个对象就会调用一次构造方法。

​	当我们自己为一个类提供了构造方法  那么jvm将不再提供该类的无参构造 如果你需要使用无参构造 必须手动的自己将他显式的写出来。

构造方法的作用;

​	（1）创建对象

​	（2）完成对象的初始化（为成员属性赋值）

​	（3）为成员属性设置默认值

 构造方法的重载 

```
public Person() {
		System.out.println("构造方法执行");
	}
	public Person(String n) {
		name = n;
	}
	public Person(int a) {
		age = a;
	}
	public Person(String n ,int a) {
		name = n;
		age =a;
	}
```

this：表示当前对象

this写在方法中，所以将来那个对象调用该方法  那么this就代表那个对象

this区分同名的成员变量和局部变量

this可以调用本类的其他的重载的构造方法

**在构造方法中使用this调用其他构造方法  必须位于该构造方法的第一句**



**this调用构造方法  只能调用一次** 

```
public Person() {
		System.out.println("构造方法执行");
	}
	public Person(String name) {
		this.name = name;
		System.out.println(name);
	}
	public Person(int age) {
		this.age = age;
	}
	public Person(String name ,int age) {
		this(name);
		this.age = 18;
		
	}
```

this不仅可以用于构造方法中 也可以用于setter（）和getter（）方法中。 



# JavaBean

- JavaBean是一种Java语言写成的可重用组件。 

- 所谓javaBean，是指符合如下标准的Java类： 

- - 类是公共的
  - 有一个无参的公共的构造器 
  - 有属性，且有对应的get、set方法

标准的javaBean的写法 

```
/*
 * 类是公共的
	至少有一个无参的公共的构造器 
	有属性，且有对应的get、set方法
 */
public class Student {
	//成员属性
	private String stuNo;
	private String stuName;
	private int stuAge;
	
	//构造器
	//1 先写无参
	public Student() {
		
	}
	
	public Student(String stuName,int stuAge) {
		this.stuName = stuName;
		this.stuAge = stuAge;
	}
	public Student(String stuNo,String stuName,int stuAge) {
		this(stuName,stuAge);
		this.stuNo = stuNo;
	}
	public void setStuNo(String stuNo) {
		this.stuNo = stuNo;
	}
	public String getStuNo() {
		return this.stuNo;
	}
	public void setStuName(String stuName) {
		this.stuName = stuName;
	}
	public String getStuName() {
		return this.stuName;
	}
	public void setStuAge(int stuAge) {
		this.stuAge = stuAge;
	}
	public int getStuAge() {
		return this.stuAge;
	}
}
```
