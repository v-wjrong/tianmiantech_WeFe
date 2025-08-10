# Basic Information

|      |      |
|------|------|
| Name | wefe |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe |
| Package Name | docs.manager.manager-service.src.main.java.com.welab.wefe |
| Brief Description | The consortium chain resource management module cluster provides full lifecycle management for certificates, data, nodes, etc., utilizing RESTful interfaces and MongoDB + smart contracts to achieve data synchronization. It supports business closed loops such as member registration, data upload, and permission settings, including functionalities like file inspection, version generation, and object mapping conversion. It relies on Spring, MongoDB, and FISCO BCOS SDK to ensure transaction consistency and secure encryption. |

# Description

## Overview  
This module group is a comprehensive management system within the consortium blockchain ecosystem, with core responsibilities including full lifecycle management of multidimensional resources (certificates/data/nodes/members) and smart contract interactions, akin to a combination of enterprise-grade RBAC and a distributed configuration center. The interface specification adopts a layered design: the RESTful API layer inherits the AbstractApi base class, the smart contract layer provides CRUD/event subscription capabilities, and the configuration layer dynamically loads via @PropertySource. Key data structures include view objects (CertVO), on-chain response classes (InsertEventResponse), version number strings (vX.Y), and extended JSON fields. External dependencies encompass the MongoDB driver, FISCO BCOS SDK, MapStruct framework, and the national cryptographic algorithm library, such as achieving on-chain/off-chain state synchronization through CertOperationService. Implementation examples are abundant, such as DownloadFileApi integrating GridFS and RealNameAuthAuditApi linking audit services with smart contracts.

## Core Business Scenarios  
The module supports the entire consortium blockchain workflow: 1) A three-stage collaboration of member registration → data upload → permission configuration; 2) Certificate management (trust store maintenance/status synchronization); 3) Data resource tagging (paged query/tag cloud generation). Interaction modes are diverse: the API layer follows a "parameter validation → service invocation → result transformation" pattern, while the contract layer employs event-driven mechanisms (e.g., file upload triggering insertEvent). Typical applications include administrators maintaining node lists via the UnionNode series of APIs and users generating tag clouds via DataSetTagsApi. Functional completeness is reflected in each entity's capabilities for state management, extended attributes, and off-chain listening, such as MemberContract managing public keys and DataResourceContract verifying permissions. API types comprehensively cover query classes (QueryAllApi), operation classes (DeleteByTagId), and file classes (DownloadApi), forming a closed loop of configuration loading → business processing → blockchain interaction.


### Package Internal Structure View

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
    service --> ManagerService.java
```

This flowchart presents the complete directory structure of the WeFe management service, starting from the top-level wefe node and hierarchically expanding to specific Java files. It primarily includes core modules such as api, contract, service, and dto. The api module is further subdivided into 12 submodules including cert and account, each containing multiple API interface files. The contract module comprises 11 contract classes, while the service module includes 13 service classes. The overall structure clearly demonstrates the layered design and functional partitioning of the backend service, involving a total of 200+ file nodes, fully showcasing the modular organization of the microservices architecture.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [manager](manager/_module.md) | package | The consortium chain resource management module cluster provides full lifecycle management for certificates, data, nodes, etc., utilizing RESTful interfaces and MongoDB + smart contracts to achieve data synchronization. It supports business closed loops such as member registration, data upload, and permission settings, including functions like file inspection, version generation, and object mapping conversion. It relies on Spring, MongoDB, and FISCO BCOS SDK to ensure transaction consistency and secure encryption. |


