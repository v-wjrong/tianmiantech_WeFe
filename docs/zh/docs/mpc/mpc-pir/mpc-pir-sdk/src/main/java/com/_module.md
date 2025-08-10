# 基础信息

|      |      |
|------|------|
| 名称 | com |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-pir/mpc-pir-sdk/src/main/java/com |
| 包名 | docs.mpc.mpc-pir.mpc-pir-sdk.src.main.java.com |
| 概述说明 | 该模块实现基于Naor-Pinkas协议的安全私有信息检索，包含数据混淆、OT交互和加密查询功能。核心类处理密钥生成、参数验证和结果解密，支持客户端-服务器安全检索流程。提供混淆接口生成差异化实例，配置类校验参数合法性。整体确保查询隐私性和流程安全性。 |

# 说明

## 概述  
该模块核心职责是实现安全私有信息检索(PIR)功能，基于Naor-Pinkas和Hauck不经意传输协议，通过数据混淆和加密传输确保查询隐私性。接口规范分为两类：基础PIR接口(如generate/query)处理数据准备和检索，协议专用接口(如queryNaorPinkasRandom)管理加密参数交换。关键数据结构包括QueryKeysRequest、ObliviousTransferKey等传输对象，以及包含主键列表和混淆参数的PrivateInformationRetrievalConfig。外部依赖涉及基础通信框架和RandomPhoneNum等工具类。例如NaorPinkasQuery类实现1024位密钥的Diffie-Hellman加密流程。

## 主要业务场景  
典型应用为客户端-服务器安全检索流程：先通过generateConfuse生成混淆数据集，再分阶段调用协议接口完成加密传输，最终解密目标结果。交互类似两阶段提交协议，支持Naor-Pinkas和Hauck两种OT模式。例如HauckObliviousTransferReceiver通过MAC验证和密钥派生确保传输安全。完整功能覆盖从数据混淆(如MD5加密电话号码)、参数校验到安全检索的全生命周期，异常处理贯穿各环节。API集成案例包括匿名查询和合规检查等场景。


### 包内部结构视图

```mermaid
graph TD
    com --> welab
    welab --> wefe
    wefe --> mpc
    mpc --> pir
    pir --> sdk
    sdk --> trasfer
    sdk --> naor
    sdk --> query
    sdk --> protocol
    sdk --> confuse
    sdk --> config
    sdk --> PrivateInformationRetrievalQuery.java
    trasfer --> impl
    trasfer --> PrivateInformationRetrievalTransferVariable.java
    trasfer --> NaorPinkasTransferVariable.java
    impl --> HttpTransferVariable.java
    naor --> NaorPinkasQuery.java
    query --> PrivateInformationRetrievalClient.java
    protocol --> HauckObliviousTransferReceiver.java
    confuse --> impl
    confuse --> GenerateConfuse.java
    impl --> GenerateConfusePhone.java
    config --> PrivateInformationRetrievalConfig.java
```

该流程图展示了WeFe项目中MPC-PIR-SDK模块的完整Java包结构，从根目录com开始逐级展开至最终实现类。核心节点pir/sdk下包含7个子模块：数据传输(trasfer)、Naor-Pinkas算法(naor)、查询接口(query)、协议实现(protocol)、混淆逻辑(confuse)、配置管理(config)以及主查询类。每个子模块又进一步细化为具体实现类，如trasfer包含3种传输变量实现，confuse包含混淆生成器实现等，完整呈现了私有信息检索功能的代码组织结构。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [welab](welab/_module.md) | package | 该模块实现基于Naor-Pinkas协议的安全私有信息检索，包含数据混淆、OT交互和加密查询功能。核心类处理密钥生成、参数验证和结果解密，支持客户端-服务器安全检索流程。提供混淆接口生成差异化实例，配置类校验参数合法性。整体确保查询隐私性和流程安全性。 |


