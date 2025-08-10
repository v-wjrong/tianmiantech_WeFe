# Basic Information

|      |      |
|------|------|
| Name | mongodb |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb |
| Package Name | docs.common.java.common-data-mongodb.src.main.java.com.welab.wefe.common.data.mongodb |
| Brief Description | The MongoDB data access layer provides CRUD and complex query functionalities, supporting logical deletion and timestamp constraints. It includes SMS business categorization and vendor enumeration management. The toolkit supports chained query construction and aggregation operations. The federated learning platform implements logging, certificates, and data governance. Unified query management handles datasets and member authentication. The connection management module dynamically registers MongoDB components. |

# Description

## Overview  
This module serves as the core data management component of the federated learning platform, enabling unified storage and operations for multi-domain data based on MongoDB, akin to a data bus pattern. Its core responsibilities include: 1) Managing 20+ business entities (e.g., certificates, datasets) through standardized CRUD interfaces; 2) Providing complex query construction tools and aggregation operation support; 3) Unified connection management and transaction control.  

The interface specification follows a layered design: the base layer (AbstractMongoModel/Repo) defines primary key and serialization rules, while the business layer extends specific operations (e.g., version control). Key data structures include the pagination object PageOutput, certificate PEM content, and dataset permission models. External dependencies include Spring Data MongoDB, QueryBuilder, and the MongoDB driver. For example, RealnameAuthAgreementTemplateMongoRepo implements optimistic lock updates, and QueryBuilder supports range filtering.  

## Key Business Scenarios  
The module supports four major scenarios: 1) Data governance (e.g., DataSet permission control), similar to the RBAC model; 2) Operation auditing (recording API call logs); 3) Federated resource retrieval (multi-condition paginated queries); 4) Full lifecycle management of certificates. Business processes include: selecting SMS templates via enumerations, chaining update conditions, and processing dataset permissions through aggregation pipelines.  

The interaction mode primarily involves DTO transmission and API composition. For instance, ImageDataSetMongoRepo queries joint label tables, while AccountMongoRepo implements activity detection. Functional completeness is reflected in covering the entire data lifecycle (metadata → usage statistics), with typical applications including resource selectors during task configuration and node qualification verification. API types encompass CRUD operations (e.g., certStatus updates) and configuration classes (@Configuration). Integration examples can be seen in the block synchronization service's height records.


### Package Internal Structure View

```mermaid
graph TD
    mongodb --> repo
    mongodb --> constant
    mongodb --> util
    mongodb --> entity
    mongodb --> dto
    mongodb --> config
    repo --> RealnameAuthAgreementTemplateMongoRepo.java
    repo --> DataSetDefaultTagMongoRepo.java
    repo --> BlockSyncDetailInfoMongoRepo.java
    repo --> TrustCertsMongoRepo.java
    repo --> UnionOperationLogMongoRepo.java
    repo --> MemberFileInfoMongoRepo.java
    repo --> BlockSyncContractHeightMongoRepo.java
    repo --> CertRequestInfoRepo.java
    repo --> TableDataSetMongoReop.java
    repo --> ImageDataSetMongoReop.java
    repo --> AbstractDataSetMongoRepo.java
    repo --> DataResourceDefaultTagMongoRepo.java
    repo --> CertKeyInfoRepo.java
    repo --> DataSetMongoReop.java
    repo --> MemberServiceMongoReop.java
    repo --> UnionNodeConfigMongoRepo.java
    repo --> MemberAuthTypeMongoRepo.java
    repo --> DataSetMemberPermissionMongoRepo.java
    repo --> UnionNodeMongoRepo.java
    repo --> ManagerOperationLogMongoRepo.java
    repo --> DataResourceMongoReop.java
    repo --> AccountMongoRepo.java
    repo --> BlockSyncHeightMongoReop.java
    repo --> AbstractOperationLogMongoRepo.java
    repo --> MemberMongoReop.java
    repo --> DataResourceLazyUpdateModelMongoReop.java
    repo --> AbstractMongoRepo.java
    repo --> BloomFilterMongoReop.java
    repo --> CertInfoRepo.java
    constant --> SmsBusinessType.java
    constant --> SmsSupplierEnum.java
    constant --> MongodbTable.java
    util --> UpdateBuilder.java
    util --> AddFieldsOperation.java
    util --> QueryBuilder.java
    entity --> common
    entity --> manager
    entity --> union
    entity --> base
    common --> OperationLog.java
    manager --> CertInfo.java
    manager --> CertRequestInfo.java
    manager --> Account.java
    manager --> CertKeyInfo.java
    union --> ext
    union --> DataResourceDefaultTag.java
    union --> TableDataSet.java
    union --> TrustCerts.java
    union --> RealnameAuthAgreementTemplate.java
    union --> DataResourceLazyUpdateModel.java
    union --> MemberFileInfo.java
    union --> DataSet.java
    union --> BloomFilter.java
    union --> BlockSyncHeight.java
    union --> UnionNode.java
    union --> BlockSyncDetailInfo.java
    union --> BlockSyncContractHeight.java
    union --> DataResource.java
    union --> TransactionResponseDetailInfo.java
    union --> MemberAuthType.java
    union --> DataSetMemberPermission.java
    union --> ImageDataSet.java
    union --> MemberService.java
    union --> Member.java
    union --> DataSetDefaultTag.java
    union --> UnionNodeSm2Config.java
    ext --> DataSetDefaultTagExtJSON.java
    ext --> MemberServiceExtJSON.java
    ext --> MemberAuthTypeExtJSON.java
    ext --> TableDataSetExtJSON.java
    ext --> RealnameAuthAgreementTemplateExtJSON.java
    ext --> BloomFilterExtJSON.java
    ext --> MemberExtJSON.java
    ext --> DataSetMemberPermissionExtJSON.java
    ext --> ImageDataSetExtJSON.java
    ext --> UnionNodeExtJSON.java
    ext --> RealnameAuthFileInfo.java
    ext --> MemberFileInfoExtJSON.java
    ext --> DataResourceDefaultTagExtJSON.java
    ext --> DataResourceExtJSON.java
    ext --> TrustCertsExtJSON.java
    ext --> DataSetExtJSON.java
    base --> AbstractBlockChainBusinessModel.java
    base --> AbstractMongoModel.java
    base --> AbstractUnionNodeConfigMongoModel.java
    base --> AbstractNormalMongoModel.java
    dto --> dataresource
    dto --> dataset
    dto --> member
    dto --> PageOutput.java
    dto --> PageInput.java
    dto --> AbstractQueryOutput.java
    dataresource --> DataResourceQueryInput.java
    dataresource --> DataResourceQueryOutput.java
    dataset --> ImageDataSetQueryOutput.java
    dataset --> DataSetQueryOutput.java
    dataset --> DataSetQueryInput.java
    dataset --> TableDataSetQueryInput.java
    dataset --> DataSetTagsQueryOutput.java
    dataset --> ImageDataSetQueryInput.java
    member --> RealnameAuthInfoQueryOutput.java
    member --> MemberAuthQueryOutput.java
    member --> MemberServiceQueryOutput.java
    config --> MongoManagerConfig.java
    config --> AbstractConfig.java
    config --> MongoUnionConfig.java
```

This flowchart illustrates the complete hierarchical structure of MongoDB-related code, comprising six main modules (repo/constant/util/entity/dto/config). The entity module is further subdivided into submodules such as common/manager/union/base, with the union module containing an ext extension submodule. The repo module includes 28 repository class files, while the entity module contains 40 entity class files. The overall structure clearly demonstrates the complete organization of the MongoDB data access layer.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [dto](dto/_module.md) | package | The data query module provides multi-criteria filtering and result encapsulation functionalities, supporting paginated queries for data types such as images/tables. It includes input parameter encapsulation, permission filtering, and result aggregation display, and is applied in scenarios like federated learning resource retrieval. It relies on MongoDB and implements CRUD operations through DTO. |
| [config](config/_module.md) | package | The MongoManagerConfig class manages MongoDB Bean registration and dynamically creates components such as MongoClient. The getConverter method of the AbstractConfig class configures the MappingMongoConverter, disabling the _class field. The MongoUnionConfig class defines MongoDB connection components, supporting transactions and file storage. |
| [entity](entity/_module.md) | package | The OperationLog class records API operation logs, including request and response information along with timestamps. The certificate management module stores full lifecycle data of certificates and supports the issuance process. The federated learning module manages multi-type data resources and supports extensibility. The universal data model abstraction layer defines storage specifications, supporting time tracking and node configuration management. |
| [util](util/_module.md) | package | The UpdateBuilder class is used to construct update operations and supports chained calls. The AddFieldsOperation class implements aggregation operations to add new fields. The QueryBuilder class builds query conditions, supporting various operators as well as pagination and sorting. |
| [constant](constant/_module.md) | package | The SmsBusinessType enumeration defines verification code types for member registration and password recovery. The SmsSupplierEnum enumeration currently only supports Alibaba Cloud SMS provider. The MongodbTable class manages MongoDB collection name constants, including over 20 collection names such as operation logs and datasets. |
| [repo](repo/_module.md) | package | Multiple MongoDB repository classes inherit from AbstractMongoRepo to implement various data operations, including queries, updates, deletions, etc. These operations involve functionalities such as real-name authentication, datasets, block synchronization, and certificate management, all of which utilize MongoTemplate for database operations. |


