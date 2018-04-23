# nifi HBase Demo

为方便快速搭建，提供demo模板 [delimitedtohbase.xml](./delimitedtohbase.xml)

## 1.Demo整体结构

demo背景：利用nifi自动生成数据组件生成数据，并将数据切割清洗为json格式并传入Hbase。

![](./img/1.png)

## 2.ReplaceText配置

![](./img/2.png)

## 3. SplitText配置

![](./img/3.png)

## 4.ExtractText配置

![](./img/4.png)

![](./img/5.png)

## 5. Rename Attributes配置

![](./img/6.png)

## 6. ReplaceText配置

![](./img/7.png)

## 7. LogAttribute配置

![](./img/8.png)

## 8. PutHBaseJSON配置

![](./img/9.png)

HBase client配置

> 需将hadoop的core-site.xml和Hbase的hbase-site.xml复制到nifi所在机器。

![](./img/10.png)