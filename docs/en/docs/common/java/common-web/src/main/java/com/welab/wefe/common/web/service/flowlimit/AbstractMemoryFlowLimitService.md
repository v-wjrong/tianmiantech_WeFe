# Basic Information

|      |      |
|------|------|
| Name | AbstractMemoryFlowLimitService |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/service/flowlimit/AbstractMemoryFlowLimitService.java |
| Package Name | com.welab.wefe.common.web.service.flowlimit |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'javax.servlet.http.HttpServletRequest', 'java.util.Iterator', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractMemoryFlowLimitService | class |  |



## Class AbstractMemoryFlowLimitService

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractMemoryFlowLimitService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| FLOW_LIMIT_CACHE = new ConcurrentHashMap<>(16) | ConcurrentHashMap<String, AbstractFlowLimitService.FlowLimit> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getFlowLimit | FlowLimit |  |
| updateFlowLimit | void |  |




