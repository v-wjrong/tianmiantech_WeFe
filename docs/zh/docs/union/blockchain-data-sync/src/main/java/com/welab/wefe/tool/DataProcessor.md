# 基础信息

|      |      |
|------|------|
| 名称 | DataProcessor |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/tool/DataProcessor.java |
| 包名 | com.welab.wefe.tool |
| 依赖项 | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.exception.BusinessException', 'com.welab.wefe.parser.AbstractParser', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.HashMap', 'java.util.Map', 'java.util.Set'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataProcessor | class |  |



## 类 DataProcessor

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DataProcessor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| log = LoggerFactory.getLogger(DataProcessor.class) | Logger |  |
| ABSTRACT = "Abstract" | String |  |
| EVENT_PARSER_SUFFIX = "EventParser" | String |  |
| CLASS_MAP = new HashMap<>() | Map<String, Class<?>> |  |
| PARSER_PKG = "com.welab.wefe.parser" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| parseBlockData | Boolean |  |
| getPackageAllClasses | void |  |
| createInstance | Object |  |




