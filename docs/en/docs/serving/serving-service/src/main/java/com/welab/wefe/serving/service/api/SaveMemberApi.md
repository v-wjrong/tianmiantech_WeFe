# Basic Information

|      |      |
|------|------|
| Name | SaveMemberApi |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/SaveMemberApi.java |
| Package Name | com.welab.wefe.serving.service.api |
| Dependencies | ['com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractNoneOutputApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.Caller', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.serving.service.service.MemberService', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SaveMemberApi | class |  |



## Class SaveMemberApi

|      |      |
|------|------|
| Access Modifier | @Api(;        path = "member_save",;        name = "保存成员信息",;        allowAccessWithSign = true,;        domain = Caller.Board;);public |
| Type | class |
| Name | SaveMemberApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberService | MemberService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handler | ApiResult<?> |  |




