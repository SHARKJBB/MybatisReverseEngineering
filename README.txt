1.修改resource文件夹下generator.properties中数据库链接的信息
	jdbc.driverLocation=G:\\maven\\maven local\\mysql\\mysql-connector-java\\5.1.38\\mysql-connector-java-5.1.38.jar
	jdbc.driverClass=com.mysql.jdbc.Driver
	jdbc.connectionURL=jdbc:mysql://IP:PORT/DATABASE
	jdbc.userId=USERNAME
	jdbc.password=PASSWORD
2.在generatorConfig.xml中修改需要的Mybatis逆工程出的文件夹分层及各层的名字
3.可一次性生成多个表，只需并列添加
   		<table tableName="表名" domainObjectName="想要的实体类名"
               enableCountByExample="true" enableUpdateByExample="true"
               enableDeleteByExample="true" enableSelectByExample="true"
               selectByExampleQueryId="true">
            <columnOverride column="特殊的属性名（如含有_）param_data" javaType="该属性的java类型java.lang.String" jdbcType="属性在数据库中的类型VARCHAR"/>
        </table>
	如果你数据库中所有表都想逆工程，可以直接设置tableName值为%，即匹配所有表，不过此时domainObjectName属性就要去掉。
4.使用前要配置一下maven的mybatis-generator:generate -e，然后运行项目，就可以得到想要的mybatis工程了
