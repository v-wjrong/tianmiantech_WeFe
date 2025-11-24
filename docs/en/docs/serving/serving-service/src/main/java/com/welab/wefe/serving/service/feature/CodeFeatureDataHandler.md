# Basic Information

|      |      |
|------|------|
| Name | CodeFeatureDataHandler |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/feature/CodeFeatureDataHandler.java |
| Package Name | com.welab.wefe.serving.service.feature |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.ReflectionsUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.sdk.model.FeatureDataModel', 'com.welab.wefe.serving.service.feature.code', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CodeFeatureDataHandler | class |  |



## Class CodeFeatureDataHandler

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CodeFeatureDataHandler |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| MAP = new HashMap<>() | Map<String, Class<? extends AbstractFeatureDataProcessor>> |  |
| LOG = LoggerFactory.getLogger(CodeFeatureDataHandler.class) | Logger |  |
| BATCH_MAP = new HashMap<>() | Map<String, Class<? extends AbstractBatchFeatureDataProcessor>> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSimpleName | String |  |
| get | AbstractFeatureDataProcessor |  |
| getBatch | AbstractBatchFeatureDataProcessor |  |
| handle | FeatureDataModel |  |
| init | void |  |
| getList | List<String> |  |




