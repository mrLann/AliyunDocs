# 创建 ECS 实例

本示例介绍如何使用阿里云 Cloud Shell 调用 ECS 的 CreateInstance 接口创建一个 ECS 实例。

在创建 ECS 实例前，您需要获取以下信息：

- 镜像 ID

    调用 DescribeImages 接口查看要使用的镜像 ID。如：
```
aliyun ecs DescribeImages --output cols=OSType,OSName,ImageId
```

- 实例规格

    查看[实例规格族](https://help.aliyun.com/document_detail/25378.html)或调用 DescribeInstanceTypes 接口查看要创建选择要创建的 ECS 实例的规格。如：

```
aliyun ecs DescribeInstanceTypes
```

## 示例代码

**说明：** 运行该示例代码将创建 ECS 实例，并产生实际费用。

```
aliyun ecs CreateInstance \
    --ImageID <镜像名称> \
    --InstanceName <实例名称> \
    --SecurityGroupId <安全组ID> \
    --InstanceType <实例规格> \
    --InstanceChargeType <计费模式> \
    --RegionId <地域ID>
```
如：
```
aliyun ecs CreateInstance --ImageId ubuntu_16_0402_64_20G_alibase_20180409.vhd --InstanceName Test-Instance --SecurityGroupId sg-uf638e1btn2lfgyxffff --InstanceType ecs.t5-lc2m1.nano --InstanceChargeType PostPaid --RegionId cn-hangzhou
```
