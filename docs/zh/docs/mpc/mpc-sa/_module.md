# 基础信息

|      |      |
|------|------|
| 名称 | mpc-sa |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-sa |
| 包名 | docs.mpc.mpc-sa |
| 概述说明 | 该模块实现安全多方计算中的查询处理和密钥交换功能，支持差分隐私和缓存管理，包含固定/自定义因子查询及DH密钥生成接口，依赖缓存系统，适用于联邦学习等场景。 |

# 说明

## 概述  
该模块核心职责是实现安全多方计算中的隐私保护数据传输与密钥交换，整合了查询结果处理、Diffie-Hellman密钥协商和HTTP聚合查询功能。统一接口规范包含两类：密钥交换接口（如`queryDiffieHellmanKey`）采用类似TLS握手模式，结果查询接口（如`queryResult`）支持固定/自定义因子处理。关键数据结构包括DiffieHellman值列表、16进制参数p/g、UUID响应对象及请求/响应体（如`QuerySAResultRequest`）。外部依赖涉及缓存系统（如CacheOperationFactory）和HTTP服务配置（如ServerConfig）。例如`SecureAggregation`类通过UUID管理实现安全聚合，`QueryResultService`利用随机种子实现差分隐私。

## 主要业务场景  
模块支持典型两阶段流程：先通过Diffie-Hellman协议协商密钥（类似RPC调用），再发起混淆结果查询（类似事件总线模式）。完整功能涵盖密钥生成、参数校验、缓存读写和结果累加，适用于联邦学习等场景。交互采用同步HTTP调用，例如客户端请求公钥后服务端响应1024位随机密钥，或通过ADD/SUB操作聚合数据。API分为密钥交换（需p/g参数）和结果查询（支持权重配置）两类，异常处理保障可靠性。具体实现如`SecureAggregation`遍历服务器配置发起请求，`QueryDiffieHellmanKeyService`强制转换16进制数据确保安全。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [mpc-sa-sdk](mpc-sa-sdk/src/main/java/com/_module.md) | module | 该模块通过HTTP协议实现安全数据传输，支持Diffie-Hellman密钥交换和结果查询，适用于联邦学习等场景。核心接口包括密钥协商和结果获取，依赖HTTP服务器配置。 |
| [mpc-sa-server](mpc-sa-server/src/main/java/com/_module.md) | module | QueryResultService处理查询请求，提供两种handle方法，涉及缓存获取、加密计算和结果调整，返回处理结果和UUID。QueryDiffieHellmanKeyService处理密钥交换请求，生成随机密钥，进行加密计算并缓存，返回加密结果和UUID。 |


