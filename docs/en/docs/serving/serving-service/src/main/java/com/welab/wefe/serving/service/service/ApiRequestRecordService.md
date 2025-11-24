# Basic Information

|      |      |
|------|------|
| Name | ApiRequestRecordService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ApiRequestRecordService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['java.util.ArrayList', 'java.util.Calendar', 'java.util.Date', 'java.util.List', 'java.util.TimeZone', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.service.api.apirequestrecord.QueryListApi', 'com.welab.wefe.serving.service.database.entity.ApiRequestRecordMysqlModel', 'com.welab.wefe.serving.service.database.repository.ApiRequestRecordRepository', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.ServiceResultEnum', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ApiRequestRecordService | class |  |



## Class ApiRequestRecordService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ApiRequestRecordService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| apiRequestRecordRepository | ApiRequestRecordRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getList | List<ApiRequestRecordMysqlModel> |  |
| getListById | PagingOutput<QueryListApi.Output> |  |
| getList | List<ApiRequestRecordMysqlModel> |  |
| save | void |  |




