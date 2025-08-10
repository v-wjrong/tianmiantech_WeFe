# 基础信息

|      |      |
|------|------|
| 名称 | request |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/psi/request |
| 包名 | docs.mpc.mpc-common.src.main.java.com.welab.wefe.mpc.psi.request |
| 概述说明 | QueryPrivateSetIntersectionRequest类封装私有集合交集请求参数，含clientIds等字段及getter/setter。QueryPrivateSetIntersectionResponse类表示响应结果，含加密ID列表、状态码等字段及getter/setter。 |

# 说明

## 概述  
该模块核心职责是处理私有集合交集(PSI)查询的请求与响应封装，类似数据交换协议模式。接口规范包含QueryPrivateSetIntersectionRequest请求类（含p参数、clientIds列表等字段）和QueryPrivateSetIntersectionResponse响应类（含加密ID列表、批次状态等字段）。关键数据结构包括客户端ID列表、批次控制参数和PSI类型标识。外部依赖仅涉及JSON序列化库。例如请求类使用JSONField注解处理字段映射。

## 主要业务场景  
模块支持分批次PSI查询场景，通过currentBatch和batchSize实现数据流式处理。交互模式为请求-响应模型，例如客户端提交带类型标识的请求，服务端返回加密结果和批次状态。典型应用包括跨机构数据安全比对，通过clientIds实现多方标识匹配。API类型为POJO实体类，集成案例表现为请求/响应对象的序列化传输。例如响应类通过hasNextBatch标志控制查询终止条件。


### 包内部结构视图

```mermaid
graph TD
    request --> QueryPrivateSetIntersectionRequest.java
    request --> QueryPrivateSetIntersectionResponse.java
```

该流程图展示了WeFe项目中mpc-common模块下psi/request目录的层级结构。根节点为request文件夹，包含两个Java文件：QueryPrivateSetIntersectionRequest和QueryPrivateSetIntersectionResponse，分别表示私有集合交集查询的请求和响应类文件。结构清晰地反映了请求响应模型的文件组织方式。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [QueryPrivateSetIntersectionRequest.java](QueryPrivateSetIntersectionRequest.md) | file | QueryPrivateSetIntersectionRequest类包含私有集合交集查询请求的参数：p、clientIds、requestId、currentBatch、batchSize和type，提供各字段的getter和setter方法。 |
| [QueryPrivateSetIntersectionResponse.java](QueryPrivateSetIntersectionResponse.md) | file | 私有集合交集查询响应类，包含请求ID、加密ID列表、客户端ID列表、字段结果、当前批次、是否有下一批次、消息和状态码。 |


