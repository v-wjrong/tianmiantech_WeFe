# 基础信息

|      |      |
|------|------|
| 名称 | JobMemberMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/job/JobMemberMySqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| JobMemberMySqlModel | class |  |



## 类 JobMemberMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "job_member");public |
| 类型 | class |
| 名称 | JobMemberMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| flowId | String |  |
| jobId | String |  |
| memberId | String |  |
| dataSetId | String |  |
| projectId | String |  |
| jobRole | JobMemberRole |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getMemberId | String |  |
| setMemberId | void |  |
| getDataSetId | String |  |
| setDataSetId | void |  |
| setFlowId | void |  |
| setJobRole | void |  |
| setProjectId | void |  |
| getFlowId | String |  |
| getProjectId | String |  |
| getJobId | String |  |
| getJobRole | JobMemberRole |  |
| setJobId | void |  |




