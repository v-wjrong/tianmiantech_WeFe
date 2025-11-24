# Basic Information

|      |      |
|------|------|
| Name | UnionServiceService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/UnionServiceService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONException', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.http.HttpRequest', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.RSAUtil', 'com.welab.wefe.common.util.SignUtil', 'com.welab.wefe.serving.service.api.service.UnionServiceApi', 'com.welab.wefe.serving.service.api.service.UnionServiceApi.Input', 'com.welab.wefe.serving.service.api.service.UnionServiceApi.Output', 'com.welab.wefe.serving.service.database.entity.TableServiceMySqlModel', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum', 'net.jodah.expiringmap.ExpiringMap', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.stereotype.Service', 'java.util', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UnionServiceService | class |  |



## Class UnionServiceService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | UnionServiceService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| CACHE_MAP = ExpiringMap            .builder()            .expiration(60, TimeUnit.SECONDS)            .maxSize(500)            .build() | ExpiringMap<String, Object> |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| request | JSONObject |  |
| offline2Union | JSONObject |  |
| updateServingBaseUrlOnUnion | JSONObject |  |
| query4Union | JSONObject |  |
| memberQuery | JSONObject |  |
| query | PagingOutput<Output> |  |
| request | JSONObject |  |
| add2Union | JSONObject |  |




