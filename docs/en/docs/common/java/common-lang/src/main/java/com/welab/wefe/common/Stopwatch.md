# Basic Information

|      |      |
|------|------|
| Name | Stopwatch |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/Stopwatch.java |
| Package Name | com.welab.wefe.common |
| Dependencies | ['org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.LinkedList'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Stopwatch | class |  |



## Class Stopwatch

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | Stopwatch |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| EMPTY_LOG_NAME = "" | String |  |
| maxLabelQueueLength | int |  |
| labelQueue | LinkedList<Label> |  |
| logger = LoggerFactory.getLogger(Stopwatch.class) | Logger |  |
| lastTapTime | Long |  |
| DEFAULT_LABEL_QUEUE_CAPACITY = 100 | int |  |
| startTime | Long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| tap | Label |  |
| tapAndPrint | Label |  |
| startNew | Stopwatch |  |
| getTotalSpend | long |  |
| printAllTap | void |  |
| tap | Label |  |
| startNew | Stopwatch |  |




