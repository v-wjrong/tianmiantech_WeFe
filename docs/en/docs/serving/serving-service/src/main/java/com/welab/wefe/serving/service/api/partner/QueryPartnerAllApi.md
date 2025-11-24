# Basic Information

|      |      |
|------|------|
| Name | QueryPartnerAllApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/partner/QueryPartnerAllApi.java |
| Package Name | com.welab.wefe.serving.service.api.partner |
| Dependencies | ['java.util.Date', 'java.util.List', 'org.springframework.beans.factory.annotation.Autowired', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractNoneInputApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.dto.PagingInput', 'com.welab.wefe.serving.service.service.PartnerService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| QueryPartnerAllApi | class |  |



## Class QueryPartnerAllApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "partner/query-all", name = "get partner list");public |
| Type | class |
| Name | QueryPartnerAllApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerService | PartnerService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<List<QueryPartnerAllApi.Output>> |  |




