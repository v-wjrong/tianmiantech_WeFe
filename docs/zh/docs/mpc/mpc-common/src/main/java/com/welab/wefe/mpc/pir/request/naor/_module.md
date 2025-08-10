# 基础信息

|      |      |
|------|------|
| 名称 | naor |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/pir/request/naor |
| 包名 | docs.mpc.mpc-common.src.main.java.com.welab.wefe.mpc.pir.request.naor |
| 概述说明 | QueryNaorPinkasRandomResponse类继承BaseResponse，含uuid、g、p、secret和randoms字段。QueryNaorPinkasRandomRequest类封装查询条件列表。QueryNaorPinkasResultResponse类继承BaseResponse，含uuid和encryptResults字段。QueryNaorPinkasResultRequest类封装uuid和pk字段。 |

# 说明

## 概述  
该模块实现基于Naor-Pinkas协议的隐私信息检索(PIR)功能，核心职责是处理随机数生成与加密结果查询的请求/响应交互。接口规范包含四类主要操作：随机数查询请求(QueryNaorPinkasRandomRequest)、随机数响应(QueryNaorPinkasRandomResponse)、结果查询请求(QueryNaorPinkasResultRequest)和结果响应(QueryNaorPinkasResultResponse)。关键数据结构涉及模幂运算参数(g/p)、密钥材料(secret/pk)、混淆标识(uuid)和加密结果集(encryptResults)。外部依赖包括基础响应基类(BaseResponse)和JCE加密库。例如响应类中randoms字段数量需比混淆IDs少1，结果密文采用AES填充格式。

## 主要业务场景  
完整流程分为两阶段：客户端先提交查询条件列表(queryCondition)获取随机数(g^a/p/randoms)，再通过uuid和公钥(pk0)请求加密结果。交互模式类似挑战-响应机制，服务端维护会话状态(uuid)并执行模幂运算。功能完整性体现在支持动态条件组合和批量结果返回，例如encryptResults列表与原始IDs保持严格对齐。典型应用包括隐私数据查询和联合计算场景，API类型涵盖条件封装类(List<Object>)和密码学参数传输类(十六进制字符串)。


### 包内部结构视图

```mermaid
graph TD
    naor --> QueryNaorPinkasRandomResponse.java
    naor --> QueryNaorPinkasRandomRequest.java
    naor --> QueryNaorPinkasResultResponse.java
    naor --> QueryNaorPinkasResultRequest.java
```

该流程图展示了naor目录下的四个Java文件结构。所有文件都直接位于naor目录中，没有更深层级的子目录。这些文件包括两个请求类（RandomRequest和ResultRequest）和两个响应类（RandomResponse和ResultResponse），构成了一个完整的请求-响应文件组。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [QueryNaorPinkasRandomResponse.java](QueryNaorPinkasRandomResponse.md) | file | QueryNaorPinkasRandomResponse类包含uuid、底数g、模数p、服务器密钥secret和随机大数列表randoms等字段，提供getter和setter方法。 |
| [QueryNaorPinkasRandomRequest.java](QueryNaorPinkasRandomRequest.md) | file | QueryNaorPinkasRandomRequest类包含一个Object类型的List查询条件，提供getter和setter方法。 |
| [QueryNaorPinkasResultResponse.java](QueryNaorPinkasResultResponse.md) | file | QueryNaorPinkasResultResponse类继承BaseResponse，包含uuid和encryptResults字段，后者存储十六进制密文和AES填充字符串列表。 |
| [QueryNaorPinkasResultRequest.java](QueryNaorPinkasResultRequest.md) | file | QueryNaorPinkasResultRequest类包含uuid和pk两个字符串属性，分别有对应的getter和setter方法。 |


