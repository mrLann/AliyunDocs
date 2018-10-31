# 专有网络 VPC

本示例介绍如何使用阿里云 Cloud Shell 调用 VPC 的 CreateVpc 接口创建一个 VPC。

专有网络 VPC（Virtual Private Cloud）是用户基于阿里云创建的自定义私有网络, 不同的专有网络之间二层逻辑隔离，用户可以在自己创建的专有网络内创建和管理云产品实例，比如 ECS、负载均衡、RDS 等。

## 示例代码

```
aliyun vpc CreateVpc --RegionId <地域ID> --VpcName <实例名称> --CidrBlock <实例网段>
```
如：
```
aliyun vpc CreateVpc --RegionId cn-hangzhou --VpcName test-vpc --CidrBlock '192.168.0.0/16'
```
