# 基础信息

|      |      |
|------|------|
| 名称 | mpc |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc |
| 包名 | docs.mpc |
| 概述说明 | 该系列模块实现安全多方计算(MPC)核心功能：PIR隐私检索、PSI隐私求交、密钥交换与安全聚合。采用Naor-Pinkas/Hauck/ECDH等协议，支持联邦学习与联合风控场景。包含加密传输、数据混淆、线程安全缓存等机制，通过分层API与POJO规范提供完整生命周期管理。 |

# 说明

## 概述  
该模块是安全多方计算(MPC)的核心组件，整合隐私信息检索(PIR)、隐私集合求交(PSI)和安全聚合(SA)功能，通过Naor-Pinkas/Hauck协议、ECDH和Diffie-Hellman等加密技术实现数据隐私保护。统一接口规范包含六类操作：PIR基础接口（如generate/query）、PSI服务接口（如PrivateSetIntersectionService）、密钥交换（如queryDiffieHellmanKey）和结果聚合（如QuerySAResult）。关键数据结构聚合为Diffie-Hellman参数（p/g）、加密映射表、会话标识（UUID）和混淆数据模型，依赖BouncyCastle/JCE加密库、线程池和JSON工具。例如通过EcdhPsi实现双向加密求交，SecureAggregation利用随机种子实现差分隐私。

## 主要业务场景  
模块支撑联邦学习和联合风控场景，典型流程为分层式安全计算：1）Diffie-Hellman密钥交换（类似TLS握手）；2）PSI数据匹配（ECDH双向加密求交）；3）PIR隐私检索（Naor-Pinkas协议）和结果聚合。交互模式采用双轨制API，同步接口处理即时请求（如getHauckTarget），异步服务管理后台任务（如HuackKeyService线程池）。功能完整性涵盖密钥管理、数据混淆到安全传输全生命周期，例如DhPsiServer加速密文比对，QueryResultService支持权重配置。API分层设计，基础层如DiffieHellmanUtil静态方法，协议层如QuerySAResultRequest对象化操作，适用于跨机构安全计算。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [mpc-sa](mpc-sa/mpc-sa-sdk/src/main/java/com/_module.md) | module | 该模块实现安全多方计算中的查询处理和密钥交换功能，支持差分隐私和缓存管理，包含固定/自定义因子查询及DH密钥生成接口，依赖缓存系统，适用于联邦学习等场景。 |
| [mpc-psi](mpc-psi/mpc-psi-sdk/src/main/java/com/_module.md) | module | 该SDK实现多方隐私集合求交(PSI)功能，支持ECDH和DH加密协议，包含服务端/客户端组件、数据预处理工具和工厂模式。核心流程为密钥生成、数据加密和结果比对，通过多线程优化性能，适用于安全数据匹配场景。 |
| [mpc-common](mpc-common/src/main/java/com/_module.md) | module | AbstractHttpTransferVariable是处理HTTP请求的抽象类，支持JSON转换和签名验证。安全聚合模块实现密钥交换和加密通信。密码学工具集提供SM2/RSA等算法。MPC基础工具集支持数值转换和随机数据生成。PSI模块处理私有集合交集查询。本地缓存系统采用两级结构。DiffieHellmanKey类管理DH协议参数。PIR模块实现隐私信息检索协议。通信配置类定义请求参数。 |
| [mpc-pir](mpc-pir/mpc-pir-sdk/src/main/java/com/_module.md) | module | 该模块实现隐私信息检索(PIR)协议，包含密钥生成、随机数验证和加密数据传输。支持Naor-Pinkas和Hauck协议，提供同步/异步接口，涉及数据混淆、参数校验和安全传输。依赖加密库和线程池，适用于分层隐私查询场景。 |


