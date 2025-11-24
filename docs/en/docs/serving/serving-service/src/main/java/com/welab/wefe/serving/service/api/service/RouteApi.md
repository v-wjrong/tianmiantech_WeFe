# Basic Information

|      |      |
|------|------|
| Name | RouteApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/service/RouteApi.java |
| Package Name | com.welab.wefe.serving.service.api.service |
| Dependencies | ['org.springframework.beans.factory.annotation.Autowired', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.Caller', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.enums.ServiceResultEnum', 'com.welab.wefe.serving.service.service.ServiceService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RouteApi | class |  |



## Class RouteApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "api", name = "api service", forward = true, allowAccessWithSign = true, domain = Caller.Customer);public |
| Type | class |
| Name | RouteApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| serviceService | ServiceService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parallelism | int |  |
| canParallel | boolean |  |
| handle | ApiResult<JObject> |  |




