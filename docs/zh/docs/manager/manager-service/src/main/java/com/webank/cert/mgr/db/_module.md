# 基础信息

|      |      |
|------|------|
| 名称 | db |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/webank/cert/mgr/db |
| 包名 | docs.manager.manager-service.src.main.java.com.webank.cert.mgr.db |
| 概述说明 | CertDao类管理证书、密钥和请求信息，提供保存、查询和更新功能，支持分页查询和状态更新。 |

# 说明

CertDao是一个服务类，负责管理证书、密钥和证书请求的数据访问操作。它通过三个自动注入的仓库接口（CertInfoRepo、CertKeyInfoRepo、CertRequestInfoRepo）实现数据的增删改查功能。主要功能包括保存证书、密钥和请求信息，根据ID查询各类信息，更新证书状态和信任状态，以及分页查询证书列表、请求列表和密钥列表。此外，还支持根据用户ID、序列号、父证书ID等条件进行查询。


### 包内部结构视图

```mermaid
graph TD
    db --> dao
    dao --> CertDao.java
```

该流程图展示了WeFe项目中manager-service模块下的数据库相关代码结构。顶层是db目录，包含dao子目录，dao目录下包含CertDao.java文件。这种层级关系清晰地反映了数据库访问层的组织结构，其中dao层负责数据访问操作。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [dao](dao/_module.md) | package | CertDao类管理证书、密钥和请求信息，提供保存、查询和更新功能，支持分页查询和状态更新。 |


