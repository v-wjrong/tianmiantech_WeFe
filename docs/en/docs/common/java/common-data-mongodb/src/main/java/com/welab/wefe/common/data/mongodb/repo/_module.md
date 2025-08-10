# Basic Information

|      |      |
|------|------|
| Name | repo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/repo |
| Package Name | docs.common.java.common-data-mongodb.src.main.java.com.welab.wefe.common.data.mongodb.repo |
| Brief Description | Multiple MongoDB repository classes inherit from AbstractMongoRepo to implement various data operations, including queries, updates, deletions, etc. These operations involve functionalities such as real-name authentication, datasets, block synchronization, and certificate management, all of which utilize MongoTemplate for database operations. |

# Description

## Overview  
This module is a data access layer based on MongoDB, providing CRUD operations and complex query capabilities for various business data, unifying the management of multi-domain data in a data bus-like pattern. Core responsibilities include: implementing standardized MongoTemplate operations by inheriting AbstractMongoRepo, supporting the persistence of 20+ business entities such as template protocols, datasets, and member information, with all operations adhering to unified constraints like logical deletion and timestamp updates.  

The interface specification follows the generic pattern defined by the abstract base class, requiring subclasses to implement getMongoTemplate() and reuse methods like save/upsert. For example, RealnameAuthAgreementTemplateMongoRepo provides version number queries, while DataSetMongoReop implements multi-table join pagination queries. Key data structures include AbstractMongoModel-derived classes (e.g., CertInfo, UnionNode), pagination object PageOutput, and extended JSON fields. External dependencies include Spring Data MongoDB, QueryBuilder, and the aggregation framework.  

## Key Business Scenarios  
Typical applications involve multi-condition pagination queries and transactional updates. For instance, ImageDataSetMongoReop implements dataset permission filtering through aggregation pipelines, and UnionNodeMongoRepo manages node status changes. Business processes encompass: 1) Data lifecycle management (e.g., enabling/deleting MemberFileInfo); 2) Version control (e.g., optimistic lock updates for BlockSyncDetailInfo); 3) Cross-entity association queries (e.g., TableDataSetMongoReop joining with tag tables).  

The interaction mode primarily revolves around API composition. For example, CertInfoRepo provides both single-record updates (certStatus) and batch queries (byUserId). Integration cases include: the block synchronization service using BlockSyncHeightMongoReop to record on-chain heights, and the account system leveraging AccountMongoRepo for activity detection. All operations return boolean results or paginated data, ensuring transactional traceability.


### Package Internal Structure View

```mermaid
graph TD
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
```

This flowchart displays all Java interface files under the MongoDB repository (repo) directory, comprising a total of 26 distinct MongoDB repository interfaces. These interfaces cover various data operations such as real-name authentication agreement templates, dataset tags, block synchronization details, trust certificates, and consortium operation logs. All interfaces inherit from the base MongoDB repository abstract class and are designed to implement persistence operations for different types of data.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [RealnameAuthAgreementTemplateMongoRepo.java](RealnameAuthAgreementTemplateMongoRepo.md) | file | The `RealnameAuthAgreementTemplateMongoRepo` class is used to manipulate real-name authentication agreement template data in MongoDB, providing functionalities such as querying and updating. It includes searching templates by version, file signature, ID, and activation status, as well as updating activation status and extended JSON data. |
| [DataSetDefaultTagMongoRepo.java](DataSetDefaultTagMongoRepo.md) | file | The default labeled dataset MongoDB repository class provides query, existence check, deletion, label update, and extended JSON functionality. |
| [BlockSyncDetailInfoMongoRepo.java](BlockSyncDetailInfoMongoRepo.md) | file | This is a MongoDB repository class for managing block synchronization details. It inherits from AbstractMongoRepo and utilizes MongoTemplate to interact with the database. Key functionalities include querying records by group ID and block number, as well as inserting or updating records (updating when the block number is larger). |
| [TrustCertsMongoRepo.java](TrustCertsMongoRepo.md) | file | The `TrustCertsMongoRepo` class inherits from `AbstractMongoRepo` and utilizes `MongoTemplate` to perform database operations. It provides functionalities to query all certificates, check existence by serial number, and delete entries. Deletion is implemented by marking the status. |
| [UnionOperationLogMongoRepo.java](UnionOperationLogMongoRepo.md) | file | The `UnionOperationLogMongoRepo` class inherits from `AbstractOperationLogMongoRepo`, injects `mongoUnionTemplate` via `@Autowired`, and overrides the `getMongoTemplate` method to return this template. |
| [MemberFileInfoMongoRepo.java](MemberFileInfoMongoRepo.md) | file | The MemberFileInfoMongoRepo class inherits from AbstractMongoRepo, utilizes MongoTemplate to operate MongoDB, and provides methods for querying MemberFileInfo by memberId, fileId, and fileSign, as well as functionality to update the enable and extJson fields. |
| [BlockSyncContractHeightMongoRepo.java](BlockSyncContractHeightMongoRepo.md) | file | This is a MongoDB repository class designed for managing block synchronization contract height data. It provides query functionality by group ID and contract name, supports updating or inserting records, and ensures data is up-to-date and non-duplicated. Inheriting from an abstract Mongo repository class, it utilizes MongoTemplate for database operations. |
| [CertRequestInfoRepo.java](CertRequestInfoRepo.md) | file | CertRequestInfoRepo is a MongoDB repository class that provides methods for querying certificate request information by pkId, pCertId, and subjectKeyId, supporting paginated list queries. |
| [TableDataSetMongoReop.java](TableDataSetMongoReop.md) | file | The `TableDataSetMongoReop` class inherits from `AbstractDataSetMongoRepo` and uses `MongoTemplate` to operate MongoDB. It provides methods such as `existsByDataResourceId`, `findByDataResourceId`, and `upsert` to manipulate table datasets. The `findCurMemberCanSee` method implements pagination to retrieve data visible to the current user through aggregation queries, supporting conditional filtering and sorting. The `deleteByDataResourceId` method performs logical deletion of data. |
| [ImageDataSetMongoReop.java](ImageDataSetMongoReop.md) | file | The ImageDataSetMongoRepo class inherits from AbstractDataSetMongoRepo and utilizes MongoTemplate to interact with MongoDB. It provides methods such as existsByDataSetId and findByDataResourceId for data querying, and findCurMemberCanSee for paginated retrieval of datasets visible to the current user, supporting conditional filtering and aggregation operations. It also includes upsert for saving data and deleteByDataResourceId for logical deletion functionality. |
| [AbstractDataSetMongoRepo.java](AbstractDataSetMongoRepo.md) | file | The abstract class AbstractDataSetMongoRepo extends AbstractMongoRepo, utilizes MongoTemplate for aggregation queries, and searches by tag names to count dataset tag results. |
| [DataResourceDefaultTagMongoRepo.java](DataResourceDefaultTagMongoRepo.md) | file | The `DataResourceDefaultTagMongoRepo` class inherits from `AbstractMongoRepo`, utilizes `MongoTemplate` to interact with MongoDB, and provides methods such as `exists`, `findByDataResourceType`, `deleteByTagId`, `update`, and `updateExtJSONById` for querying, deleting, and updating `DataResourceDefaultTag` data. |
| [CertKeyInfoRepo.java](CertKeyInfoRepo.md) | file | CertKeyInfoRepo is a MongoDB repository class that provides functionalities for querying a single record by pkId, querying a list by userId, and paginated queries. It inherits from AbstractMongoRepo and utilizes MongoTemplate for data operations. |
| [DataSetMongoReop.java](DataSetMongoReop.md) | file | The DataSetMongoRepo class inherits from AbstractDataSetMongoRepo, providing CRUD operations for datasets, including querying by ID, deletion, updating, and paginated querying of visible datasets, utilizing MongoTemplate to interact with MongoDB. |
| [MemberServiceMongoReop.java](MemberServiceMongoReop.md) | file | The MemberServiceMongoReop class inherits from AbstractMongoRepo and utilizes MongoTemplate to operate MongoDB. It provides CRUD functionalities for member services, including deletion by ID, updating, querying, and paginated queries, with support for conditional filtering and aggregation operations. |
| [UnionNodeConfigMongoRepo.java](UnionNodeConfigMongoRepo.md) | file | The `UnionNodeConfigMongoRepo` is a MongoDB repository class that extends `AbstractMongoRepo`. It utilizes `mongoUnionTemplate` for database operations and provides a `find` method to query `UnionNodeSm2Config` sorted by `updateTime`. |
| [MemberAuthTypeMongoRepo.java](MemberAuthTypeMongoRepo.md) | file | The MemberAuthTypeMongoRepo class inherits from AbstractMongoRepo, utilizes MongoTemplate to interact with the database, and provides functionalities for querying, existence checking, deletion, updating, and extended JSON updates. |
| [DataSetMemberPermissionMongoRepo.java](DataSetMemberPermissionMongoRepo.md) | file | Dataset member permission MongoDB repository class, providing delete, query, update, and insert functionalities, operates the database using MongoTemplate. |
| [UnionNodeMongoRepo.java](UnionNodeMongoRepo.md) | file | The UnionNodeMongoRepo class inherits from AbstractMongoRepo and provides CRUD operations for UnionNode, including queries by status, URL, node ID, etc., as well as update and delete functionalities. |
| [ManagerOperationLogMongoRepo.java](ManagerOperationLogMongoRepo.md) | file | The `ManagerOperationLogMongoRepo` class inherits from `AbstractOperationLogMongoRepo`, uses `MongoTemplate` to query operation logs, and supports paginated queries with conditions while returning both the result list and total count. |
| [DataResourceMongoReop.java](DataResourceMongoReop.md) | file | The `DataResourceMongoRepo` class is a MongoDB data access layer that provides CRUD operations for data resources, including querying by ID, deletion, existence checks, combined queries, and pagination functionality. |
| [AccountMongoRepo.java](AccountMongoRepo.md) | file | The `AccountMongoRepo` class inherits from `AbstractMongoRepo` and utilizes `MongoTemplate` to interact with MongoDB. It provides functionalities such as account querying, updating, and paginated queries, while supporting conditional deactivation and deletion of long-inactive accounts. |
| [BlockSyncHeightMongoReop.java](BlockSyncHeightMongoReop.md) | file | This is a MongoDB repository class for managing block synchronization height data. It provides query and upsert functionality based on groupId, ensuring no duplicate data and updating the latest timestamp. |
| [AbstractOperationLogMongoRepo.java](AbstractOperationLogMongoRepo.md) | file | The abstract class `AbstractOperationLogMongoRepo` extends `AbstractMongoRepo` and is used for MongoDB storage of operation logs. |
| [MemberMongoReop.java](MemberMongoReop.md) | file | The MemberMongoRepo class inherits from AbstractMongoRepo and utilizes MongoTemplate to operate MongoDB. It provides CRUD functionality for members, including deletion by ID, updating fields such as activity time, logo, and public key, as well as paginated queries and existence checks. |
| [DataResourceLazyUpdateModelMongoReop.java](DataResourceLazyUpdateModelMongoReop.md) | file | This is a MongoDB repository class that inherits from AbstractMongoRepo and uses MongoTemplate to interact with the database. It includes methods for querying by ID, querying all records, and deleting by ID. |
| [AbstractMongoRepo.java](AbstractMongoRepo.md) | file | Abstract MongoDB repository class, providing save, upsert, and fuzzy query methods, requires subclass implementation of template acquisition. |
| [BloomFilterMongoReop.java](BloomFilterMongoReop.md) | file | The BloomFilterMongoRepo class inherits from AbstractDataSetMongoRepo and uses MongoTemplate to operate on the MongoDB table Union.BLOOM_FILTER. It provides methods such as existsByDataResourceId, findByDataResourceId, upsert, and deleteByDataResourceId to manipulate BloomFilter data, as well as the findCurMemberCanSee method to query paginated BloomFilter data visible to the current member. |
| [CertInfoRepo.java](CertInfoRepo.md) | file | The CertInfoRepo class inherits from AbstractMongoRepo and operates on CertInfo data through MongoTemplate, providing functionalities such as querying by pkId and serial number, paginated queries, batch queries, and updating status and trust status. |


