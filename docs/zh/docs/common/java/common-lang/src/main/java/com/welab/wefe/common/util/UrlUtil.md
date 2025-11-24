# 基础信息

|      |      |
|------|------|
| 名称 | UrlUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/UrlUtil.java |
| 包名 | com.welab.wefe.common.util |
| 依赖项 | ['org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.UnsupportedEncodingException', 'java.net.URI', 'java.net.URISyntaxException', 'java.net.URLDecoder', 'java.net.URLEncoder', 'java.nio.charset.StandardCharsets', 'java.util.HashMap', 'java.util.Map', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UrlUtil | class |  |



## 类 UrlUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | UrlUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(StringUtil.class) | Logger |  |
| PATTERN_MATCH_QUERY_STRING = Pattern.compile("(?<name>[^?&]+)=(?<value>[^?&]+)") | Pattern |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| decode | String |  |
| createUri | URI |  |
| decode | String |  |
| encode | String |  |
| appendQueryParameters | String |  |
| queryString2Map | Map<String, String> |  |
| setValue | String |  |
| encode | String |  |
| appendQueryParameters | String |  |
| params2QueryString | String |  |
| appendQueryParameter | String |  |
| getValue | String |  |
| params2QueryString | String |  |
| queryString2Map | Map<String, String> |  |




