# Basic Information

|      |      |
|------|------|
| Name | api |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api |
| Package Name | docs.board.board-service.src.main.java.com.welab.wefe.board.service.api |
| Brief Description | GenerateRsaKeyPairApi generates RSA key pairs and returns the public key. The global configuration module provides configuration update and query functions. The account management module handles member information queries and UI configuration updates. The online demo module supports URL generation and account verification. The data resource module manages the lifecycle of multimodal data. The chat system module provides message sending/receiving and status updates. The message module supports CRUD operations for messages. The service status module checks version and availability. The blacklist module manages member additions, deletions, and queries. The partner configuration module handles CRUD operations. The file module implements upload merging and security checks. The gateway module provides connection checks and task queries. The model output module handles model deployment and file exports. The alliance module manages data resources and member authentication. The log module queries operation records. The federated learning module manages the entire project lifecycle. The data source module provides CRUD and connection testing. The member module manages alliance member information. The inference module supports the complete model inference workflow. The component module retrieves filtered component lists. |

# Description

## Overview  
The core responsibility of this module system is to construct the backend service matrix for a federated learning platform, covering four key domains: data governance (key generation/resource management), member collaboration (account/authentication), task orchestration (project/workflow), and system operations (configuration/monitoring), analogous to the control plane of a distributed system. The interface specifications uniformly adopt the RESTful style, with hierarchical inheritance from the AbstractApi base class. Paths are organized by functional domains (e.g., `crypto/`, `project/`), and inputs/outputs are structured via nested classes. Key data structures include three types of models: validation classes (e.g., Input annotated with `@Check`), pagination classes (e.g., PagingOutput), and business entity classes (e.g., AccountOutputModel). External dependencies are centralized into domain-specific Service layers (e.g., GlobalConfigService) and infrastructure components (e.g., AES/RSA encryption libraries). For example, GenerateRsaKeyPairApi manages keys via TempRsaCache, while DataResourceDetailApi returns JSONObject resource details.

## Key Business Scenarios  
The module supports end-to-end federated learning scenarios: 1) Secure initialization (RSA key generation → member authentication → gateway connection testing); 2) Collaborative modeling (project creation → dataset addition → workflow orchestration → inference service deployment); 3) System operations (hot configuration updates → log auditing → file chunk uploads). The interaction mode combines synchronous API calls (e.g., CRUD operations) with asynchronous workflows (e.g., ModelExportToFileApi), driven similarly to a workflow engine. Typical applications include: key management center (GenerateRsaKeyPairApi), member management backend (QueryMemberAccountsApi), modeling monitoring console (GetProgressApi), and risk control module (BlacklistMemberApi). Functional completeness is reflected in cross-module coordination, such as project deletion triggering data cleanup or model exports synchronously pushing keys to the Serving system.


### Package Internal Structure View

```mermaid
graph TD
    api --> crypto
    api --> global_config
    api --> account
    api --> online_demo
    api --> data_resource
    api --> storage
    api --> chat
    api --> dev
    api --> message
    api --> service
    api --> blacklist
    api --> partner_config
    api --> file
    api --> gateway
    api --> data_output_info
    api --> union
    api --> operation
    api --> project
    api --> datasource
    api --> member
    api --> model
    api --> component

    crypto --> GenerateRsaKeyPairApi.java
    global_config --> GlobalConfigUpdateApi.java
    global_config --> GetGlobalConfigApi.java
    account --> QueryMemberAccountsApi.java
    account --> QueryOnlineApi.java
    account --> ListAllApi.java
    account --> UpdateUiConfigApi.java
    account --> SsoLoginApi.java
    online_demo --> TianmiantechPageApi.java
    online_demo --> CheckAccountExistApi.java
    online_demo --> TianmiantechCallApi.java
    online_demo --> CreateOnlineDemoAccountApi.java
    data_resource --> table_data_set
    data_resource --> upload_task
    data_resource --> bloom_filter
    data_resource --> image_data_set
    data_resource --> UsageInProjectListApi.java
    data_resource --> ListTagsApi.java
    data_resource --> DataResourceQueryApi.java
    table_data_set --> column
    table_data_set --> ListServerLocalFilesApi.java
    table_data_set --> UpdateApi.java
    table_data_set --> AddApi.java
    table_data_set --> TableDataSetDeleteApi.java
    table_data_set --> DetailApi.java
    table_data_set --> PreviewApi.java
    column --> ListApi.java
    upload_task --> DataResourceUploadTaskDetailApi.java
    upload_task --> DataResourceUploadTaskQueryApi.java
    bloom_filter --> BloomFilterPreviewApi.java
    bloom_filter --> BloomFilterDeleteApi.java
    bloom_filter --> BloomFilterDataResourceListApi.java
    bloom_filter --> BloomFilterDetailApi.java
    bloom_filter --> BloomFilterAddApi.java
    bloom_filter --> BloomFilterUpdateApi.java
    image_data_set --> sample
    image_data_set --> ImageDataSetUpdateApi.java
    image_data_set --> ImageDataSetAddApi.java
    image_data_set --> ImageDataSetDetailApi.java
    image_data_set --> ImageDataSetDownloadApi.java
    image_data_set --> ImageDataSetDeleteApi.java
    sample --> ImageDataSetSampleDeleteApi.java
    sample --> ImageDataSetSampleQueryApi.java
    sample --> ImageDataSetSampleDownloadApi.java
    sample --> ImageDataSetSampleUpdateApi.java
    sample --> ImageDataSetSampleStatisticsApi.java
    storage --> PreviewDataSetApi.java
    chat --> QueryChatLastAccountApi.java
    chat --> AddChatLastAccountApi.java
    chat --> SendMessageApi.java
    chat --> UpdateToReadApi.java
    chat --> QueryChatDetailApi.java
    chat --> UnreadMessageIncreaseOneApi.java
    chat --> ResendMessageApi.java
    chat --> DeleteChatLastAccountApi.java
    dev --> ShowConfigApi.java
    message --> QueryApi.java
    message --> ReadApi.java
    message --> DetailApi.java
    service --> VersionApi.java
    service --> ServiceAvailableApi.java
    service --> AliveApi.java
    blacklist --> BlacklistApi.java
    blacklist --> BlacklistMemberApi.java
    blacklist --> DeleteApi.java
    blacklist --> AddApi.java
    partner_config --> QueryApi.java
    partner_config --> DeleteApi.java
    partner_config --> AddApi.java
    file --> security
    file --> FileUploadApi.java
    file --> MergeApi.java
    security --> CsvSecurityChecker.java
    security --> FileSecurityChecker.java
    security --> ExcelSecurityChecker.java
    security --> ImageSecurityChecker.java
    gateway --> TestConnectApi.java
    gateway --> GetMemberJobProgressApi.java
    gateway --> GetDerivedDataSetDetailApi.java
    gateway --> RedirectApi.java
    data_output_info --> PushModelToServingByProviderApi.java
    data_output_info --> ModelExportToFileApi.java
    data_output_info --> PushRsaKeyToServingApi.java
    data_output_info --> ModelExportController.java
    data_output_info --> PushModelToServingApi.java
    union --> data_resource
    union --> member_auth
    union --> MemberListApi.java
    union --> GetMemberMapApi.java
    union --> AbstractThroughUnionApi.java
    data_resource --> tag
    data_resource --> DataResourceQueryApi.java
    data_resource --> DataResourceDetailApi.java
    tag --> QueryTagApi.java
    tag --> QueryDefaultTagApi.java
    member_auth --> MemberAuthTypeQueryApi.java
    member_auth --> DownloadFileApi.java
    member_auth --> QueryRealnameAuthAgreementTemplateApi.java
    member_auth --> MemberFileUploadApi.java
    member_auth --> MemberRealnameAuthInfoQueryApi.java
    member_auth --> MemberRealnameAuthApi.java
    operation --> LogQueryApi.java
    project --> modeling
    project --> job
    project --> dataset
    project --> project
    project --> flow
    project --> member
    project --> fusion
    project --> node
    modeling --> QueryApi.java
    modeling --> DetailApi.java
    job --> task
    job --> PreviewJobApi.java
    job --> QueryApi.java
    job --> ResumeJobApi.java
    job --> DownloadLogApi.java
    job --> GetJobProgressApi.java
    job --> DetailApi.java
    job --> UpdateJobStatusApi.java
    job --> StopJobApi.java
    job --> ViewDataSetApi.java
    job --> OnJobFinishedApi.java
    task --> TaskProgressDetailApi.java
    task --> GetFeatureApi.java
    task --> DetailApi.java
    task --> GetResultHistoryApi.java
    task --> GetResultApi.java
    dataset --> ListApi.java
    dataset --> RawDataSetListApi.java
    dataset --> AddDataSetApi.java
    dataset --> QueryDerivedDataSetApi.java
    dataset --> GetFeaturesApi.java
    dataset --> RemoveDataSetApi.java
    dataset --> AuditDataSetApi.java
    project --> QueryApi.java
    project --> UpdateProjectApi.java
    project --> AddApi.java
    project --> TopProjectApi.java
    project --> DataInfoApi.java
    project --> DetailApi.java
    project --> AuditApi.java
    project --> CloseProjectApi.java
    project --> CountStatisticsApi.java
    flow --> ListFlowNodeApi.java
    flow --> AddFlowApi.java
    flow --> UpdateFlowBaseInfoApi.java
    flow --> QueryFlowTemplateApi.java
    flow --> StartFlowApi.java
    flow --> QueryDataIoTaskConfigApi.java
    flow --> GetProgressApi.java
    flow --> DeleteApi.java
    flow --> SaveFlowTemplateApi.java
    flow --> QueryDataIoTaskFeaturesApi.java
    flow --> UpdateFlowGraphApi.java
    flow --> DetailFlowApi.java
    flow --> FlowQueryApi.java
    flow --> AddOotFlowApi.java
    flow --> CopyFlowApi.java
    flow --> TopFlowApi.java
    flow --> FlowDataSetInfoApi.java
    flow --> ListFlowTableDataSetApi.java
    member --> audit
    member --> AddApi.java
    member --> ListInAllProjectApi.java
    member --> ListInProjectApi.java
    member --> ExitProjectApi.java
    member --> OnlineCheckApi.java
    member --> RemoveApi.java
    audit --> ProjectMemberAuditListApi.java
    audit --> AuditApi.java
    fusion --> result
    fusion --> actuator
    fusion --> task
    fusion --> member
    fusion --> HashOptionsEnumApi.java
    result --> ResultExportApi.java
    result --> ResultPreviewApi.java
    result --> TestDBConnectApi.java
    result --> ResultExportProgressApi.java
    actuator --> psi
    psi --> DownloadBFApi.java
    psi --> ReceiveResultApi.java
    psi --> ServerSynStatusApi.java
    psi --> ServerCloseApi.java
    psi --> PsiCryptoApi.java
    task --> ReceiveApi.java
    task --> InfoApi.java
    task --> PagingApi.java
    task --> UpdateApi.java
    task --> RestartApi.java
    task --> DeleteApi.java
    task --> AddApi.java
    task --> DeleteCallbackApi.java
    task --> AuditCallbackApi.java
    task --> DetailApi.java
    task --> AuditApi.java
    task --> TaskStatusApi.java
    member --> QueryProvidersApi.java
    node --> CheckExistVertModelComponentApi.java
    node --> UpdateApi.java
    node --> CheckExistEvaluationComponentApi.java
    node --> DetailApi.java
    datasource --> QueryApi.java
    datasource --> DeleteApi.java
    datasource --> AddApi.java
    datasource --> TestDBConnectApi.java
    member --> SyncMemberToServingApi.java
    member --> IsInitializedApi.java
    member --> ResetRsaKeyApi.java
    member --> SyncMemberToUnionApi.java
    member --> CheckMemberRouteConnectApi.java
    member --> GetMemberMachineLearningEnvApi.java
    member --> UpdateMemberInfoApi.java
    member --> UpdateMemberLogoApi.java
    member --> MemberAvailableCheckApi.java
    member --> InitializeApi.java
    member --> MemberDetailApi.java
    model --> deep_learning
    deep_learning --> DownloadInferResultApi.java
    deep_learning --> DownloadDataSetZipApi.java
    deep_learning --> StartInferApi.java
    deep_learning --> DownloadDataSetImageApi.java
    deep_learning --> DownloadModelApi.java
    deep_learning --> StopInferApi.java
    component --> ListApi.java
```

This flowchart illustrates the hierarchical structure of the WeFe project's API modules, starting from the root directory 'api' and expanding into submodules such as 'data_resource', 'project', 'member', etc., ultimately detailing specific API implementation classes. The diagram clearly presents the dependency relationships between modules, for example, the 'project' module contains multiple submodules like 'modeling', 'job', 'dataset', each of which includes specific API classes. The entire structure is well-organized, comprehensively covering all given path information.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [crypto](crypto/_module.md) | package | API for generating RSA key pairs, returning the public key for encrypted data transmission. |
| [project](project/_module.md) | package | The module provides modeling information query APIs, supporting pagination and detail retrieval. The task management module enables full lifecycle control, including creation, suspension, resumption, etc. The dataset module manages CRUD operations and review processes. The project management module covers CRUD, status changes, and statistical analysis. The workflow management module handles process orchestration and status control. The member management module manages additions, deletions, modifications, and reviews. The federated learning module oversees alignment tasks and data fusion. The node module is responsible for node information maintenance and compliance checks. |
| [datasource](datasource/_module.md) | package | QueryApi is used for paginated querying of data sources, with inputs including names and pagination parameters, and outputs being data source details. DeleteApi deletes a data source by ID. AddApi adds a data source and validates input fields. TestDBConnectApi tests database connections and returns a boolean result. All inherit from the base API class and process requests via DataSourceService. |
| [dev](dev/_module.md) | package | This is an API class named ShowConfigApi, with the path dev/show_config, used to generate test datasets. It inherits from AbstractNoneInputApi and returns a Config object. The handle method retrieves the configuration and returns a successful result. |
| [member](member/_module.md) | package | SyncMemberToServingApi synchronizes member information to the server. IsInitializedApi checks the system initialization status. ResetRsaKeyApi resets the RSA key. SyncMemberToUnionApi synchronizes members to the union. CheckMemberRouteConnectApi checks member route connectivity. GetMemberMachineLearningEnvApi retrieves the member's machine learning environment. UpdateMemberInfoApi updates member information. UpdateMemberLogoApi updates the member logo. MemberAvailableCheckApi checks member service availability. InitializeApi initializes the system. MemberDetailApi retrieves member details. |
| [component](component/_module.md) | package | The ListApi interface filters the component list based on input conditions, excluding deep learning, undeveloped, and removed components, and returns information on the components that meet the criteria. The input parameter is the federated learning type. |
| [model](model/_module.md) | package | Six deep learning APIs are defined: download inference results, batch inference zip, start inference, download inference images, download model, and abort inference. All require the taskId parameter to handle file operations and task validation. |
| [operation](operation/_module.md) | package | The LogQueryApi provides paginated query functionality for operation logs. The input includes the interface name, operator ID, and time range, while the output returns paginated results of operation logs. |
| [union](union/_module.md) | package | The data resource management module provides services such as tag query, resource retrieval, and details, adopting a unified interface specification. The member authentication module handles authentication processes, including file uploads and real-name verification. The MemberListApi queries alliance members, while the GetMemberMapApi retrieves the member list. The AbstractThroughUnionApi serves as the foundational abstract class, encapsulating API invocation logic. |
| [data_output_info](data_output_info/_module.md) | package | PushModelToServingByProviderApi pushes the model to the serving system. ModelExportToFileApi exports and encrypts the model file. PushRsaKeyToServingApi pushes the RSA key. ModelExportController handles model export requests. PushModelToServingApi synchronizes the model to the server. |
| [gateway](gateway/_module.md) | package | TestConnectApi checks the connectivity between the gateway and the circuit board. GetMemberJobProgressApi retrieves task progress. GetDerivedDataSetDetailApi obtains derived dataset details. RedirectApi redirects gateway requests to internal APIs and supplements logs. |
| [file](file/_module.md) | package | This module provides multi-format file security checks, supporting 10 types including CSV/Excel/images, following a process of format validation first and then content scanning. It includes file upload chunking and merging functionalities, involving security checks, exception handling, and directory operations. Key classes include FileUploadApi and MergeApi. |
| [partner_config](partner_config/_module.md) | package | The QueryApi implements paginated queries for partner configurations, with Input containing memberIdList and gatewayAddress, returning paginated results. The DeleteApi handles deletion operations, requiring an id to be passed in. The AddApi is used to add records, requiring memberId and gatewayAddress, and returns the generated id. All inherit from AbstractApi and execute business logic through the PartnerConfigService. |
| [blacklist](blacklist/_module.md) | package | The BlacklistApi retrieves blacklists with pagination, accessible via the path blacklist/list. The BlacklistMemberApi queries blacklist members, accessible via the path blacklist/member. The DeleteApi removes blacklist members, accessible via the path blacklist/delete. The AddApi adds members to the blacklist, accessible via the path blacklist/add. All inherit from the base class and handle logic through the BlacklistService. |
| [service](service/_module.md) | package | VersionApi provides version information at the path "service/version", returning version number, build number, and date. ServiceAvailableApi checks service availability at the path "service/available", requiring specification of the service type. AliveApi is used for liveness detection at the path "service/alive", directly returning a success status. |
| [message](message/_module.md) | package | The QueryApi is used for paginated message queries with various filtering conditions. The ReadApi marks messages as read, requiring the input of message IDs. The DetailApi retrieves message details, querying and returning detailed data based on the ID. |
| [chat](chat/_module.md) | package | Multiple chat-related APIs are defined: query recent accounts, add recent accounts, send messages, update read status, query chat details, increment unread messages, resend messages, and delete recent accounts. Each API includes necessary input parameters, processes requests through corresponding services, and returns results or empty outputs. |
| [storage](storage/_module.md) | package | API class for previewing datasets, which queries datasets by ID and returns column names and data rows. Supports both native and derived datasets, with derived data retrieved from streaming services. The input is a dataset ID, and the output includes table headers and a JSON-formatted data list. |
| [data_resource](data_resource/_module.md) | package | Manage the dataset lifecycle, including CRUD operations, preview, and metadata handling. Supports file uploads, structured storage, and sample viewing. Provides Bloom filter management, image dataset maintenance, and label query functionality. APIs adhere to RESTful specifications, uniformly inheriting from AbstractApi with clear path prefixes. Key data structures include input/output models, relying on the service layer for business logic processing. |
| [online_demo](online_demo/_module.md) | package | TianmiantechPageApi generates Tianmian Tech website URLs with checksum and signature. CheckAccountExistApi verifies account existence by returning a boolean value for input phone numbers. TianmiantechCallApi invokes Tianmian Tech service interfaces and returns JObject results. CreateOnlineDemoAccountApi creates trial accounts without requiring login. |
| [account](account/_module.md) | package | QueryMemberAccountsApi retrieves account information by member ID. QueryOnlineApi queries online accounts. ListAllApi obtains a full list of users. UpdateUiConfigApi modifies user UI configurations. SsoLoginApi processes single sign-on requests. |
| [global_config](global_config/_module.md) | package | The GlobalConfigUpdateApi is used to update system configurations, with the endpoint `global_config/update`, accepting a required Map-type `groups` field. The GetGlobalConfigApi is used to retrieve configurations, with the endpoint `global_config/get`, accepting a required `groups` list and returning a Map of configuration data. Both rely on the GlobalConfigService to implement their functionalities. |


