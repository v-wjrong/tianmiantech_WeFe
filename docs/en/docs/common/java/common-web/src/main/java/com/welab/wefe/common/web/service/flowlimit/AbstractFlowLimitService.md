# Basic Information

|      |      |
|------|------|
| Name | AbstractFlowLimitService |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/service/flowlimit/AbstractFlowLimitService.java |
| Package Name | com.welab.wefe.common.web.service.flowlimit |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.wefe.enums.FlowLimitStrategyTypeEnum', 'javax.servlet.http.HttpServletRequest'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractFlowLimitService | class |  |



## Class AbstractFlowLimitService

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractFlowLimitService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| httpServletRequest | HttpServletRequest |  |
| api | AbstractApi<?, ?> |  |
| params | JSONObject |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getApi | AbstractApi<?, ?> |  |
| setHttpServletRequest | void |  |
| setApi | void |  |
| getParams | JSONObject |  |
| setParams | void |  |
| getFlowLimitSecond | long |  |
| updateFlowLimit | void |  |
| getFlowLimitCount | int |  |
| getFlowLimitStrategyValue | String |  |
| getFlowLimitExceptionTips | String |  |
| getFlowLimit | FlowLimit |  |
| getHttpServletRequest | HttpServletRequest |  |
| check | void |  |
| getFlowLimitStrategyType | FlowLimitStrategyTypeEnum |  |
| getFlowLimitKey | String |  |
| createFlowLimit | FlowLimit |  |




