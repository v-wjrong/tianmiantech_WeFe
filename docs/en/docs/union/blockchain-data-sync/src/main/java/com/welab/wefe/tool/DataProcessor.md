# Basic Information

|      |      |
|------|------|
| Name | DataProcessor |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/tool/DataProcessor.java |
| Package Name | com.welab.wefe.tool |
| Dependencies | ['com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.exception.BusinessException', 'com.welab.wefe.parser.AbstractParser', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.HashMap', 'java.util.Map', 'java.util.Set'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataProcessor | class |  |



## Class DataProcessor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DataProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| log = LoggerFactory.getLogger(DataProcessor.class) | Logger |  |
| ABSTRACT = "Abstract" | String |  |
| EVENT_PARSER_SUFFIX = "EventParser" | String |  |
| CLASS_MAP = new HashMap<>() | Map<String, Class<?>> |  |
| PARSER_PKG = "com.welab.wefe.parser" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseBlockData | Boolean |  |
| getPackageAllClasses | void |  |
| createInstance | Object |  |




