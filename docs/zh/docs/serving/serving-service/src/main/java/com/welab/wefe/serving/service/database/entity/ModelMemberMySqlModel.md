# 基础信息

|      |      |
|------|------|
| 名称 | ModelMemberMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ModelMemberMySqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.service.enums.MemberModelStatusEnum', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelMemberMySqlModel | class |  |



## 类 ModelMemberMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "model_member");public |
| 类型 | class |
| 名称 | ModelMemberMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| status = MemberModelStatusEnum.offline | MemberModelStatusEnum |  |
| memberId | String |  |
| modelId | String |  |
| role | JobMemberRole |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getModelId | String |  |
| setMemberId | void |  |
| setModelId | void |  |
| getMemberId | String |  |
| getRole | JobMemberRole |  |
| setRole | void |  |
| getStatus | MemberModelStatusEnum |  |
| setStatus | void |  |




