# 基础信息

|      |      |
|------|------|
| 名称 | Stopwatch |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/Stopwatch.java |
| 包名 | com.welab.wefe.common |
| 依赖项 | ['org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.LinkedList'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| Stopwatch | class |  |



## 类 Stopwatch

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | Stopwatch |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| EMPTY_LOG_NAME = "" | String |  |
| maxLabelQueueLength | int |  |
| labelQueue | LinkedList<Label> |  |
| logger = LoggerFactory.getLogger(Stopwatch.class) | Logger |  |
| lastTapTime | Long |  |
| DEFAULT_LABEL_QUEUE_CAPACITY = 100 | int |  |
| startTime | Long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| tap | Label |  |
| tapAndPrint | Label |  |
| startNew | Stopwatch |  |
| getTotalSpend | long |  |
| printAllTap | void |  |
| tap | Label |  |
| startNew | Stopwatch |  |




