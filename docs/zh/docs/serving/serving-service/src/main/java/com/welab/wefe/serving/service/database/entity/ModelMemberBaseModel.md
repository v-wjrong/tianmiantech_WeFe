# 基础信息

|      |      |
|------|------|
| 名称 | ModelMemberBaseModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ModelMemberBaseModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.Id', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelMemberBaseModel | class |  |



## 类 ModelMemberBaseModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "model_member_base");public |
| 类型 | class |
| 名称 | ModelMemberBaseModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| id = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| role | String |  |
| api | String |  |
| memberId | String |  |
| modelId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setMemberId | void |  |
| getId | String |  |
| getRole | String |  |
| getMemberId | String |  |
| setModelId | void |  |
| setId | void |  |
| setRole | void |  |
| getApi | String |  |
| getModelId | String |  |
| setApi | void |  |




