# 基础信息

|      |      |
|------|------|
| 名称 | AbstractTemplate |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/feature/sql/AbstractTemplate.java |
| 包名 | com.welab.wefe.serving.service.feature.sql |
| 依赖项 | ['com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractTemplate | class |  |



## 类 AbstractTemplate

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractTemplate |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| host | String |  |
| port | int |  |
| database | String |  |
| placeholder = "?" | String |  |
| databaseType | DatabaseType |  |
| username | String |  |
| logger = LoggerFactory.getLogger(getClass()) | Logger |  |
| password | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| execute | Map<String, Object> |  |
| handle | Map<String, Object> |  |




