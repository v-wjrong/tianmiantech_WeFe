# Basic Information

|      |      |
|------|------|
| Name | HttpResponse |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/http/HttpResponse.java |
| Package Name | com.welab.wefe.common.http |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.fastjson.LoggerValueFilter', 'com.welab.wefe.common.util.StringUtil', 'org.apache.commons.codec.binary.Base64', 'org.apache.commons.lang3.StringUtils', 'org.apache.http.Header', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.UnsupportedEncodingException', 'java.nio.charset.StandardCharsets', 'java.util.HashMap', 'java.util.Map', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HttpResponse | class |  |



## Class HttpResponse

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HttpResponse |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| bodyBytes | byte[] |  |
| sessionId | String |  |
| contentType | String |  |
| url | String |  |
| code | int |  |
| encoding | String |  |
| error | Exception |  |
| message | String |  |
| CODE_ERROR = -1 | int |  |
| PATTERN_MATCH_CHARSET = Pattern.compile("(?<=charset=)[a-z0-9\\-]+", Pattern.CASE_INSENSITIVE) | Pattern |  |
| request | HttpRequest |  |
| spend | long |  |
| bodyAsString | String |  |
| LOG = LoggerFactory.getLogger(HttpResponse.class) | Logger |  |
| headers = new HashMap<>() | Map<String, String> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| create | HttpResponse |  |
| getMessage | String |  |
| getBodyAsString | String |  |
| getBodyAsBase64 | String |  |
| success | boolean |  |
| error | HttpResponse |  |
| getError | Exception |  |
| create | HttpResponse |  |
| getBodyBytes | byte[] |  |
| log | void |  |
| getCode | int |  |
| getSpend | long |  |
| header | HttpResponse |  |
| getContentType | String |  |
| url | HttpResponse |  |
| statusCode | HttpResponse |  |
| isCacheEntity | boolean |  |
| body | HttpResponse |  |
| message | HttpResponse |  |
| getBodyAsJson | JSONObject |  |
| getRequest | HttpRequest |  |
| getHeaders | Map<String, String> |  |
| getEncoding | String |  |
| setRequest | void |  |
| setSpend | void |  |
| getUrl | String |  |




