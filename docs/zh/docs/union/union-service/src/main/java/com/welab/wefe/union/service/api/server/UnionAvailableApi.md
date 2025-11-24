# 基础信息

|      |      |
|------|------|
| 名称 | UnionAvailableApi |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/api/server/UnionAvailableApi.java |
| 包名 | com.welab.wefe.union.service.api.server |
| 依赖项 | ['com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.wefe.checkpoint.CheckpointManager', 'com.welab.wefe.common.wefe.checkpoint.dto.ServiceAvailableCheckOutput', 'com.welab.wefe.union.service.dto.base.BaseInput', 'org.springframework.beans.factory.annotation.Autowired'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UnionAvailableApi | class |  |



## 类 UnionAvailableApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "service/available", name = "available", allowAccessWithSign = true);public |
| 类型 | class |
| 名称 | UnionAvailableApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| checkpointManager | CheckpointManager |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| handle | ApiResult<ServiceAvailableCheckOutput> |  |




