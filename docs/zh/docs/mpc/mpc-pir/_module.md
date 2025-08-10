# 基础信息

|      |      |
|------|------|
| 名称 | mpc-pir |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-pir |
| 包名 | docs.mpc.mpc-pir |
| 概述说明 | 该模块实现隐私信息检索(PIR)协议，包含密钥生成、随机数验证和加密数据传输。支持Naor-Pinkas和Hauck协议，提供同步/异步接口，涉及数据混淆、参数校验和安全传输。依赖加密库和线程池，适用于分层隐私查询场景。 |

# 说明

## 概述  
该模块实现多方安全计算中的隐私信息检索(PIR)功能，核心职责是通过Naor-Pinkas和Hauck不经意传输协议确保查询隐私性，结合数据混淆和加密传输实现安全中间件模式。统一接口规范包含六类操作：基础PIR接口（如generate/query）、协议专用接口（如queryNaorPinkasRandom）、随机数处理、密钥派生等。关键数据结构聚合为五类：传输对象（QueryKeysRequest/ObliviousTransferKey）、配置参数（PrivateInformationRetrievalConfig）、加密参数（Diffie-Hellman密钥对/AES密钥）、缓存对象（HauckTarget）和跟踪标识（UUID）。外部依赖包括JCE加密库、线程池、通信框架和工具类（如RandomPhoneNum），例如通过ArrayBlockingQueue实现线程安全缓存，采用1024位Diffie-Hellman密钥交换流程。

## 主要业务场景  
典型应用为分层式安全检索流程：预处理阶段生成混淆数据集（如MD5加密电话号码），查询阶段组合Naor-Pinkas/Hauck协议完成加密传输，类似两阶段提交协议。完整业务流程覆盖三个维度：1）缓存控制（500容量阈值+2秒休眠检测）2）安全验证（120秒超时+MAC校验）3）异步传输（JSON结果封装）。交互模式支持双轨制API：同步接口处理即时请求（如getHauckTarget），异步服务管理后台任务（如HuackKeyService线程池）。例如HauckObliviousTransferReceiver通过密钥派生确保传输安全，NaorPinkasResultService实现混合加密网关功能。功能完整性涵盖数据混淆、参数校验到安全检索全生命周期，异常处理贯穿各环节。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [mpc-pir-sdk](mpc-pir-sdk/src/main/java/com/_module.md) | module | 该模块实现基于Naor-Pinkas协议的安全私有信息检索，包含数据混淆、OT交互和加密查询功能。核心类处理密钥生成、参数验证和结果解密，支持客户端-服务器安全检索流程。提供混淆接口生成差异化实例，配置类校验参数合法性。整体确保查询隐私性和流程安全性。 |
| [mpc-pir-server](mpc-pir-server/src/main/java/com/_module.md) | module | PrivateInformationRetrievalEvent类处理私有信息检索事件，含uuid和keys属性。模块实现PIR协议数据传输与验证，管理随机数和加密数据。ProduceHauckTargetThread线程生成并缓存HauckTarget对象。HauckObliviousTransferSender类实现密钥生成流程。模块基于Naor-Pinkas协议提供安全查询服务。HauckTargetCache单例类管理线程安全缓存。PrivateInformationRetrievalFlowServer类处理检索流程。PrivateInformationRetrievalServer类提供服务器初始化和缓存管理功能。 |


