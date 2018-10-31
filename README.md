# Cloud Shell 快速上手指南

## 产品入口

请在 [shell.aliyun.com](https://shell.aliyun.com) 登录并请求一个 Cloud Shell 使用。

## 使用说明

### 调用API

您需要按照如下方式拼装命令：

```
aliyun <product> <operation> [--parameter1 value1 --parameter2 value2 ...]
```

- `aliyun` 为固定值，启动命令行。

- `product` 为云产品英文名称缩写，获取方式：

    键入命令：`aliyun help` 或 `aliyun --help`

- `operation` 为 API 名称或者PATH。阿里云的 API 分为 RPC 和 REST 两种风格。如：“云服务器 ECS”、“云数据库 RDS” 版 为 RPC 风格，而“容器服务”、“资源编排”则为 REST 风格。
    - RPC 风格 API 的 `operation` 为 API Name 获取方式：
	    - 键入命令：`aliyun <product> help` ，如：`aliyun ecs help`
		- 键入命令：`aliyun <product> --help` ，如：`aliyun ecs --help`
	- REST 风格 API 的 `operation` 为 API 的 PATH。获取方式：
	    - 键入命令：`aliyun <product> help` 或 `aliyun <product> --help` 点击 API 文档链接，或者直接打开 API 文档来获取。

- `parameter` 为 API 的请求入参，获取方式：
    - `aliyun <product> <operation> help` ，如：`aliyun ecs DescribeRegions help`
	- `aliyun <product> <operation> --help` ，如：`aliyun ecs DescribeRegions --help`

### 返回结果格式

返回结果可以是格式化的 JSON 数据或表格。默认返回 JSON 数据。

- JSON

    不指定返回数据格式，默认会以 JSON 格式返回。如：
	![avatar](http://docs-aliyun.cn-hangzhou.oss.aliyun-inc.com/assets/pic/74637/cn_zh/1528946649585/20180614112244.png)

- 自定义表格
    如需要输出自定义表格格式，您需要按照如下方式添加参数：
    `--output cols=[parameter1,parameter2,...]`
	- `--output` 表示使用表格输出。
	- 使用--output参数，必须同时指定cols：
	    - `cols` 为表格的列名，需要与 JSON 数据中的字段相对应。如 ecs DescribeInstances 接口返回结果中的字段 InstanceId 以及 Status。
		    以 查询 ECS 地域 指令为例：`aliyun ecs DescribeRegions --output cols=RegionId,LocalName`
	        该指令的数据结果将以表格的形式输出，以 RegionId、LocalName 作为表头。执行结果如图：
			![avatar](http://docs-aliyun.cn-hangzhou.oss.aliyun-inc.com/assets/pic/74637/cn_zh/1528957092904/20180614141757.png)
	
### 调用示例

请查看本仓库下的其他文件。
