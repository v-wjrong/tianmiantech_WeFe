# Basic Information

|      |      |
|------|------|
| Name | ModelManager |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/manager/ModelManager.java |
| Package Name | com.welab.wefe.serving.service.manager |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.sdk.model.BaseModel', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.service.CacheObjects', 'com.welab.wefe.serving.service.service.ModelService', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelManager | class |  |



## Class ModelManager

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ModelManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| modelService | ModelService |  |
| MODEL = new HashMap<>() | Map<String, BaseModel> |  |
| MODEL_ENABLE = new HashMap<>() | Map<String, Boolean> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getModelParam | BaseModel |  |
| getModelParam | BaseModel |  |
| getModelEnable | Boolean |  |
| refreshModelEnable | void |  |




