# 基础信息

|      |      |
|------|------|
| 名称 | HttpResponse |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/http/HttpResponse.java |
| 包名 | com.welab.wefe.common.http |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.fastjson.LoggerValueFilter', 'com.welab.wefe.common.util.StringUtil', 'org.apache.commons.codec.binary.Base64', 'org.apache.commons.lang3.StringUtils', 'org.apache.http.Header', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.UnsupportedEncodingException', 'java.nio.charset.StandardCharsets', 'java.util.HashMap', 'java.util.Map', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| HttpResponse | class |  |



## 类 HttpResponse

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | HttpResponse |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




