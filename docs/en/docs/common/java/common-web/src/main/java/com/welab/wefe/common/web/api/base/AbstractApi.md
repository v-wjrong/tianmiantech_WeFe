# Basic Information

|      |      |
|------|------|
| Name | AbstractApi |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/api/base/AbstractApi.java |
| Package Name | com.welab.wefe.common.web.api.base |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.enums.ContentType', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractWithFilesApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.core.io.FileSystemResource', 'org.springframework.http.HttpHeaders', 'org.springframework.http.MediaType', 'org.springframework.http.ResponseEntity', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'javax.servlet.http.HttpServletRequest', 'java.io.File', 'java.lang.reflect.ParameterizedType', 'java.lang.reflect.Type', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.LongAdder'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractApi | class |  |



## Class AbstractApi

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| API_PARALLELISM = new ConcurrentHashMap<>() | Map<String, LongAdder> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| execute | ApiResult<Out> |  |
| fail | ApiResult<?> |  |
| file | ApiResult<ResponseEntity<?>> |  |
| canParallel | boolean |  |
| parallelism | int |  |
| success | ApiResult<Out> |  |
| fail | ApiResult<Out> |  |
| unionApiResultToBoardApiResult | ApiResult<Object> |  |
| fail | ApiResult<Out> |  |
| handle | ApiResult<Out> |  |
| fail | ApiResult<Out> |  |
| getInputClass | Class<In> |  |
| fail | ApiResult<Out> |  |
| execute | ApiResult<Out> |  |
| checkParallelism | boolean |  |
| success | ApiResult<Out> |  |
| execute | ApiResult<Out> |  |
| fail | ApiResult<Out> |  |




