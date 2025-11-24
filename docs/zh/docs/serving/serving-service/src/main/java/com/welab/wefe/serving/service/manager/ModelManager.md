# 基础信息

|      |      |
|------|------|
| 名称 | ModelManager |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/manager/ModelManager.java |
| 包名 | com.welab.wefe.serving.service.manager |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.sdk.model.BaseModel', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.service.CacheObjects', 'com.welab.wefe.serving.service.service.ModelService', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelManager | class |  |



## 类 ModelManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ModelManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| modelService | ModelService |  |
| MODEL = new HashMap<>() | Map<String, BaseModel> |  |
| MODEL_ENABLE = new HashMap<>() | Map<String, Boolean> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getModelParam | BaseModel |  |
| getModelParam | BaseModel |  |
| getModelEnable | Boolean |  |
| refreshModelEnable | void |  |




