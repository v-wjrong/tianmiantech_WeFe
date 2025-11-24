# 基础信息

|      |      |
|------|------|
| 名称 | ApiExecutor |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/ApiExecutor.java |
| 包名 | com.welab.wefe.common.web |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.SamplingLogger', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.FlowLimitByIp', 'com.welab.wefe.common.web.api.base.FlowLimitByMobile', 'com.welab.wefe.common.web.dto.ApiResult', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.slf4j.MDC', 'org.springframework.beans.BeansException', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'javax.servlet.http.HttpServletRequest', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ApiExecutor | class |  |



## 类 ApiExecutor

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ApiExecutor |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| REQUEST_FROM_REFRESH = "request-from-refresh" | String |  |
| LOG = LoggerFactory.getLogger(ApiExecutor.class) | Logger |  |
| SLOG | SamplingLogger |  |
| API_LOG_TIME_MAP = new ConcurrentHashMap<>() | Map<String, Long> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| checkSessionToken | void |  |
| logResponse | void |  |
| checkApiPermission | void |  |
| execute | ApiResult<?> |  |
| checkFlowLimitByIp | void |  |
| checkFlowLimitByMobile | void |  |




