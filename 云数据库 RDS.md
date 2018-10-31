# 云数据库RDS

本示例介绍如何使用阿里云 Cloud Shell 调用 RDS 的 CreateDBInstance 接口创建一个 RDS 实例。

阿里云关系型数据库（Relational Database Service，简称 RDS）是一种稳定可靠、可弹性伸缩的在线数据库服务。基于阿里云分布式文件系统和高性能存储，RDS 支持 MySQL、SQL Server、PostgreSQL 和 PPAS（Postgre Plus Advanced Server，一种高度兼容 Oracle 的数据库）引擎，并且提供了容灾、备份、恢复、监控和迁移等方面的全套解决方案，彻底解决数据库运维的烦恼。

## 示例代码

**说明：** 运行该示例代码将创建 RDS 实例，并产生实际费用。

```
aliyun rds CreateDBInstance \
--Engine <数据库引擎> \
--EngineVersion <引擎版本> \
--DBInstanceClass <实例规格> \
--DBInstanceStorage <存储容量> \
--DBInstanceNetType <网络类型> \
--SecurityIPList <IP白名单> \
--PayType <计费模式> \
--RegionId <地域ID> \
--DBInstanceDescription <数据库描述> 
```
如：
```
aliyun rds CreateDBInstance --Engine MySQL --EngineVersion 5.6 --DBInstanceClass rds.mysql.t1.small --DBInstanceStorage 20 --DBInstanceNetType Intranet --SecurityIPList '%' --PayType Postpaid --RegionId cn-hangzhou --DBInstanceDescription test-rds
```
