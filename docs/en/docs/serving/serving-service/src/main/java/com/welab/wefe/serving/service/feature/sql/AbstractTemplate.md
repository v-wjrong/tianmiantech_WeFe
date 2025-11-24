# Basic Information

|      |      |
|------|------|
| Name | AbstractTemplate |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/feature/sql/AbstractTemplate.java |
| Package Name | com.welab.wefe.serving.service.feature.sql |
| Dependencies | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractTemplate | class |  |



## Class AbstractTemplate

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractTemplate |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| host | String |  |
| port | int |  |
| database | String |  |
| placeholder = "?" | String |  |
| databaseType | DatabaseType |  |
| username | String |  |
| logger = LoggerFactory.getLogger(getClass()) | Logger |  |
| password | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| execute | Map<String, Object> |  |
| handle | Map<String, Object> |  |




