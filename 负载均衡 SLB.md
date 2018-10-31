# 负载均衡 SLB

本示例介绍如何使用阿里云 Cloud Shell 调用 SLB 的 CreateLoadBalancer 接口创建一个 SLB 实例。

负载均衡（Server Load Balancer）是将访问流量根据转发策略分发到后端多台云服务器（ECS 实例）的流量分发控制服务。负载均衡扩展了应用的服务能力，增强了应用的可用性。

## 示例代码

**说明：** 运行该示例代码将创建 SLB 实例，并产生实际费用。

```
aliyun slb CreateLoadBalancer \
--RegionId <地域ID> \
--LoadBalancerName <实例名称> \
--AddressType <网络类型> \
--LoadBalancerSpec <实例规格> \
```
如：
```
aliyun slb CreateLoadBalancer --RegionId cn-hangzhou --LoadBalancerName test-slb --AddressType intranet --LoadBalancerSpec slb.s1.small
```
