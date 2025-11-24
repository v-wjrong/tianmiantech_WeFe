# 基础信息

|      |      |
|------|------|
| 名称 | ProjectMemberAuditMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/ProjectMemberAuditMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ProjectMemberAuditMySqlModel | class |  |



## 类 ProjectMemberAuditMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "project_member_audit");public |
| 类型 | class |
| 名称 | ProjectMemberAuditMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| memberId | String |  |
| auditComment | String |  |
| projectId | String |  |
| auditResult | AuditStatus |  |
| auditorId | String |  |
| serialVersionUID = 8870060097218263816L | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getProjectId | String |  |
| setAuditorId | void |  |
| setProjectId | void |  |
| getMemberId | String |  |
| getAuditResult | AuditStatus |  |
| getAuditorId | String |  |
| setMemberId | void |  |
| setAuditResult | void |  |
| getAuditComment | String |  |
| setAuditComment | void |  |




