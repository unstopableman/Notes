**昨日回顾**：

Java基础语法：

​	标识符

​	关键字

​	保留字

​	变量和数据类型

​	自动转化

​		byte   short   char   int   long

​			byte、short、char 可以直接转换为int

​			byte、short、char 类型之间不能相互转换

​			int 也可以直接转换为long，需要在数据的结尾添加L

​		float   double

​			float也可以直接转换为double

​		强制类型转换

​			语法： 接受类型  变量名 = （将要转换的类型）待转换变量

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029013722140.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

​			

​			特殊情况：

​				long—>float

​				可以转换

​				float 32位，使用最高位1位表示符号位，8位表示E，23位表示小数

​				long转换为float，可以自动转换你，但是这种转换之后E后的数据具有不确定性，尽量不用

​				long到double同理。

​			浮点数转换为整数

​				进行转换时会舍弃小数位

​			boolean类型占一个字节的空间

​				boolean  true/false  —>1/0

​			理论上 一位（bit）就可以保存boolean，但是最小的存储单元是byte（字节），所以在分配空间时依然分配一个字节。

​			String类型：不属于8种基本类型，属于引用类型。		

------



# 一、进制

## 1.常用进制：

二进制 0 1

八进制 0 1 2 3 4 5 6 7

十进制 0~9

十六进制 0~9 A~F

## 2.二进制的表示形式

### （原码 反码 补码）

1.正数的原码、反码、补码都是它本身

2.负数的		

- 原码 将该负数表示为二进制
- 反码 按位取反（0变为1,1变为0）
- 补码 反码+1

## 3.十进制转二进制

​	对十进制的数字使用短除法，除数为2，一直到商为0，然后余数从下往上排列就是对应的二进制。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029013745971.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

​	如十进制的5对应的二进制就是 0000 0101

​	为什么要设计程原码 反码 补码  就在于计算机无法识别符号位  所以在运算中  将符号位也参与运算    只有加法没有减法 

![在这里插入图片描述](https://img-blog.csdnimg.cn/2019102901380627.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

## 4.十进制转八进制

首先转换为二进制，然后三位2进制表示一位8进制。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029013822302.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)



## 5.十进制准十六进制

四位二进制表示一位16进制。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029013843258.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

## 6.不同进制的数据的表示

十进制直接表示

二进制直接使用01表示

八进制表示的时候一般在数据前加0  如：014

十六进制表示的时候一般在前边加0x  如：0xC

System.out.println(bb1);输出时 所有的整数都按照int类型输出 

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029013907945.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/2019102901392229.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)



# 二、运算符

- 算术运算符
- 逻辑运算符
- 赋值运算符
- 关系运算符
- 位运算
- 三元运算符

## 1.算术运算符

算术运算中  byte  short char  int  运算的结果都是int类型 ；

在整数类型及char类型做运算的时候 如果操作数如果时byte short char，那么运算的结果是int；

如果期中有int类型的操作书 结果肯定是int；

如果操作书中有long类型 结果肯定是long；

如果在运算中操作数中有float类型 则结果为float；

如果在运算中操作数中有double类型 则结果为double；

boolean不能参与算数运算 boolean也不能和其他类型之间进行相互转换；

对于/  *法运算 其中如果有负数 则结果为负；

在除法运算中 取得是相除的商；

%取模运算  结果为余数  结果的正负与第一个操作数保持一致；



​    ++ 自增

​    --自减

​    ++  作用都是给当前操作数+ 1

​    ++写在操作数之后  是先取操作数的值 然后在给该数加1

​    ++写在操作数之前 是先加1 在取值



![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029013938122.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

​    赋值运算符

​    =  +=  -+ /=   %=

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029014022200.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019102901404478.png)

​    ① 编译报错 结果是int  ②正确 += 会进行强制类型转换

​    比较运算

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191029014107640.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

比较运算的结果都是boolean类型  通常用于逻辑判断  注意不要将 == 误写为 = 

> 逻辑运算符

&—逻辑与  | —逻辑或   ！—逻辑非   && —短路与   || —短路或   ^ —逻辑异或

![在这里插入图片描述](https://img-blog.csdnimg.cn/2019102901412291.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzQxNzI5,size_16,color_FFFFFF,t_70)

&运算中只要有false  结果就为false

| 运算中 只要有true  结果就为true 

！ true 为false  false 为true

^  当两个不同时  则为true 相同时为false

&& 当在运算中 如果符号左边为false  则右边不在执行运算 只有左边为true  右边才会进行运算

|| 短路或 如果符号左边为true  右边就不执行运算  只有左边为false 右边才会执行运算



果就为false

| 运算中 只要有true  结果就为true 

！ true 为false  false 为true

^  当两个不同时  则为true 相同时为false

&& 当在运算中 如果符号左边为false  则右边不在执行运算 只有左边为true  右边才会进行运算

|| 短路或 如果符号左边为true  右边就不执行运算  只有左边为false 右边才会执行运算



