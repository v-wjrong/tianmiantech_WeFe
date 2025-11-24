# 基础信息

|      |      |
|------|------|
| 名称 | AbstractServiceProcessor |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service_processor/AbstractServiceProcessor.java |
| 包名 | com.welab.wefe.serving.service.service_processor |
| 依赖项 | ['java.util.ArrayList', 'java.util.List', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.service.service.DataSourceService'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractServiceProcessor | class |  |



## 类 AbstractServiceProcessor

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractServiceProcessor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| calllogs = new ArrayList<>() | List<JSONObject> |  |
| dataSourceService = Launcher.getBean(DataSourceService.class) | DataSourceService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| calllogs | List<JSONObject> |  |
| addCalllog | void |  |
| addCalllog | void |  |
| process | JObject |  |




