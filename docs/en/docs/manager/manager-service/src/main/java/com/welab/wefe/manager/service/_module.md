# Basic Information

|      |      |
|------|------|
| Name | service |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service |
| Package Name | docs.manager.manager-service.src.main.java.com.welab.wefe.manager.service |
| Brief Description | The consortium chain resource management module cluster provides full lifecycle management of certificates, data, nodes, etc., utilizing RESTful interfaces and MongoDB + smart contracts for data synchronization. It supports business closed loops such as member registration, data upload, and permission settings, including functionalities like file inspection, version generation, and object mapping conversion. It relies on Spring, MongoDB, and FISCO BCOS SDK to ensure transaction consistency and secure encryption. |

# Description

## Overview  
This module group is a comprehensive management system within the consortium blockchain ecosystem, with core responsibilities including full lifecycle management of multi-dimensional resources (certificates/data/nodes/members) and smart contract interactions, akin to a combination of enterprise-level RBAC and a distributed configuration center. The interface specification adopts a layered design: the RESTful API layer inherits from the AbstractApi base class, the smart contract layer provides CRUD/event subscription, and the configuration layer dynamically loads via @PropertySource. Key data structures encompass view objects (CertVO), on-chain response classes (InsertEventResponse), version number strings (vX.Y), and extended JSON fields. External dependencies include the MongoDB driver, FISCO BCOS SDK, MapStruct framework, and national cryptographic algorithm libraries, such as achieving on-chain/off-chain state synchronization through CertOperationService. Implementation examples are abundant, such as DownloadFileApi integrating GridFS and RealNameAuthAuditApi linking audit services with smart contracts.  

## Core Business Scenarios  
The module supports the entire consortium blockchain workflow: 1) Three-stage collaboration of member registration → data upload → permission configuration; 2) Certificate management (trust store maintenance/state synchronization); 3) Data resource tagging (paged query/tag cloud generation). Interaction modes are diverse: the API layer adopts "parameter validation → service invocation → result transformation," while the contract layer employs event-driven mechanisms (e.g., file upload triggering insertEvent). Typical applications include administrators maintaining node lists via the UnionNode series of APIs and users generating tag clouds via DataSetTagsApi. Functional completeness is reflected in each entity possessing state management, extended attributes, and off-chain listening capabilities, such as MemberContract managing public keys and DataResourceContract validating permissions. API types comprehensively cover queries (QueryAllApi), operations (DeleteByTagId), and file handling (DownloadApi), forming a closed loop of configuration loading → business processing → blockchain interaction.


### Package Internal Structure View

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

This flowchart illustrates the complete directory structure of the WeFe Manager Service project, starting from the top-level service node and expanding into major modules such as api, contract, and dto. The api module includes submodules like cert and account, each containing specific API interface classes; the contract module comprises various contract classes; the dto module organizes input/output classes by functionality. The overall structure clearly reflects a modular business design philosophy, with distinct responsibilities and well-defined hierarchical relationships among modules, facilitating maintenance and extensibility.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [mapper](mapper/_module.md) | package | Multiple MapStruct mapping interfaces for converting between different types of objects, including functionalities such as field mapping, time formatting, and type conversion. |
| [service](service/_module.md) | package | The DataSetContractService updates dataset extension JSON, including query, reflection processing, blockchain transactions, and validation. The RealNameAuthAuditService handles real-name authentication audits, updating certificate statuses and member information. The RealnameAuthAgreementTemplateContractService manages the addition and activation of agreement templates. The AbstractContractService provides transaction result verification methods. The AccountService handles SSO account creation and updates. The DataResourceDefaultTagContractService and DataSetDefaultTagContractService manage tag additions, deletions, and modifications. The TrustCertsContractService processes certificate operations. The MemberAuthTypeContractService manages authentication types. The PrivacyDatabaseEncryptService encrypts private data. The DataResourceContractService updates data resource statuses. The UnionNodeContractService manages node operations. The MemberContractService handles member information updates and checks. |
| [ManagerService.java](ManagerService.md) | file | A SpringBoot application excludes data source and Mongo auto-configuration, enables scheduled tasks, customizes component scanning paths, and implements the ApplicationContextAware interface to save the context. The main method launches the application via Launcher. |
| [config](config/_module.md) | package | The Config class is a Spring component that inherits from CommonConfig, loads external configuration files with UTF-8 encoding, and manages application configurations. The BlockChainConfig class initializes blockchain configurations, including attributes such as certificate paths and group IDs, creates BcosSDK instances and contract services, and supports configuration injection. |
| [listener](listener/_module.md) | package | AutoPrivacyDatabaseEncryptListener monitors application startup events, automatically encrypts database data after checking configurations, logs activities, and handles exceptions. |
| [task](task/_module.md) | package | The `UploadFileSyncToUnionTask` class is designed for multi-threaded file uploads to a specified API, supporting 3 retries with incrementally increasing intervals. It handles parameters and file streams, and checks response status and return codes. |
| [operation](operation/_module.md) | package | The ManagerApiLogger inherits from AbstractApiLogger, ignores logs from UploadRealnameAuthAgreementTemplateApi, converts ApiLog to OperationLog and stores it in MongoDB, with the updateAccountLastActionTime method left unimplemented. |
| [dto](dto/_module.md) | package | 1. Trust Certificate Management Module: Responsible for certificate lifecycle management, supporting CRUD operations, including basic certificate information and hierarchical relationships.  2. Account Management Module: Handles registration, login, password reset, and other operations, adopting the standard DTO pattern with support for permission control.  3. Member Authentication Type Module: Manages the addition, deletion, modification, and querying of authentication types, validating mandatory fields through DTO.  4. Data Resource Module: Uniformly manages multiple data types, supporting paginated queries and detail retrieval.  5. Tag Management Module: Handles CRUD operations for tags, supporting paginated queries and statistics.  6. File Management Module: Manages file uploads and queries, encapsulating input parameters via POJO.  7. Dataset Module: Manages dataset metadata, supporting paginated queries and extended attribute updates.  8. Blockchain Node Module: Manages node information, supporting queries, enable/disable operations, and more.  9. Operation Log Module: Provides log query functionality, supporting pagination and conditional filtering.  10. Real-name Authentication Agreement Module: Manages template activation and output data, supporting status changes.  11. Member Information Module: Manages member information, supporting updates, queries, and real-name authentication.  12. Basic Input Module: Provides member ID management, status queries, and pagination control. |
| [util](util/_module.md) | package | The `FileCheckerUtil` class checks file types, allowing only PDFs; illegal files are deleted and an exception is thrown. The `VersionUtil` class generates version numbers, returning `v1.0` for empty input; otherwise, the major version remains unchanged while the minor version increments by 1. If the minor version ≥ 9, the major version increments by 1 and the minor version resets to zero. |
| [constant](constant/_module.md) | package | The user constants class contains static constants for administrator accounts and default passwords. |
| [contract](contract/_module.md) | package | The MemberAuthTypeContract manages member authentication types, providing CRUD functionality with support for ECDSA/SM2 encryption and event listening. The DataSetContract handles dataset operations, supporting CRUD and two encryption algorithms. The TrustCertsContract manages trusted certificates, enabling insert, query, and delete operations. The MemberContract manages member information, offering CRUD and event subscription capabilities. The DataSetDefaultTagContract manages dataset tags, supporting CRUD and event listening. The DataResourceContract manages data resources, providing CRUD and event subscription. The RealnameAuthAgreementTemplateContract manages real-name authentication templates, supporting CRUD and status updates. The UnionNodeContract manages consortium nodes, offering CRUD and event listening. The DataResourceDefaultTagContract manages data resource tags, enabling CRUD and event subscription. The DataSetMemberPermissionContract manages dataset member permissions, providing CRUD functionality. The MemberFileInfoContract manages member file information, supporting CRUD and event listening. |
| [api](api/_module.md) | package | The certificate management module provides full lifecycle management functions for certificates, including querying, downloading, updating status, and trust store maintenance. It supports three major scenarios: initialization, querying, and status management, relying on components such as CertOperationService. |


