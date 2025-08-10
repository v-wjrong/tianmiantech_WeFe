# 基础信息

|      |      |
|------|------|
| 名称 | welab |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/welab |
| 包名 | docs.manager.manager-service.src.main.java.com.welab |
| 概述说明 | 联盟链资源管理模块群，提供证书、数据、节点等全生命周期管理，采用RESTful接口和MongoDB+智能合约实现数据同步。支持成员注册、数据上传、权限设置等业务闭环，含文件检查、版本生成、对象映射转换等功能。依赖Spring、MongoDB、FISCO BCOS SDK，确保事务一致性与安全加密。 |

# 说明

## 概述  
该模块群是联盟链生态下的综合管理系统，核心职责包括多维资源（证书/数据/节点/成员）全生命周期管理和智能合约交互，类似企业级RBAC与分布式配置中心的结合体。接口规范采用分层设计：RESTful API层继承AbstractApi基类，智能合约层提供CRUD/事件订阅，配置层通过@PropertySource动态加载。关键数据结构涵盖视图对象（CertVO）、链上响应类（InsertEventResponse）、版本号字符串（vX.Y）及扩展JSON字段。外部依赖包括MongoDB驱动、FISCO BCOS SDK、MapStruct框架和国密算法库，例如通过CertOperationService实现链上链下状态同步。实现案例丰富，如DownloadFileApi结合GridFS，RealNameAuthAuditApi联动审核服务与智能合约。

## 主要业务场景  
模块支持联盟链全业务流程：1)成员注册→数据上传→权限设置的三段式协作；2)证书管理（信任库维护/状态同步）；3)数据资源标签化（分页查询/标签云生成）。交互模式多样：API层采用"参数校验→服务调用→结果转换"，合约层采用事件驱动（如文件上传触发insertEvent）。典型应用包括管理员通过UnionNode系列API维护节点列表，用户通过DataSetTagsApi生成标签云。功能完整性体现在各实体均具备状态管理、扩展属性和链下监听能力，例如MemberContract管理公钥，DataResourceContract验证权限。API类型全面覆盖查询类（QueryAllApi）、操作类（DeleteByTagId）和文件类（DownloadApi），形成配置加载→业务处理→区块链交互的闭环。


### 包内部结构视图

```mermaid
graph TD
    wefe --> manager
    manager --> service
    service --> api
    service --> contract
    service --> constant
    service --> util
    service --> mapper
    service --> service
    service --> dto
    service --> operation
    service --> task
    service --> listener
    service --> config
    service --> ManagerService.java
    api --> cert
    api --> account
    api --> authtype
    api --> dataresource
    api --> common
    api --> dataset
    api --> union
    api --> defaulttag
    api --> agreement
    api --> member
    cert --> QueryCertApi.java
    cert --> DetailCsrApi.java
    cert --> DownloadApi.java
    cert --> TrustCertsUpdateApi.java
    cert --> DetailKeyApi.java
    cert --> QueryCsrApi.java
    cert --> UpdateCertStatusApi.java
    cert --> InitApi.java
    cert --> QueryKeyApi.java
    cert --> DetailCertApi.java
    cert --> QueryTrustCertApi.java
    account --> SsoLoginApi.java
    authtype --> UpdateApi.java
    authtype --> DeleteApi.java
    authtype --> AddApi.java
    authtype --> QueryAllApi.java
    dataresource --> QueryApi.java
    dataresource --> DetailApi.java
    dataresource --> DataResourceTagsApi.java
    dataresource --> EnableApi.java
    common --> DownloadFileApi.java
    dataset --> UpdateExtJsonApi.java
    dataset --> QueryApi.java
    dataset --> DetailApi.java
    dataset --> DataSetTagsApi.java
    union --> UpdateApi.java
    union --> DeleteApi.java
    union --> QueryAllApi.java
    union --> EnableApi.java
    defaulttag --> QueryApi.java
    defaulttag --> UpdateApi.java
    defaulttag --> DeleteApi.java
    defaulttag --> AddApi.java
    agreement --> UploadRealnameAuthAgreementTemplateApi.java
    agreement --> QueryApi.java
    agreement --> EnableApi.java
    member --> QueryApi.java
    member --> UpdateApi.java
    member --> RealNameAuthAuditApi.java
    member --> RealNameAuthInfoQueryApi.java
    contract --> MemberAuthTypeContract.java
    contract --> DataSetContract.java
    contract --> TrustCertsContract.java
    contract --> MemberContract.java
    contract --> DataSetDefaultTagContract.java
    contract --> DataResourceContract.java
    contract --> RealnameAuthAgreementTemplateContract.java
    contract --> UnionNodeContract.java
    contract --> DataResourceDefaultTagContract.java
    contract --> DataSetMemberPermissionContract.java
    contract --> MemberFileInfoContract.java
    constant --> UserConstant.java
    util --> FileCheckerUtil.java
    util --> VersionUtil.java
    mapper --> ImageDataSetMapper.java
    mapper --> DataSetMapper.java
    mapper --> TableDataSetMapper.java
    mapper --> BloomFilterMapper.java
    mapper --> MemberMapper.java
    mapper --> DataResourceMapper.java
    mapper --> TrustCertsMapper.java
    mapper --> AccountMapper.java
    mapper --> RealnameAuthAgreementTemplateMapper.java
    mapper --> UnionNodeMapper.java
    service --> DataSetContractService.java
    service --> RealNameAuthAuditService.java
    service --> RealnameAuthAgreementTemplateContractService.java
    service --> AbstractContractService.java
    service --> AccountService.java
    service --> DataResourceDefaultTagContractService.java
    service --> DatSetDefaultTagContractService.java
    service --> TrustCertsContractService.java
    service --> MemberAuthTypeContractService.java
    service --> PrivacyDatabaseEncryptService.java
    service --> DataResourceContractService.java
    service --> UnionNodeContractService.java
    service --> MemberContractService.java
    dto --> cert
    dto --> account
    dto --> authtype
    dto --> dataresource
    dto --> tag
    dto --> common
    dto --> dataset
    dto --> union
    dto --> operation
    dto --> agreement
    dto --> member
    dto --> base
    cert --> TrustCertsQueryOutput.java
    cert --> TrustCertsAddInput.java
    account --> ResetPasswordInput.java
    account --> AccountEnableInput.java
    account --> UpdatePasswordInput.java
    account --> LoginOutput.java
    account --> LoginInput.java
    account --> AccountRoleChangeInput.java
    account --> QueryAccountInput.java
    account --> QueryAccountOutput.java
    account --> RegisterInput.java
    account --> UpdateInput.java
    authtype --> MemberAuthTypeDeleteInput.java
    authtype --> MemberAuthTypeAddInput.java
    authtype --> MemberAuthTypeUpdateInput.java
    dataresource --> ApiTableDataSetQueryOutput.java
    dataresource --> ApiBloomFilterQueryOutput.java
    dataresource --> ApiDataResourceQueryOutput.java
    dataresource --> ApiDataResourceDetailInput.java
    dataresource --> ApiImageDataSetQueryOutput.java
    dataresource --> ApiDataResourceQueryInput.java
    tag --> DataSetTagsQueryInput.java
    tag --> DataResourceDefaultTagUpdateInput.java
    tag --> ApiDataResourceDefaultTagQueryOutput.java
    tag --> DataResourceDefaultTagAddInput.java
    tag --> DataResourceDefaultTagDeleteInput.java
    tag --> ApiDataSetTagsQueryOutput.java
    tag --> TagsDTO.java
    common --> UploadFileInput.java
    common --> QueryFileInput.java
    dataset --> ApiDataSetQueryOutput.java
    dataset --> DataSetDetailInput.java
    dataset --> DataSetUpdateExtJsonInput.java
    dataset --> ApiDataSetQueryInput.java
    union --> UnionNodeQueryOutput.java
    union --> UnionNodeEnableInput.java
    union --> UnionNodeAddInput.java
    union --> UnionNodeUpdateInput.java
    union --> UnionNodeDeleteInput.java
    operation --> OperationLogQueryOutput.java
    operation --> OperationLogQueryInput.java
    agreement --> RealnameAuthAgreementTemplateEnableInput.java
    agreement --> RealnameAuthAgreementTemplateOutput.java
    member --> MemberUpdateInput.java
    member --> RealNameAuthInfoQueryInput.java
    member --> MemberQueryInput.java
    member --> MemberQueryOutput.java
    member --> RealNameAuthInput.java
    base --> BaseInput.java
    base --> BaseQueryInput.java
    base --> PageInput.java
    operation --> ManagerApiLogger.java
    task --> UploadFileSyncToUnionTask.java
    listener --> AutoPrivacyDatabaseEncryptListener.java
    config --> Config.java
    config --> BlockChainConfig.java
```

该流程图展示了WeFe管理服务的完整目录结构，从顶层wefe目录开始，逐级展开到具体的Java文件。主要包含api接口、contract合约、service服务、dto数据传输对象等核心模块，其中api模块下细分了cert证书、account账户等12个子模块，每个子模块包含多个具体API实现类。整体结构清晰展现了Spring Boot项目的标准分层架构，各模块职责分明，便于维护和扩展。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [wefe](wefe/_module.md) | package | 联盟链资源管理模块群，提供证书、数据、节点等全生命周期管理，采用RESTful接口和MongoDB+智能合约实现数据同步。支持成员注册、数据上传、权限设置等业务闭环，含文件检查、版本生成、对象映射转换等功能。依赖Spring、MongoDB、FISCO BCOS SDK，确保事务一致性与安全加密。 |


