# 基础信息

|      |      |
|------|------|
| 名称 | ApiRequestRecordService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ApiRequestRecordService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['java.util.ArrayList', 'java.util.Calendar', 'java.util.Date', 'java.util.List', 'java.util.TimeZone', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.service.api.apirequestrecord.QueryListApi', 'com.welab.wefe.serving.service.database.entity.ApiRequestRecordMysqlModel', 'com.welab.wefe.serving.service.database.repository.ApiRequestRecordRepository', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.ServiceResultEnum', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ApiRequestRecordService | class |  |



## 类 ApiRequestRecordService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ApiRequestRecordService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| apiRequestRecordRepository | ApiRequestRecordRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getList | List<ApiRequestRecordMysqlModel> |  |
| getListById | PagingOutput<QueryListApi.Output> |  |
| getList | List<ApiRequestRecordMysqlModel> |  |
| save | void |  |




