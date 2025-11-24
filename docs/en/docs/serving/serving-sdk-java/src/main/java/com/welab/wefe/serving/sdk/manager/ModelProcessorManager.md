# Basic Information

|      |      |
|------|------|
| Name | ModelProcessorManager |
| Language | .java |
| Code Path | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/manager/ModelProcessorManager.java |
| Package Name | com.welab.wefe.serving.sdk.manager |
| Dependencies | ['com.welab.wefe.common.util.ReflectionsUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.sdk.processor', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelProcessorManager | class |  |



## Class ModelProcessorManager

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ModelProcessorManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| MAP = new HashMap<>() | Map<String, Class<? extends AbstractModelProcessor>> |  |
| MAP_BATCH_PROCESSOR = new HashMap<>() | Map<String, Class<? extends AbstractBatchModelProcessor>> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getProcessor | AbstractModelProcessor |  |
| init | void |  |
| getBatchProcessor | AbstractBatchModelProcessor |  |




