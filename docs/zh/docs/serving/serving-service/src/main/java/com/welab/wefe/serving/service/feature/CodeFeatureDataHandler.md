# 基础信息

|      |      |
|------|------|
| 名称 | CodeFeatureDataHandler |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/feature/CodeFeatureDataHandler.java |
| 包名 | com.welab.wefe.serving.service.feature |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.ReflectionsUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.sdk.model.FeatureDataModel', 'com.welab.wefe.serving.service.feature.code', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CodeFeatureDataHandler | class |  |



## 类 CodeFeatureDataHandler

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CodeFeatureDataHandler |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MAP = new HashMap<>() | Map<String, Class<? extends AbstractFeatureDataProcessor>> |  |
| LOG = LoggerFactory.getLogger(CodeFeatureDataHandler.class) | Logger |  |
| BATCH_MAP = new HashMap<>() | Map<String, Class<? extends AbstractBatchFeatureDataProcessor>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getSimpleName | String |  |
| get | AbstractFeatureDataProcessor |  |
| getBatch | AbstractBatchFeatureDataProcessor |  |
| handle | FeatureDataModel |  |
| init | void |  |
| getList | List<String> |  |




