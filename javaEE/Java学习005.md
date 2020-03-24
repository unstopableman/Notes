# 昨日回顾
    变量必须先声明后使用
# 一、选择/分支结构
## if()语句 

```
if(条件表达式结果一定是boolean){
        条件表达式的结果为true时，需要执行的语句;
    }else{
        条件表达式的结果为false时，需要执行的语句;
    }
```


    常量：不可改变的变量就称为常量
    常量：字面常量、自定义常量
    字面常量：所使用的所有的数字、字母、汉字、符号
    int i =2;   char c = 'a';
    final int I = 2;

## switch语句 

```
switch(表达式){
     case 常量1: 
         语句1; 
         // break; 
     case 常量2: 
         语句2; 
         // break; 
         … … 
     case 常量N: 
         语句N;
         // break; 
     default: 语句; 
         // break; 
 }
```

```
public  class SwitchDemo{
	/*
	3.根据用于指定月份，打印该月份所属的季节。 
		3,4,5 春季 
		6,7,8 夏季 
		9,10,11 秋季 
		12, 1, 2 冬季 
	*/
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		System.out.println("请输入你需要判断的月份（1--12）：");
		int month = sc.nextInt();
		switch(month){
			case 3:
			case 4:	
			case 5:
				System.out.println("春季");
				break;
			case 6:
				
			case 7:
				
			case 8:
				System.out.println("夏季");
				break;
			case 9:
				
			case 10:
				
			case 11:
				System.out.println("秋季");
				break;
			case 12:
				
			case 1:
				
			case 2:
				System.out.println("冬季");
				break;
			default:
				System.out.println("输入的月份有误");
				break;

		}
	}
}
```

```
public  class SwitchDemo{
	/*
	编写程序：从键盘上输入2019年的“month”和“day”，
	要求通过程序 输出输入的日期为2019年的第几天。
	*/
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		System.out.println("请输入你的月份（1--12）：");
		int month = sc.nextInt();
		System.out.println("请输入你的日期（1--31）：");
		int day = sc.nextInt();
		int days= 0;
		switch(month){
			case 1:
				days = day;	
				break;
			case 2:
				days = 31 + day;
				break;
			case 3:
				days = 31 + 28 + day;
				break;
			case 4:	
				days = 31 + 28 + 31 + day;
				break;
		}
		System.out.println("您输入的日期为2019年的第"+days+"天");
		
	}
}
```

		
	
```
public  class SwitchDemo{
	
		/*
	
		编写一个程序，为一个给定的年份找出其对应的中国生肖。
	
		中国的生肖基于12年一个周期， 每年用一个动物代表：
	
		rat、ox、tiger、rabbit、dragon、snake、horse、sheep、monkey、 rooster、dog、pig。
	
		算法是程序的灵魂：
	
		2008 鼠  （2019 - 1900 ）% 12  1900鼠
	
		*/
	
		public static void main(String[] args){
	
			Scanner sc = new Scanner(System.in);
	
			System.out.println("请输入4位数的年 ：");
	
			int year = sc.nextInt();
	
			int num = (year - 1900 )% 12;
	
			switch(num){
	
				case 0:
	
					System.out.println("鼠");
	
					break;
	
				case 1:
	
					System.out.println("牛");
	
					break;
	
				case 2:
	
					System.out.println("虎");
	
					break;
	
			}
	
		}	
	
	}
```


![在这里插入图片描述](https://img-blog.csdnimg.cn/20191101180233958.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

使用注意事项：
    
    1.在每一个case之后都需要break，如果没有break会出现case穿透；
    2.default不是必须的，如果有default，也必须加上break；
    3.switch的表达式的类型：int byte  short  char String(jdk7.0)  枚举 (jdk 5.0)
    4.case后必须是常量
    5.case后的常量不允许重复

# 二、循环结构
## for循环
    for(){
        
    }   

## while循环

    while(){
        
    }

## do…while();循环
    do{
        
    }while();


## 区别
    1.从循环变量的生命周期：for仅限于其整个循环，while范围更大；
    2.for用于能够明确循环次数，while用于循环次数模糊的循环；
    通常情况两者可以进行转换

## 循环嵌套


    如果break出现在嵌套循环中，则结束的是它所在的循环，并不能结束外层循环
    如果想结束外层循环 可以通过加标记的方式（了解） 开发中尽量不用


```
public class ForDemo 
{	
	/*
		 输出九九乘法表
	*/
	public static void main(String[] args) 
	{	
		l1:for(int i = 1 ; i < 10 ;i++){//外层循环  控制的行
			for(int j = 1 ; j <= i; j++){// 内层循环 控制每一行列
				System.out.print(i +" * " + j +" = " + i * j +"  ");
				if( j == 5){
					break l1;//结束指定标记的循环
				}
			}
			System.out.println();
		
		}
	}
}

```
