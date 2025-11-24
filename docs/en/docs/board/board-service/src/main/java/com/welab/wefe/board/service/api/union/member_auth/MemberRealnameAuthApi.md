# Basic Information

|      |      |
|------|------|
| Name | MemberRealnameAuthApi |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/union/member_auth/MemberRealnameAuthApi.java |
| Package Name | com.welab.wefe.board.service.api.union.member_auth |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.database.entity.cert.CertRequestInfoMysqlModel', 'com.welab.wefe.board.service.sdk.union.UnionService', 'com.welab.wefe.board.service.service.CertOperationService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.IOException', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberRealnameAuthApi | class |  |



## Class MemberRealnameAuthApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "union/member/realname/auth", name = "apply realname auth");public |
| Type | class |
| Name | MemberRealnameAuthApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| unionService | UnionService |  |
| certOperationService | CertOperationService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateCertRequestContent | void |  |
| handle | ApiResult<Object> |  |




