# 基础信息

|      |      |
|------|------|
| 名称 | AbstractApi |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/api/base/AbstractApi.java |
| 包名 | com.welab.wefe.common.web.api.base |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.enums.ContentType', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractWithFilesApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.core.io.FileSystemResource', 'org.springframework.http.HttpHeaders', 'org.springframework.http.MediaType', 'org.springframework.http.ResponseEntity', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'javax.servlet.http.HttpServletRequest', 'java.io.File', 'java.lang.reflect.ParameterizedType', 'java.lang.reflect.Type', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.LongAdder'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractApi | class |  |



## 类 AbstractApi

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| API_PARALLELISM = new ConcurrentHashMap<>() | Map<String, LongAdder> |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




