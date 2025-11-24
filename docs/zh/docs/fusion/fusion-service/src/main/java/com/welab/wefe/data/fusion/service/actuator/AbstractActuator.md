# 基础信息

|      |      |
|------|------|
| 名称 | AbstractActuator |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/actuator/AbstractActuator.java |
| 包名 | com.welab.wefe.data.fusion.service.actuator |
| 依赖项 | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.data.fusion.service.manager.TaskResultManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.concurrent.atomic.LongAdder'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractActuator | class |  |



## 类 AbstractActuator

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractActuator |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| DUMP_TABLE_EXIST = false | boolean |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| dataCount | Integer |  |
| processedCount = new LongAdder() | LongAdder |  |
| fusionCount = new LongAdder() | LongAdder |  |
| businessId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| init | void |  |
| handle | void |  |
| createTable | void |  |
| dump | void |  |




