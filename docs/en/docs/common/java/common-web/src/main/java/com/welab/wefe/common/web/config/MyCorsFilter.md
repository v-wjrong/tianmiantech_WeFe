# Basic Information

|      |      |
|------|------|
| Name | MyCorsFilter |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/config/MyCorsFilter.java |
| Package Name | com.welab.wefe.common.web.config |
| Dependencies | ['com.welab.wefe.common.util.StringUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.http.HttpHeaders', 'org.springframework.web.cors', 'org.springframework.web.filter.OncePerRequestFilter', 'javax.servlet.FilterChain', 'javax.servlet.ServletException', 'javax.servlet.http.HttpServletRequest', 'javax.servlet.http.HttpServletResponse', 'java.io.IOException', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MyCorsFilter | class |  |



## Class MyCorsFilter

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MyCorsFilter |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| processor = new DefaultCorsProcessor() | CorsProcessor |  |
| configSource | CorsConfigurationSource |  |
| corsConfiguration | CorsConfiguration |  |
| needCheckCors | boolean |  |
| allowedOriginString | String |  |
| allowedOrigins | List<String> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| blockRequest | boolean |  |
| doFilterInternal | void |  |
| setCorsInfoIntoResponseHeader | void |  |




