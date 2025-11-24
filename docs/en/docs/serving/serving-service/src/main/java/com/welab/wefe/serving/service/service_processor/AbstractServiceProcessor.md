# Basic Information

|      |      |
|------|------|
| Name | AbstractServiceProcessor |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service_processor/AbstractServiceProcessor.java |
| Package Name | com.welab.wefe.serving.service.service_processor |
| Dependencies | ['java.util.ArrayList', 'java.util.List', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.service.service.DataSourceService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractServiceProcessor | class |  |



## Class AbstractServiceProcessor

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractServiceProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| calllogs = new ArrayList<>() | List<JSONObject> |  |
| dataSourceService = Launcher.getBean(DataSourceService.class) | DataSourceService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| calllogs | List<JSONObject> |  |
| addCalllog | void |  |
| addCalllog | void |  |
| process | JObject |  |




