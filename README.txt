1.�޸�resource�ļ�����generator.properties�����ݿ����ӵ���Ϣ
	jdbc.driverLocation=G:\\maven\\maven local\\mysql\\mysql-connector-java\\5.1.38\\mysql-connector-java-5.1.38.jar
	jdbc.driverClass=com.mysql.jdbc.Driver
	jdbc.connectionURL=jdbc:mysql://IP:PORT/DATABASE
	jdbc.userId=USERNAME
	jdbc.password=PASSWORD
2.��generatorConfig.xml���޸���Ҫ��Mybatis�湤�̳����ļ��зֲ㼰���������
3.��һ�������ɶ����ֻ�貢�����
   		<table tableName="����" domainObjectName="��Ҫ��ʵ������"
               enableCountByExample="true" enableUpdateByExample="true"
               enableDeleteByExample="true" enableSelectByExample="true"
               selectByExampleQueryId="true">
            <columnOverride column="��������������纬��_��param_data" javaType="�����Ե�java����java.lang.String" jdbcType="���������ݿ��е�����VARCHAR"/>
        </table>
	��������ݿ������б����湤�̣�����ֱ������tableNameֵΪ%����ƥ�����б�������ʱdomainObjectName���Ծ�Ҫȥ����
4.ʹ��ǰҪ����һ��maven��mybatis-generator:generate -e��Ȼ��������Ŀ���Ϳ��Եõ���Ҫ��mybatis������
