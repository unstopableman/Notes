PLSQL：声明部分	主体部分		

声明部分：声明变量

主体部分：所有的逻辑操作

异常部分：对主体部分发生异常情况进行处理

```
declare

begin

end;
```

变量：变量名 类型（长度）;

数据类型：oracle的基本的数据类型，%type，%RowType

dbms_output.put_line();

控制语句：

条件语句：

```
declare

begin
	if 条件表达式 then 
	elseif 条件表达式 then
	else
	endif;
end;
```

循环语句：

```
基本循环
loop
	循环体;
	exit when 条件;
end loop;
```

```
while循环
while 条件表达式 loop
	循环体;
end loop;
```

```
数字式循环
for 变量 in 下限 .. 上限 loop
	循环体;
end loop;
```

运算符：赋值运算符  := 		字符串拼接  ||



```
select 字段 into 变量 from 表明 where 条件;
```

