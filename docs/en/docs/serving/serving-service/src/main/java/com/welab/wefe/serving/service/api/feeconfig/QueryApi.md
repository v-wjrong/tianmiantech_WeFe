# Basic Information

|      |      |
|------|------|
| Name | QueryApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/feeconfig/QueryApi.java |
| Package Name | com.welab.wefe.serving.service.api.feeconfig |
| Dependencies | ['com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.database.entity.FeeConfigMysqlModel', 'com.welab.wefe.serving.service.service.FeeConfigService', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| QueryApi | class |  |



## Class QueryApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "feeconfig/query-one", name = "query fee config");public |
| Type | class |
| Name | QueryApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| feeConfigService | FeeConfigService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<FeeConfigMysqlModel> |  |




