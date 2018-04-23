# Nifi Ftp与HDFS使用

## 1.Windows10搭建Ftp文件服务器

为方便快捷，本案例直接使用windows自带的ftp服务

### 1.启用ftp服务

![](./img/1.png)

### 2.IIS管理器

![](./img/2.png)

### 3.打开“IIS管理器”后，在左栏的“网站”上点击右键，打开“添加FTP站点，并配置

![](./img/3.png)

![](./img/4.png)



![](./img/5.png)

![](./img/6.png)

### 4.启动运行

![](./img/7.png)

到此Ftp服务搭建完成。

## 2.FTP与HDFS操作

为方便操作请使用模板[FtpToHDFS.xml](./FtpToHDFS.xml)

整体结构图

![](./img/8.png)

### 2.定时从ftp中拉去文件到HDFS 

#### 1.配置GetFTP

![](./img/10.png)

#### 2.配置PutHDFS

![](./img/11.png)

> Hadoop Configuration Resources:配置需要将hadoop集群的core-site.xml、hdfs-site.xml拷贝至nifi所在服务器的目录下。

### 3.定时从HDFS中拉取数据到ftp

#### 1.GetHDFS配置

![](./img/12.png)

#### 2.PutFTP配置

![](./img/13.png)

就此配置完成，启动处理器开始传输数据吧。