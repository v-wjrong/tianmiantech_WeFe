# 基础信息

|      |      |
|------|------|
| 名称 | MyCorsFilter |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/config/MyCorsFilter.java |
| 包名 | com.welab.wefe.common.web.config |
| 依赖项 | ['com.welab.wefe.common.util.StringUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.http.HttpHeaders', 'org.springframework.web.cors', 'org.springframework.web.filter.OncePerRequestFilter', 'javax.servlet.FilterChain', 'javax.servlet.ServletException', 'javax.servlet.http.HttpServletRequest', 'javax.servlet.http.HttpServletResponse', 'java.io.IOException', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MyCorsFilter | class |  |



## 类 MyCorsFilter

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MyCorsFilter |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| processor = new DefaultCorsProcessor() | CorsProcessor |  |
| configSource | CorsConfigurationSource |  |
| corsConfiguration | CorsConfiguration |  |
| needCheckCors | boolean |  |
| allowedOriginString | String |  |
| allowedOrigins | List<String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| blockRequest | boolean |  |
| doFilterInternal | void |  |
| setCorsInfoIntoResponseHeader | void |  |




