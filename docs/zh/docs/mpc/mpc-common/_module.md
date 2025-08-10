# 基础信息

|      |      |
|------|------|
| 名称 | mpc-common |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-common |
| 包名 | docs.mpc.mpc-common |
| 概述说明 | AbstractHttpTransferVariable是处理HTTP请求的抽象类，支持JSON转换和签名验证。安全聚合模块实现密钥交换和加密通信。密码学工具集提供SM2/RSA等算法。MPC基础工具集支持数值转换和随机数据生成。PSI模块处理私有集合交集查询。本地缓存系统采用两级结构。DiffieHellmanKey类管理DH协议参数。PIR模块实现隐私信息检索协议。通信配置类定义请求参数。 |

# 说明

## 概述  
该模块是安全多方计算(MPC)基础框架，核心职责是实现加密协议封装、密钥管理和安全通信，类似零信任架构的中间件层。接口规范包含四类：安全聚合(QuerySAResult)、密钥交换(QueryDiffieHellmanKey)、PSI查询(QueryPrivateSetIntersection)和PIR协议(QueryKeysRequest)，均采用POJO+JSON序列化。关键数据结构涵盖Diffie-Hellman参数(p/g)、PSI批次控制字段、PIR会话标识(uuid)和群运算坐标，依赖BouncyCastle/JCE加密库和JSON工具。例如SM2KeyPair管理国密密钥，LocalIntermediateCache实现线程安全存储。

## 主要业务场景  
模块支撑联邦学习和联合风控场景，典型流程为：1) DH密钥交换→2) 数据安全聚合/PSI比对→3) PIR隐私检索。交互采用请求-响应链模式，通过uuid关联会话，类似加密信封机制。功能完整性体现在：支持SM2/RSA签名、AES/SHA加密、Naor-Pinkas协议和权重调节聚合。例如SignUtil自动选择算法，CacheUtil管理临时数据。API类型分层设计，基础层如DiffieHellmanUtil静态方法，协议层如QuerySAResultRequest对象化操作。集成案例包括跨机构ID安全匹配和加密手机号生成。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | AbstractHttpTransferVariable是处理HTTP请求的抽象类，支持JSON转换和签名验证。安全聚合模块实现密钥交换和加密通信。密码学工具集提供SM2/RSA等算法。MPC基础工具集支持数值转换和随机数据生成。PSI模块处理私有集合交集查询。本地缓存系统采用两级结构。DiffieHellmanKey类管理DH协议参数。PIR模块实现隐私信息检索协议。通信配置类定义请求参数。 |


