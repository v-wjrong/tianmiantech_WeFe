# 基础信息

|      |      |
|------|------|
| 名称 | ClientService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ClientService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.service.api.client.QueryClientApi', 'com.welab.wefe.serving.service.api.client.QueryClientListApi', 'com.welab.wefe.serving.service.api.client.SaveClientApi', 'com.welab.wefe.serving.service.api.client.UpdateApi', 'com.welab.wefe.serving.service.database.entity.ClientMysqlModel', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.repository.ClientRepository', 'com.welab.wefe.serving.service.database.repository.ClientServiceRepository', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.ClientStatusEnum', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClientService | class |  |



## 类 ClientService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ClientService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clientRepository | ClientRepository |  |
| clientServiceRepository | ClientServiceRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| queryByCode | ClientMysqlModel |  |
| queryByServiceIdAndClientId | ClientServiceMysqlModel |  |
| queryByClientName | ClientMysqlModel |  |
| update | void |  |
| queryList | PagingOutput<QueryClientListApi.Output> |  |
| save | void |  |
| detele | void |  |
| queryByClientId | ClientMysqlModel |  |
| queryById | QueryClientApi.Output |  |
| queryByName | QueryClientApi.Output |  |




