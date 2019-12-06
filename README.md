# mybatis-tools
生成数据库对应的MyBatis配置文件的工具应用，目前支持MySql和Postgresql数据库。

支持生成数据库表对应的java domain类和MyBatis的映射文件, domain类名从表名转化而来，类名和表名的映射关系：
1. 表对应的 Java 类名采用驼峰命名法，表名中如果有"\_"，则把"\_"后面的首字母大写。 如 user_order 表对应的domain类名为 UserOrder.java，对应的映射文件名称也是UserOrder.xml。
2. 生成的domain类的属性对应表的字段。
3. 生成的MyBatis映射文件的内容，只有基本信息。


使用方法：
1. 修改database.properties，写上数据库连接URL信息和要生成文件的路径、Mapper类的包名等。
2. 根据数据库的种类，选择mysql或postgresql包下的TableToBean.java和TableToXml.java，就生成相应的Domain类和XML文件到相应目录。


Gitee 代码库的 mybatis-tooles 项目链接：
https://gitee.com/geeksun/mybatis-tools
