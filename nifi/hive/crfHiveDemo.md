# crfHIveDemo

为方便快速搭建，提供demo模板 [hiveDemo.xml](./hiveDemo.xml)

## 1.nifi同步mysql表至hive



![](./img/hive1.png)

### 1.配置QueryDatabaseTable

若是第一次使用，请选择Database Connection Pooling Service ，
用来创建连接池,mysql选择 DBCPConnectionPool。

![](./img/3.png)

配置连接池

![](./img/4.png)

选择DBCPConnectionPool服务进行配置

![](./img/5.png)

配置QueryDatabaseTable剩下的配置

![](./img/6.png)

就此QueryDatabaseTable配置完成

### 2.配置PutHiveStreaming

![](./img/7.png)

## 2.nifi同步hive数据至kafka

![](./img/2.png)

### 1.配置SelectHiveQL

![](./img/8.png)

配置hive连接池

![](./img/9.png)

### 2.配置PublishKafka

![](./img/10.png)

就此整个案例配置完成，右键start运行。