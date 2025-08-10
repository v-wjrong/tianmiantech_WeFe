# 基础信息

|      |      |
|------|------|
| 名称 | java |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java |
| 包名 | docs.common.java |
| 概述说明 | Java基础工具库，含配置管理、数据处理、验证、HTTP通信等功能，依赖Log4j等。Web应用全栈方案，支持API管理、权限控制、日志记录，依赖Spring等。JPA数据访问层，提供CRUD、动态查询，依赖JPA。跨云数据存储，支持分片、连接池管理，依赖Druid。Protobuf协议，支持数据序列化。MongoDB数据管理，支持CRUD、聚合查询。联邦学习框架，含健康检查、配置管理等。验证码服务，支持短信/邮件发送。密码学工具集，支持密钥管理、证书操作。JDBC框架，支持多数据库操作。 |

# 说明

## 概述  
该模块是联邦学习平台的全栈基础设施，核心职责包括数据治理（多数据库CRUD/动态查询）、安全通信（国密算法/证书管理）和开发支持（配置管理/验证码服务）。接口规范分层设计，如AbstractApi基类体系、JdbcScanner抽象查询和工厂模式（ClientFactory）。关键数据结构涵盖分页对象（Pageable）、证书模型（CryptoKeyPair）、条件构建器（Where）和验证码枚举（CaptchaSendChannel）。外部依赖包括Spring框架、BouncyCastle、MongoDB驱动和云平台SDK，例如Log4j用于日志记录，阿里云短信SDK实现验证码发送。  

模块采用多模式集成设计，类似中间件集合。例如Configurations管理多环境配置，JdbcClient统一JDBC操作，CertService处理证书签发。技术特征包含注解驱动（@FlowLimitByMobile）、策略枚举（ServiceType）和流式处理（BatchConsumer）。典型实现如SM2密钥生成→PEM格式化存储，或通过Where.equal().groupBy()构建动态查询。  

## 主要业务场景  
模块支撑三大核心闭环：1) 安全闭环，通过验证码服务（短信/邮件）→证书管理（SM2签名）→HTTPS通信，例如用户注册时的短信验证码校验；2) 数据闭环，组合JdbcScanner流式查询→MongoDB聚合操作→分页存储，类似ETL管道；3) 服务闭环，从健康检查（UnionService检测）→API执行（反射调用）→日志审计。  

统一交互模式为链式调用与工厂模式结合。例如Where构建器生成动态SQL条件，ClientFactory按渠道选择验证码客户端。功能完整性体现在覆盖国密算法（SM3WITHSM2）、多数据库（MySQL/MongoDB）和全生命周期管理（如证书WAIT_VERIFY→VALID）。典型应用包括：联邦学习任务配置（资源选择器）、高并发数据分片（PageInputModel）和跨云存储切换（OSS凭证管理）。例如HttpRequest自动处理302跳转，Validator验证身份证格式。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [common-data-mysql](common-data-mysql/src/main/java/com/_module.md) | module | MyJpaRepository提供分页查询和字符串处理默认方法。PageUtils处理单对象分页。OrderBy枚举定义排序方向。CurdException为自定义异常。实体类继承体系管理通用字段。SQL监控模块捕获慢SQL和错误。抽象JPA配置类创建实体管理器工厂和数据源。MySpecification实现动态查询条件构建。DataMysql为数据库操作基础类。Where类链式构建查询条件。 |
| [common-jdbc](common-jdbc/src/main/java/com/_module.md) | module | HiveScanner和MysqlScanner是JdbcScanner的子类，分别用于Hive和MySQL查询。JdbcScanner是抽象基类，封装JDBC查询流程，支持多数据库适配。JdbcClient封装JDBC操作，支持多种数据库，提供连接管理、批量写入和流式查询功能。 |
| [common-proto](common-proto/src/main/java/com/_module.md) | module | 这是一个Google Protocol Buffers (protobuf) 定义文件，描述了一个中间数据结构的协议。主要包含三个消息类型：IntermediateDataItem（键值对数据项）、BatchSerializationData（批量序列化数据）和IntermediateData（中间数据容器）。IntermediateData支持两种存储方式：1）多条键值对数据集合；2）整体序列化后的二进制数据。文件定义了数据结构和相关操作方法，用于不同系统间的数据交换。 |
| [common-cert](common-cert/src/main/java/com/_module.md) | module | 密码学工具集，含密钥管理、证书操作、文件处理。支持RSA/ECDSA/SM2算法，PFX/JKS解析，依赖BouncyCastle。适用PKI全周期管理，如密钥生成、证书签发、存储。含静态工具类如KeyUtils、CertUtils。 |
| [common-verification-code](common-verification-code/src/main/java/com/_module.md) | module | 阿里云短信服务Java客户端，封装SDK提供短信发送功能，支持验证码场景，依赖阿里云SDK。邮件发送模块封装SMTP协议，支持HTML邮件和SSL加密，依赖JavaMail。验证码管理模块定义业务类型和发送渠道枚举，无外部依赖。抽象验证码服务类提供生成、发送和校验功能，有效期2分钟。工厂类根据渠道返回短信或邮件客户端实例。抽象客户端和响应类提供基础封装，需子类实现具体逻辑。 |
| [common-wefe](common-wefe/src/main/java/com/_module.md) | module | 服务检查框架实现分层健康检测，枚举模块定义联邦学习类型状态，配置管理模块统一处理多源连接，数据类型推断器分析字段类型。 |
| [common-data-mongodb](common-data-mongodb/src/main/java/com/_module.md) | module | MongoDB数据访问层提供CRUD和复杂查询功能，支持逻辑删除和时间戳约束。包含短信业务分类、供应商枚举管理。工具集支持链式查询构建和聚合操作。联邦学习平台实现日志、证书和数据治理。统一查询管理数据集和成员认证。连接管理模块动态注册MongoDB组件。 |
| [common-data-storage](common-data-storage/src/main/java/com/_module.md) | module | DruidAbstractDataSource是Druid连接池核心抽象类，提供连接池配置、监控、线程安全等基础功能。多云存储模块支持异构数据库统一操作，包含分片、分页、流处理等能力，依赖主流云SDK和JDBC驱动。 |
| [common-web](common-web/src/main/java/com/_module.md) | module | 该模块集成了Web API开发框架，包含日志记录、用户活动管理、权限控制、流量限制、验证码服务、文档生成等核心功能。采用注解驱动和反射机制，支持多格式文档输出和自动化校验。通过线程安全设计和防御式编程保障稳定性，适用于多角色系统和微服务场景。 |
| [common-lang](common-lang/src/main/java/com/_module.md) | module | Java配置管理工具集，统一管理配置并提供类型安全接口。支持多环境配置加载和类型转换，依赖Log4j。数据处理工具集含Excel解析和文本批处理，支持ETL和日志分析。字段验证平台实现敏感数据脱敏和格式校验。基础常量模块定义密钥类型和压缩格式。通用工具库涵盖加密、集合操作等。HTTP通信模块管理文件下载和请求处理。压缩解压模块支持多格式处理。函数式接口支持Lambda操作。线程池管理工具提供任务执行功能。验证类检查数据类型合法性。状态码枚举定义系统错误码。安全工具生成随机盐值。时间间隔类处理时间计算。批量消费类实现数据批量处理。验证码生成类创建Base64验证码。信息大小类转换存储单位。数据类型转换类处理多种格式转换。采样日志类控制日志频率。计时工具类记录代码执行时间。 |


