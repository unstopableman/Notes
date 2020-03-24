JDBC：实现数据的持久化

JDBC是java所提供的一套访问数据库的接口（规范）

接口都位于java.sql包下

接口由数据库厂商实现呢——数据库的驱动包

JDBC的使用步骤：；

1. 获取数据库的驱动包

2. 将数据库的驱动包导入到项目中（类路径下）

3. 配置连接属性

   url：jdbc:mysql://localhost:3306/databaseName

   driver:

   com.mysql.jdbc.Driver/oracle.jdbc.driver.OracleDriver

   user:username

   password:password

   jdbc.properties

4. 加载（注册）驱动 class.forName（驱动的全类名）；

5. 获取链接：

   ```
   Connection conn = DriverManager.connection(url,user.password);
   ```

…………

…………

数据库存储中一些特殊数据

大文本数据	text（mysql）	字符类型