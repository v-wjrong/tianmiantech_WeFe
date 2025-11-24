# 基础信息

|      |      |
|------|------|
| 名称 | ModelProcessorManager |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-sdk-java/src/main/java/com/welab/wefe/serving/sdk/manager/ModelProcessorManager.java |
| 包名 | com.welab.wefe.serving.sdk.manager |
| 依赖项 | ['com.welab.wefe.common.util.ReflectionsUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.sdk.processor', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelProcessorManager | class |  |



## 类 ModelProcessorManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ModelProcessorManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MAP = new HashMap<>() | Map<String, Class<? extends AbstractModelProcessor>> |  |
| MAP_BATCH_PROCESSOR = new HashMap<>() | Map<String, Class<? extends AbstractBatchModelProcessor>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getProcessor | AbstractModelProcessor |  |
| init | void |  |
| getBatchProcessor | AbstractBatchModelProcessor |  |




