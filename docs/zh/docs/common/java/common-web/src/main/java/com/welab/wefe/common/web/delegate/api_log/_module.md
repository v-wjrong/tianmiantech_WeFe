# 基础信息

|      |      |
|------|------|
| 名称 | api_log |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/delegate/api_log |
| 包名 | docs.common.java.common-web.src.main.java.com.welab.wefe.common.web.delegate.api_log |
| 概述说明 | ApiLog类记录API调用日志，包含请求响应信息。ApiCallerType枚举定义调用者类型，目前仅支持User。AbstractApiLogger抽象类管理日志和用户活动时间，提供忽略API列表和更新功能。 |

# 说明

## 概述  
该模块核心职责是规范化和记录API调用日志，同时管理用户活动时间。接口规范包括日志记录抽象方法save/updateAccountLastActionTime，以及忽略规则控制方法ignoreWithoutLogin。关键数据结构为ApiLog日志实体（含请求/响应全链路字段）和ConcurrentHashMap存储的用户活动时间表。外部依赖仅涉及Java基础并发库。例如通过静态IGNORE_LOG_APIS列表实现白名单过滤，类似事件总线模式的消息筛选机制。

## 主要业务场景  
典型场景为API网关拦截请求后，通过AbstractApiLogger自动记录带调用者信息的结构化日志（例如User类型+IP+耗时），同时维护用户活跃状态。交互模式采用"执行后拦截"机制，结合线程池异步处理日志持久化。完整功能涵盖日志字段装配、访问频控（如5分钟间隔更新活动时间）、白名单过滤等。集成案例表现为通过枚举限定调用者类型，预留未来扩展第三方应用类型的能力。


### 包内部结构视图

```mermaid
graph TD
    api_log --> ApiLog.java
    api_log --> ApiCallerType.java
    api_log --> AbstractApiLogger.java
```

该流程图展示了api_log目录下的三个Java文件之间的层级关系。api_log作为父节点，包含ApiLog.java、ApiCallerType.java和AbstractApiLogger.java三个子节点文件，清晰地呈现了该模块中API日志相关类的组织结构。所有节点名称均采用路径最后一级元素，符合规范要求。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [ApiLog.java](ApiLog.md) | file | ApiLog类记录API调用信息，包括接口名、调用者类型、ID、名称、IP、请求参数、响应码、消息、内容、请求和响应时间及耗时。提供getter/setter方法。 |
| [ApiCallerType.java](ApiCallerType.md) | file | 枚举类型ApiCallerType定义了一个成员User，表示API调用者类型。 |
| [AbstractApiLogger.java](AbstractApiLogger.md) | file | 抽象类AbstractApiLogger实现API日志记录，包含忽略日志API列表、用户最后活动时间更新及日志保存功能，支持异步处理和参数过滤。 |


