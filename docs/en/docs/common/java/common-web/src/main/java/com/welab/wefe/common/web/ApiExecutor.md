# Basic Information

|      |      |
|------|------|
| Name | ApiExecutor |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/ApiExecutor.java |
| Package Name | com.welab.wefe.common.web |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.SamplingLogger', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.FlowLimitByIp', 'com.welab.wefe.common.web.api.base.FlowLimitByMobile', 'com.welab.wefe.common.web.dto.ApiResult', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.slf4j.MDC', 'org.springframework.beans.BeansException', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'javax.servlet.http.HttpServletRequest', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ApiExecutor | class |  |



## Class ApiExecutor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ApiExecutor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| REQUEST_FROM_REFRESH = "request-from-refresh" | String |  |
| LOG = LoggerFactory.getLogger(ApiExecutor.class) | Logger |  |
| SLOG | SamplingLogger |  |
| API_LOG_TIME_MAP = new ConcurrentHashMap<>() | Map<String, Long> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| checkSessionToken | void |  |
| logResponse | void |  |
| checkApiPermission | void |  |
| execute | ApiResult<?> |  |
| checkFlowLimitByIp | void |  |
| checkFlowLimitByMobile | void |  |




