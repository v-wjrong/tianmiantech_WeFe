# 基础信息

|      |      |
|------|------|
| 名称 | service |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service |
| 包名 | docs.manager.manager-service.src.main.java.com.welab.wefe.manager.service |
| 概述说明 | 联盟链资源管理模块群，提供证书、数据、节点等全生命周期管理，采用RESTful接口和MongoDB+智能合约实现数据同步。支持成员注册、数据上传、权限设置等业务闭环，含文件检查、版本生成、对象映射转换等功能。依赖Spring、MongoDB、FISCO BCOS SDK，确保事务一致性与安全加密。 |

# 说明

## 概述  
该模块群是联盟链生态下的综合管理系统，核心职责包括多维资源（证书/数据/节点/成员）全生命周期管理和智能合约交互，类似企业级RBAC与分布式配置中心的结合体。接口规范采用分层设计：RESTful API层继承AbstractApi基类，智能合约层提供CRUD/事件订阅，配置层通过@PropertySource动态加载。关键数据结构涵盖视图对象（CertVO）、链上响应类（InsertEventResponse）、版本号字符串（vX.Y）及扩展JSON字段。外部依赖包括MongoDB驱动、FISCO BCOS SDK、MapStruct框架和国密算法库，例如通过CertOperationService实现链上链下状态同步。实现案例丰富，如DownloadFileApi结合GridFS，RealNameAuthAuditApi联动审核服务与智能合约。

## 主要业务场景  
模块支持联盟链全业务流程：1)成员注册→数据上传→权限设置的三段式协作；2)证书管理（信任库维护/状态同步）；3)数据资源标签化（分页查询/标签云生成）。交互模式多样：API层采用"参数校验→服务调用→结果转换"，合约层采用事件驱动（如文件上传触发insertEvent）。典型应用包括管理员通过UnionNode系列API维护节点列表，用户通过DataSetTagsApi生成标签云。功能完整性体现在各实体均具备状态管理、扩展属性和链下监听能力，例如MemberContract管理公钥，DataResourceContract验证权限。API类型全面覆盖查询类（QueryAllApi）、操作类（DeleteByTagId）和文件类（DownloadApi），形成配置加载→业务处理→区块链交互的闭环。


### 包内部结构视图

```mermaid
graph TD
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

该流程图展示了WeFe Manager Service项目的完整目录结构，从顶层service节点开始，逐级展开api、contract、dto等主要模块。api模块下包含cert、account等子模块，每个子模块包含具体的API接口类；contract模块包含各类合约类；dto模块按功能划分输入输出类。整体结构清晰体现了业务模块化设计思想，各模块职责分明，层级关系明确，便于维护和扩展。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [mapper](mapper/_module.md) | package | 多个MapStruct映射接口，用于不同类型对象转换，包含字段映射、时间格式化和类型转换等功能。 |
| [service](service/_module.md) | package | DataSetContractService更新数据集扩展JSON，含查询、反射处理、区块链交易和验证。RealNameAuthAuditService处理实名认证审核，更新证书状态和成员信息。RealnameAuthAgreementTemplateContractService管理协议模板的添加和启用。AbstractContractService提供交易结果检查方法。AccountService处理SSO账户创建和更新。DataResourceDefaultTagContractService和DatSetDefaultTagContractService管理标签增删改。TrustCertsContractService处理证书操作。MemberAuthTypeContractService管理认证类型。PrivacyDatabaseEncryptService加密隐私数据。DataResourceContractService更新数据资源状态。UnionNodeContractService管理节点操作。MemberContractService处理会员信息更新和检查。 |
| [ManagerService.java](ManagerService.md) | file | SpringBoot应用排除数据源和Mongo自动配置，启用定时任务，自定义组件扫描路径，实现ApplicationContextAware接口保存上下文。主方法通过Launcher启动应用。 |
| [config](config/_module.md) | package | Config类为Spring组件，继承CommonConfig，加载外部UTF-8编码配置文件，管理应用配置。BlockChainConfig类初始化区块链配置，包含证书路径、组ID等属性，创建BcosSDK实例和合约服务，支持配置注入。 |
| [listener](listener/_module.md) | package | AutoPrivacyDatabaseEncryptListener监听应用启动事件，检查配置后自动加密数据库数据，记录日志并处理异常。 |
| [task](task/_module.md) | package | UploadFileSyncToUnionTask类用于多线程上传文件到指定API，支持3次重试，每次间隔递增，处理参数和文件流，检查响应状态和返回码。 |
| [operation](operation/_module.md) | package | ManagerApiLogger继承AbstractApiLogger，忽略UploadRealnameAuthAgreementTemplateApi日志，将ApiLog转为OperationLog并存储至MongoDB，未实现updateAccountLastActionTime方法。 |
| [dto](dto/_module.md) | package | 1. 信任证书管理模块：负责证书生命周期管理，支持CRUD操作，包含证书基础信息和层级关系。  2. 账户管理模块：处理注册、登录、密码重置等操作，采用标准DTO模式，支持权限控制。  3. 成员认证类型模块：管理认证类型的增删改查，通过DTO校验必填字段。  4. 数据资源模块：统一管理多种数据类型，支持分页查询和详情获取。  5. 标签管理模块：处理标签的CRUD操作，支持分页查询和统计。  6. 文件管理模块：处理文件上传和查询，通过POJO封装输入参数。  7. 数据集模块：管理数据集元信息，支持分页查询和扩展属性更新。  8. 区块链节点模块：管理节点信息，支持查询、启用/禁用等操作。  9. 操作日志模块：提供日志查询功能，支持分页和条件筛选。  10. 实名认证协议模块：管理模板启用与输出数据，支持状态变更。  11. 成员信息模块：管理成员信息，支持更新、查询和实名认证。  12. 基础输入模块：提供成员ID管理、状态查询和分页控制。 |
| [util](util/_module.md) | package | FileCheckerUtil类检查文件类型，仅允许pdf，非法则删除并抛异常。VersionUtil类生成版本号，空输入返回v1.0，否则主版本号不变次版本号加1，次版本≥9则主版本加1次版本归零。 |
| [constant](constant/_module.md) | package | 用户常量类包含管理员账户和默认密码的静态常量。 |
| [contract](contract/_module.md) | package | MemberAuthTypeContract管理成员认证类型，提供增删改查功能，支持ECDSA/SM2加密和事件监听。DataSetContract操作数据集，支持增删改查和两种加密算法。TrustCertsContract管理可信证书，支持插入、查询和删除操作。MemberContract管理成员信息，提供增删改查和事件订阅功能。DataSetDefaultTagContract管理数据集标签，支持增删改查和事件监听。DataResourceContract管理数据资源，提供增删改查和事件订阅。RealnameAuthAgreementTemplateContract管理实名认证模板，支持增删改查和状态更新。UnionNodeContract管理联盟节点，提供增删改查和事件监听。DataResourceDefaultTagContract管理数据资源标签，支持增删改查和事件订阅。DataSetMemberPermissionContract管理数据集成员权限，提供增删改查功能。MemberFileInfoContract管理成员文件信息，支持增删改查和事件监听。 |
| [api](api/_module.md) | package | 证书管理模块提供证书全生命周期管理功能，包括查询、下载、更新状态及信任库维护。支持初始化、查询、状态管理三大场景，依赖CertOperationService等组件。 |


