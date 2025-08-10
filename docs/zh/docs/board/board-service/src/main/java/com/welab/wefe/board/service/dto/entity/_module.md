# 基础信息

|      |      |
|------|------|
| 名称 | entity |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity |
| 包名 | docs.board.board-service.src.main.java.com.welab.wefe.board.service.dto.entity |
| 概述说明 | 该模块提供联邦学习项目的数据资源管理、任务流编排、成员协作及状态跟踪功能。采用Java Bean模式，通过继承和注解实现标准化接口，支持数据生命周期管理和多场景应用。 |

# 说明

## 概述  
该模块核心职责是构建联邦学习全生命周期管理体系，类似工作流引擎与数据中台的混合模式，统一管理项目协同、任务编排、数据资源和成员交互。接口规范采用Java Bean模式，通过继承AbstractOutputModel实现字段复用，配合@Check注解校验和JSON序列化控制。关键数据结构包括四层模型体系：基础类（如ProjectOutputModel）、流程类（如JobOutputModel）、成员类（如MemberOutputModel）和衍生类（如BloomFilterDataResourceListOutputModel）。外部依赖主要为Spring校验框架和ModelMapper，例如通过ModelMapper实现MySql模型到输出模型的转换。

## 主要业务场景  
模块支撑联邦学习全流程协同，典型场景包括：1）项目看板（聚合流程状态与数据集统计）；2）任务编排（如ProjectFlowNodeOutputModel定义DAG关系）；3）数据治理（如DataSetOutputModel分析特征分布）。交互模式类似多租户SaaS系统，通过标准化模型传递状态变更，例如BlacklistOutputModel同步成员状态。API涵盖资源查询（getStorageNamespace）、参数配置（如逻辑回归学习率）和进度跟踪（progressPercentage）。集成案例包括网关推送任务拓扑和数据看板实时同步。


### 包内部结构视图

```mermaid
graph TD
    entity --> data_resource
    entity --> job
    entity --> modeling_config
    entity --> data_set
    entity --> project
    entity --> component
    entity --> BlacklistOutputModel.java
    entity --> ProjectDataSetInput.java
    entity --> MemberOutputModel.java
    entity --> ProjectMemberAuditOutput.java
    entity --> MessageOutputModel.java
    entity --> OperationLogOutputModel.java
    entity --> MemberFeatureInfoModel.java
    entity --> ProjectMemberInput.java
    entity --> DataIoTaskFeatureInfoOutputModel.java
    entity --> MemberModel.java
    entity --> AccountListAllOutputModel.java
    entity --> AbstractOutputModel.java
    entity --> AccountOutputModel.java
    entity --> MemberChatOutputModel.java
    entity --> PartnerConfigOutputModel.java
    entity --> ChatLastAccountOutputModel.java
    entity --> BloomFilterDataResourceListOutputModel.java
    data_resource --> output
    output --> ImageDataSetOutputModel.java
    output --> TableDataSetOutputModel.java
    output --> DataResourceUploadTaskOutputModel.java
    output --> BloomFilterOutputModel.java
    output --> DataResourceOutputModel.java
    job --> gateway
    job --> RelateDataSetOutputModel.java
    job --> TaskOutputModel.java
    job --> ProjectFlowNodeOutputModel.java
    job --> PreviewJobNodeOutputModel.java
    job --> JobOutputModel.java
    job --> TaskProgressOuputModel.java
    job --> TaskResultOutputModel.java
    job --> TaskOutputView.java
    job --> JobMemberOutputModel.java
    job --> JobListOutputModel.java
    gateway --> ProjectForGatewayDataSetOutputModel.java
    gateway --> ProjectForGatewayMemberOutputModel.java
    modeling_config --> ModelingConfigLogisticRegressionOutputModel.java
    modeling_config --> AbstractModelingConfigOutputModel.java
    modeling_config --> ModelingInfoOutputModel.java
    data_set --> ImageDataSetSampleOutputModel.java
    data_set --> DataSetColumnOutputModel.java
    data_set --> DataSetOutputModel.java
    data_set --> DataSetColumnInputModel.java
    project --> ProjectFlowListOutputModel.java
    project --> ProjectModelingOutputModel.java
    project --> ProjectMemberOutputModel.java
    project --> ProjectFlowDetailOutputModel.java
    project --> data_set
    project --> ProjectQueryOutputModel.java
    project --> ProjectDetailMemberOutputModel.java
    project --> ProjectFlowOutputModel.java
    project --> ProjectOutputModel.java
    project --> ProjectFlowProgressOutputModel.java
    project --> ProjectUsageDetailOutputModel.java
    data_set --> DerivedProjectDataSetOutputModel.java
    data_set --> ProjectDataResourceOutputModel.java
    component --> ComponentOutputModel.java
```

该流程图展示了WeFe项目中board-service模块的DTO实体类层级结构。根节点为entity，下分data_resource、job、modeling_config等主要子模块。每个子模块包含具体的输出模型类，如data_resource/output下的各种资源输出模型，job模块包含任务、项目流程等相关模型。整体结构清晰展现了数据流转和业务模块间的关联关系，共包含50余个节点，完整覆盖了项目中的数据传输对象定义。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [BlacklistOutputModel.java](BlacklistOutputModel.md) | file | BlacklistOutputModel类包含ID、会员ID、姓名、备注、创建者和创建时间字段，提供getter和setter方法。 |
| [ProjectDataSetInput.java](ProjectDataSetInput.md) | file | ProjectDataSetInput类继承AbstractCheckModel，包含成员ID、角色、数据集ID和类型字段，均需校验非空，并提供getter/setter方法。 |
| [MemberOutputModel.java](MemberOutputModel.md) | file | 成员输出模型类，包含ID、姓名、手机、邮箱和黑名单状态字段及对应getter/setter方法。 |
| [ProjectMemberAuditOutput.java](ProjectMemberAuditOutput.md) | file | ProjectMemberAuditOutput类用于项目成员审核，包含项目ID、成员ID、审核人ID、审核结果（adopt/disagree）和审核意见字段，提供getter/setter方法。 |
| [MessageOutputModel.java](MessageOutputModel.md) | file | 消息输出模型类，包含生产者、级别、事件、标题、内容、未读状态、待办事项及完成状态等属性及对应getter/setter方法。 |
| [OperationLogOutputModel.java](OperationLogOutputModel.md) | file | OperationLogOutputModel类继承AbstractOutputModel，包含日志接口、名称、IP、操作员ID、token、行为、结果编码和消息等字段，提供getter和setter方法。 |
| [MemberFeatureInfoModel.java](MemberFeatureInfoModel.md) | file | MemberFeatureInfoModel继承MemberModel，包含必填特征列表features和数据集ID dataSetId。Feature类有特征名name、cv、iv、缺失率missingRate和方法method等属性。 |
| [ProjectMemberInput.java](ProjectMemberInput.md) | file | ProjectMemberInput类包含成员ID、角色和数据集列表字段，提供getter/setter方法，成员ID为必填项。 |
| [DataIoTaskFeatureInfoOutputModel.java](DataIoTaskFeatureInfoOutputModel.md) | file | 数据IO任务特征信息输出模型，包含成员ID、名称、角色、数据集ID及特征列列表。 |
| [MemberModel.java](MemberModel.md) | file | MemberModel类继承AbstractCheckModel，包含必填成员id、可选成员名和必填成员角色字段，提供各字段的getter和setter方法。 |
| [AccountListAllOutputModel.java](AccountListAllOutputModel.md) | file | AccountListAllOutputModel类包含用户昵称、超级管理员标识、管理员标识、审核状态、可用状态及注销状态字段及其getter/setter方法。 |
| [AbstractOutputModel.java](AbstractOutputModel.md) | file | AbstractOutputModel类包含ID、创建/更新人和时间等字段，通过set方法自动设置创建者和更新者昵称。 |
| [AccountOutputModel.java](AccountOutputModel.md) | file | AccountOutputModel类包含用户账号信息，如手机号、昵称、邮箱、管理员角色、审核状态及最后活动时间等字段，并提供getter/setter方法。 |
| [MemberChatOutputModel.java](MemberChatOutputModel.md) | file | 成员聊天输出模型类，包含发送接收方账号ID、成员ID、聊天内容、消息状态及消息ID等字段及其getter/setter方法。 |
| [PartnerConfigOutputModel.java](PartnerConfigOutputModel.md) | file | PartnerConfigOutputModel类继承AbstractOutputModel，包含memberId和gatewayAddress字段及其getter/setter方法，提供getMemberName方法通过CacheObjects获取成员名称。 |
| [ChatLastAccountOutputModel.java](ChatLastAccountOutputModel.md) | file | ChatLastAccountOutputModel类包含账户、成员及联络人信息，以及未读消息数。提供各字段的getter和setter方法。 |
| [BloomFilterDataResourceListOutputModel.java](BloomFilterDataResourceListOutputModel.md) | file | BloomFilter数据资源列表输出模型，包含项目ID、身份角色、成员ID及数据集列表字段。 |
| [modeling_config](modeling_config/_module.md) | package | 逻辑回归配置类含初始化、惩罚、优化等参数，继承类含名称、模式、删除标记字段，建模信息类含任务ID、流程、组件等字段，均提供getter/setter方法。 |
| [data_set](data_set/_module.md) | package | ImageDataSetSampleOutputModel处理图像样本输出，含ID、文件名、标签等字段，提供校验和getter/setter。DataSetColumnOutputModel描述数据集列，含字段名、类型、分布等属性。DataSetOutputModel包含数据集基本信息、特征、可见性等，管理使用次数和来源。DataSetColumnInputModel校验字段名、类型和注释，提供标准方法。 |
| [project](project/_module.md) | package | ProjectFlowListOutputModel类封装项目流程列表信息，包含状态、类型、ID等属性。ProjectModelingOutputModel类用于建模输出数据，含流程ID、任务ID等。ProjectMemberOutputModel类描述成员信息，含ID、角色、审核状态等。ProjectFlowDetailOutputModel类扩展流程详情，含项目信息、空参数节点等。ProjectQueryOutputModel类包含项目查询结果，含ID、名称、状态等。ProjectDetailMemberOutputModel类扩展成员信息，增加数据资源列表。ProjectFlowOutputModel类表示流程输出，含状态、类型、ID等。ProjectOutputModel类封装项目输出，含ID、名称、审核状态等。ProjectFlowProgressOutputModel类表示流程进度，含状态、更新时间等。ProjectUsageDetailOutputModel类封装项目使用详情，含ID、名称、时间等。 |
| [component](component/_module.md) | package | ComponentOutputModel类包含id、name、desc三个属性，分别表示组件唯一标识、中文名称和描述，提供构造方法和getter/setter。 |
| [job](job/_module.md) | package | 该模块管理联邦学习网关项目的数据集和成员信息，包含结构化数据定义和状态追踪。关键数据结构包括数据集元信息、成员角色和审核状态枚举。支持成员角色审核和数据集特征校验等业务场景，通过数据实体类实现联合状态管理。 |
| [data_resource](data_resource/_module.md) | package | ImageDataSetOutputModel继承DataResourceOutputModel，含任务类型、标签列表、标注状态等字段。TableDataSetOutputModel描述数据集属性，如列名、特征、标签分布等。DataResourceUploadTaskOutputModel记录上传任务信息，包括进度、状态等。BloomFilterOutputModel处理布隆过滤器相关数据。DataResourceOutputModel为基类，包含资源基本信息、使用统计等。 |


