# Basic Information

|      |      |
|------|------|
| Name | AbstractCheckpoint |
| Language | .java |
| Code Path | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/checkpoint/AbstractCheckpoint.java |
| Package Name | com.welab.wefe.common.wefe.checkpoint |
| Dependencies | ['com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.checkpoint.dto.ServiceCheckPointOutput', 'com.welab.wefe.common.wefe.enums.ServiceType', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.Future', 'java.util.concurrent.TimeUnit', 'java.util.concurrent.TimeoutException'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractCheckpoint | class |  |



## Class AbstractCheckpoint

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractCheckpoint |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| configValue | String |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| service | ServiceType |  |
| tryCheck | Exception |  |
| check | ServiceCheckPointOutput |  |
| desc | String |  |
| doCheck | void |  |
| getConfigValue | String |  |
| messageWhenConfigValueEmpty | String |  |
| tryGetConfigValue | String |  |
| skip | boolean |  |
| log | void |  |




