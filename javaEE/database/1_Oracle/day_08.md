[TOC]

------

## 数据的处理：select		insert	update		delete

insert：insert into table_name（字段名，）	values（）；

update：update table_name set 字段名=字段值 where ...;

delete：delete [from] table_name where ...;

## 表的创建和管理：

oracle-oracle的实例-表空间-用户-表

### 表空间：

​	永久表空间	临时表空间	undo表空间

### 表的存储：

​	数据文件（.dbf），日志文件（.log），控制文件（.ctl）

### 创建表的步骤：

1. 创建表空间： 永久表空间	临时表空间	undo表空间

2. 创建用户：create user user_name indetify by password；

3. 为用户赋予权限：grant 角色名，to user_name；

4. 创建表：create table table_name（

   字段名	字段类型（长度）	default	value		约束，

   ）

5. 约束：not null，唯一约束，主键约束，外键约束，检查约束

   非空约束：只能用在列上

   唯一约束：unique

   主键约束：唯一约束 + 非空约束

   CONSTRAINT 约束名 PRIMARY KEY（主键列的列名）

   还可以使用联合主键。

6. 外键约束

   表与表之间的关系：一对一，一对多，多对一，多对多

   ​	一对一：一夫一妻制

   ​	一对多/多对一：员工与部门之间的关系

   ​	多对多：订单和商品，用户和权限

   关系的维护：

   ​	一对一的关系维护可以在任意一方来维护；

   ​	一对多/多对一  ——  往往一方来维护

   ​	多对多  ——  需要借助于第三张表来维护这种关系

   表的设计：以一对多为例：在一方的表中，设计一个冗余字段来保存自己与多方的关系

   employees中有一个department_id

   为了保证 在插入数据的时候，不至于出现非法数据，所以在建表的时候，就会为表指定外键约束。

   