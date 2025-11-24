# Basic Information

|      |      |
|------|------|
| Name | BaseController |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/controller/BaseController.java |
| Package Name | com.welab.wefe.common.web.controller |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.parser.Feature', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.UrlUtil', 'com.welab.wefe.common.web.ApiExecutor', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'org.apache.catalina.connector.RequestFacade', 'org.springframework.core.io.ClassPathResource', 'org.springframework.core.io.FileSystemResource', 'org.springframework.http.HttpHeaders', 'org.springframework.http.MediaType', 'org.springframework.http.ResponseEntity', 'org.springframework.util.FileCopyUtils', 'org.springframework.util.MultiValueMap', 'org.springframework.web.bind.annotation.GetMapping', 'org.springframework.web.bind.annotation.PostMapping', 'org.springframework.web.bind.annotation.RestController', 'org.springframework.web.multipart.MultipartFile', 'org.springframework.web.multipart.support.StandardMultipartHttpServletRequest', 'javax.servlet.http.HttpServletRequest', 'java.io.BufferedReader', 'java.io.File', 'java.io.IOException', 'java.util.Map', 'java.util.TreeMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BaseController | class |  |



## Class BaseController

|      |      |
|------|------|
| Access Modifier | @RestController;public |
| Type | class |
| Name | BaseController |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| download | ResponseEntity<FileSystemResource> |  |
| post | ResponseEntity<ApiResult<?>> |  |
| getBodyParamsFromHttpRequest | JSONObject |  |
| get | ResponseEntity<?> |  |
| buildRequestParams | JSONObject |  |




