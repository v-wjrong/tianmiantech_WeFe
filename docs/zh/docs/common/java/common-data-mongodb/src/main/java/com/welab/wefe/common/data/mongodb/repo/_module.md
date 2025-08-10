# 基础信息

|      |      |
|------|------|
| 名称 | repo |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/repo |
| 包名 | docs.common.java.common-data-mongodb.src.main.java.com.welab.wefe.common.data.mongodb.repo |
| 概述说明 | 多个MongoDB仓库类继承AbstractMongoRepo，实现各类数据操作，包括查询、更新、删除等，涉及实名认证、数据集、区块同步、证书管理等功能，均使用MongoTemplate进行数据库操作。 |

# 说明

## 概述  
该模块是基于MongoDB的数据访问层，提供各类业务数据的CRUD操作及复杂查询功能，类似数据总线模式统一管理多领域数据。核心职责包括：通过继承AbstractMongoRepo实现标准化MongoTemplate操作，支持模板协议、数据集、成员信息等20+业务实体的持久化，所有操作均包含逻辑删除、更新时间戳等统一约束。  

接口规范遵循抽象基类定义的泛型模式，子类需实现getMongoTemplate()并复用save/upsert等方法。例如RealnameAuthAgreementTemplateMongoRepo提供版本号查询，DataSetMongoReop实现多表关联分页查询。关键数据结构含AbstractMongoModel派生类（如CertInfo、UnionNode）、分页对象PageOutput及扩展JSON字段。外部依赖包括Spring Data MongoDB、QueryBuilder和聚合框架。  

## 主要业务场景  
典型应用为多条件分页查询与事务更新，例如ImageDataSetMongoReop通过聚合管道实现数据集权限过滤，UnionNodeMongoRepo管理节点状态变更。业务流程涵盖：1) 数据生命周期管理（如MemberFileInfo的启用/删除）；2) 版本控制（如BlockSyncDetailInfo的乐观锁更新）；3) 跨实体关联查询（如TableDataSetMongoReop联合标签表）。  

交互模式以API组合为主，如CertInfoRepo同时提供单条更新(certStatus)和批量查询(byUserId)。集成案例包括：区块同步服务使用BlockSyncHeightMongoReop记录链上高度，账户系统通过AccountMongoRepo实现活跃度检测。所有操作均返回布尔结果或分页数据，确保事务可追溯性。


### 包内部结构视图

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

该流程图展示了MongoDB仓库(repo)目录下的所有Java接口文件，共包含26个不同的MongoDB仓库接口，涵盖了实名认证协议模板、数据集标签、区块同步详情、信任证书、联盟操作日志等多种数据操作接口。这些接口均继承自基础MongoDB仓库抽象类，用于实现不同类型数据的持久化操作。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [RealnameAuthAgreementTemplateMongoRepo.java](RealnameAuthAgreementTemplateMongoRepo.md) | file | RealnameAuthAgreementTemplateMongoRepo类用于操作MongoDB中的实名认证协议模板数据，提供查询、更新等功能，包括按版本、文件签名、ID和启用状态查找模板，以及更新启用状态和扩展JSON数据。 |
| [DataSetDefaultTagMongoRepo.java](DataSetDefaultTagMongoRepo.md) | file | 数据集默认标签MongoDB仓库类，提供查询、存在检查、删除、更新标签及扩展JSON功能。 |
| [BlockSyncDetailInfoMongoRepo.java](BlockSyncDetailInfoMongoRepo.md) | file | 这是一个MongoDB存储库类，用于管理区块同步详情信息。它继承自AbstractMongoRepo，使用MongoTemplate操作数据库。主要功能包括按组ID和区块号查询记录，以及插入或更新记录（当区块号更大时更新）。 |
| [TrustCertsMongoRepo.java](TrustCertsMongoRepo.md) | file | TrustCertsMongoRepo类继承AbstractMongoRepo，使用MongoTemplate操作数据库。提供查询所有证书、按序列号查询存在性和删除功能。删除通过标记状态实现。 |
| [UnionOperationLogMongoRepo.java](UnionOperationLogMongoRepo.md) | file | UnionOperationLogMongoRepo类继承AbstractOperationLogMongoRepo，通过@Autowired注入mongoUnionTemplate，重写getMongoTemplate方法返回该模板。 |
| [MemberFileInfoMongoRepo.java](MemberFileInfoMongoRepo.md) | file | MemberFileInfoMongoRepo类继承AbstractMongoRepo，使用MongoTemplate操作MongoDB，提供按memberId、fileId、fileSign查询MemberFileInfo的方法，以及更新enable和extJson字段的功能。 |
| [BlockSyncContractHeightMongoRepo.java](BlockSyncContractHeightMongoRepo.md) | file | 这是一个MongoDB仓库类，用于管理区块同步合约高度数据。提供按组ID和合约名称查询功能，支持更新或插入记录，确保数据最新且不重复。继承自抽象Mongo仓库类，使用MongoTemplate操作数据库。 |
| [CertRequestInfoRepo.java](CertRequestInfoRepo.md) | file | CertRequestInfoRepo是MongoDB仓库类，提供按pkId、pCertId和subjectKeyId查询证书请求信息的方法，支持分页查询列表。 |
| [TableDataSetMongoReop.java](TableDataSetMongoReop.md) | file | TableDataSetMongoReop类继承AbstractDataSetMongoRepo，使用MongoTemplate操作MongoDB。提供existsByDataResourceId、findByDataResourceId、upsert等方法操作表数据集。findCurMemberCanSee方法通过聚合查询实现分页获取当前用户可见数据，支持条件筛选和排序。deleteByDataResourceId方法逻辑删除数据。 |
| [ImageDataSetMongoReop.java](ImageDataSetMongoReop.md) | file | ImageDataSetMongoReop类继承AbstractDataSetMongoRepo，使用MongoTemplate操作MongoDB。提供existsByDataSetId、findByDataResourceId方法查询数据，findCurMemberCanSee方法分页查询当前用户可见数据集，支持条件筛选和聚合操作。包含upsert保存数据和deleteByDataResourceId逻辑删除功能。 |
| [AbstractDataSetMongoRepo.java](AbstractDataSetMongoRepo.md) | file | 抽象类AbstractDataSetMongoRepo继承AbstractMongoRepo，使用MongoTemplate进行聚合查询，通过标签名查找并统计数据集标签结果。 |
| [DataResourceDefaultTagMongoRepo.java](DataResourceDefaultTagMongoRepo.md) | file | DataResourceDefaultTagMongoRepo类继承AbstractMongoRepo，使用MongoTemplate操作MongoDB，提供exists、findByDataResourceType、deleteByTagId、update和updateExtJSONById等方法，用于查询、删除和更新DataResourceDefaultTag数据。 |
| [CertKeyInfoRepo.java](CertKeyInfoRepo.md) | file | CertKeyInfoRepo是MongoDB仓库类，提供按pkId查询单条记录、按userId查询列表及分页查询功能，继承AbstractMongoRepo并使用MongoTemplate操作数据。 |
| [DataSetMongoReop.java](DataSetMongoReop.md) | file | DataSetMongoRepo类继承AbstractDataSetMongoRepo，提供数据集CRUD操作，包括按ID查询、删除、更新及分页查询可见数据集，使用MongoTemplate操作MongoDB。 |
| [MemberServiceMongoReop.java](MemberServiceMongoReop.md) | file | MemberServiceMongoReop类继承AbstractMongoRepo，使用MongoTemplate操作MongoDB。提供成员服务增删改查功能，包括按ID删除、更新、查询及分页查询，支持条件筛选和聚合操作。 |
| [UnionNodeConfigMongoRepo.java](UnionNodeConfigMongoRepo.md) | file | UnionNodeConfigMongoRepo是一个MongoDB仓库类，继承AbstractMongoRepo，使用mongoUnionTemplate操作数据库，提供find方法按updateTime排序查询UnionNodeSm2Config。 |
| [MemberAuthTypeMongoRepo.java](MemberAuthTypeMongoRepo.md) | file | MemberAuthTypeMongoRepo类继承AbstractMongoRepo，使用MongoTemplate操作数据库，提供查询、存在性检查、删除、更新及扩展JSON更新功能。 |
| [DataSetMemberPermissionMongoRepo.java](DataSetMemberPermissionMongoRepo.md) | file | 数据集成员权限Mongo仓库类，提供删除、查询、更新及插入功能，使用MongoTemplate操作数据库。 |
| [UnionNodeMongoRepo.java](UnionNodeMongoRepo.md) | file | UnionNodeMongoRepo类继承AbstractMongoRepo，提供对UnionNode的CRUD操作，包括按状态、URL、节点ID等查询，以及更新、删除功能。 |
| [ManagerOperationLogMongoRepo.java](ManagerOperationLogMongoRepo.md) | file | ManagerOperationLogMongoRepo类继承AbstractOperationLogMongoRepo，使用MongoTemplate查询操作日志，支持按条件分页查询并返回结果列表和总数。 |
| [DataResourceMongoReop.java](DataResourceMongoReop.md) | file | DataResourceMongoRepo类是一个MongoDB数据访问层，提供对数据资源的增删改查操作，包括按ID查询、删除、存在性检查、联合查询及分页功能。 |
| [AccountMongoRepo.java](AccountMongoRepo.md) | file | AccountMongoRepo类继承AbstractMongoRepo，使用MongoTemplate操作MongoDB。提供账号查询、更新、分页查询等功能，支持按条件禁用和注销长期未活跃账号。 |
| [BlockSyncHeightMongoReop.java](BlockSyncHeightMongoReop.md) | file | 这是一个MongoDB存储库类，用于管理区块同步高度数据。提供根据groupId查询和更新插入功能，确保数据不重复且更新最新时间戳。 |
| [AbstractOperationLogMongoRepo.java](AbstractOperationLogMongoRepo.md) | file | 抽象类AbstractOperationLogMongoRepo继承自AbstractMongoRepo，用于操作日志的MongoDB存储。 |
| [MemberMongoReop.java](MemberMongoReop.md) | file | MemberMongoRepo类继承AbstractMongoRepo，使用MongoTemplate操作MongoDB。提供成员增删改查功能，包括按ID删除、更新活动时间、logo、公钥等字段，以及分页查询和存在性检查。 |
| [DataResourceLazyUpdateModelMongoReop.java](DataResourceLazyUpdateModelMongoReop.md) | file | 这是一个MongoDB仓库类，继承自AbstractMongoRepo，使用MongoTemplate操作数据库。包含按ID查询、查询全部和按ID删除方法。 |
| [AbstractMongoRepo.java](AbstractMongoRepo.md) | file | 抽象MongoDB仓库类，提供保存、更新插入和模糊查询方法，需子类实现模板获取。 |
| [BloomFilterMongoReop.java](BloomFilterMongoReop.md) | file | BloomFilterMongoRepo类继承AbstractDataSetMongoRepo，使用MongoTemplate操作MongoDB表Union.BLOOM_FILTER。提供existsByDataResourceId、findByDataResourceId、upsert、deleteByDataResourceId等方法操作BloomFilter数据，以及findCurMemberCanSee方法查询当前成员可见的BloomFilter分页数据。 |
| [CertInfoRepo.java](CertInfoRepo.md) | file | CertInfoRepo类继承AbstractMongoRepo，通过MongoTemplate操作CertInfo数据，提供按pkId、序列号查询，分页查询，批量查询及更新状态、信任状态等功能。 |


