# 基础信息

|      |      |
|------|------|
| 名称 | actuator |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/fusion/actuator |
| 包名 | docs.board.board-service.src.main.java.com.welab.wefe.board.service.api.project.fusion.actuator |
| 概述说明 | DownloadBFApi类处理布隆过滤器下载，路径fusion/psi/download_bloom_filter。ReceiveResultApi类接收结果，路径fusion/receive/result。ServerSynStatusApi类查询服务器状态，路径fusion/psi/server_is_ready。ServerCloseApi类处理服务器关闭，路径fusion/server/close。PsiCryptoApi类处理PSI加密，路径fusion/psi/crypto。均需签名访问，使用businessId标识业务。 |

# 说明

## 概述  
该模块提供PSI（隐私集合求交）协议执行过程中的核心API，类似分布式任务协调器，统一管理布隆过滤器下载、状态同步、结果接收等流程。所有API均继承自AbstractApi基类，支持签名访问，通过businessId关联ServerActuator实例实现状态跟踪。关键数据结构包括PsiActuatorMeta（执行元数据）、JObject（状态响应）和PSIActuatorStatus（枚举）。依赖项为统一的ActuatorManager执行器管理组件。例如DownloadBFApi返回布隆过滤器参数，PsiCryptoApi处理加密数据转换。

## 主要业务场景  
模块支持端到端PSI协议执行，类似多阶段事务处理：先通过ServerSynStatusApi轮询服务状态，再经PsiCryptoApi完成数据加密，最终由ReceiveResultApi聚合结果。典型交互模式为客户端携带businessId发起链式调用，服务端通过ActuatorManager维持会话状态。API分为三类：数据操作型（如DownloadBFApi）、状态控制型（如ServerCloseApi）和结果处理型（如ReceiveResultApi）。例如关闭请求会更新PSIActuatorStatus，而结果接收API将数据透传给执行器实例。


### 包内部结构视图

```mermaid
graph TD
    actuator --> psi
    psi --> DownloadBFApi.java
    psi --> ReceiveResultApi.java
    psi --> ServerSynStatusApi.java
    psi --> ServerCloseApi.java
    psi --> PsiCryptoApi.java
```

该流程图展示了WeFe项目中融合执行器(actuator)下的PSI相关API结构。顶层是actuator目录，其下包含psi子目录，psi目录中包含了5个具体的API实现类文件，包括下载BF文件、接收结果、服务器同步状态等功能的接口实现。所有节点都只显示路径最后一级名称，层级关系清晰。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [psi](psi/_module.md) | package | DownloadBFApi类处理布隆过滤器下载，路径fusion/psi/download_bloom_filter。ReceiveResultApi类接收结果，路径fusion/receive/result。ServerSynStatusApi类查询服务器状态，路径fusion/psi/server_is_ready。ServerCloseApi类处理服务器关闭，路径fusion/server/close。PsiCryptoApi类处理PSI加密，路径fusion/psi/crypto。均需签名访问，使用businessId标识业务。 |


