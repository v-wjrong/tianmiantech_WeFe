# Basic Information

|      |      |
|------|------|
| Name | FlowLimitByMobileService |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/service/flowlimit/FlowLimitByMobileService.java |
| Package Name | com.welab.wefe.common.web.service.flowlimit |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.FlowLimitByMobile', 'com.welab.wefe.common.wefe.enums.FlowLimitStrategyTypeEnum', 'javax.servlet.http.HttpServletRequest', 'java.util.Arrays', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FlowLimitByMobileService | class |  |



## Class FlowLimitByMobileService

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | FlowLimitByMobileService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| PARAMS_MOBILE_KEY = Arrays.asList("mobile", "phoneNumber", "phone_number") | List<String> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getFlowLimitStrategyValue | String |  |
| getFlowLimitStrategyType | FlowLimitStrategyTypeEnum |  |
| getFlowLimitSecond | long |  |
| getFlowLimitKey | String |  |
| getFlowLimitCount | int |  |
| getFlowLimitExceptionTips | String |  |
| getMobile | String |  |




