# Basic Information

|      |      |
|------|------|
| Name | FileSecurityChecker |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/api/file/security/FileSecurityChecker.java |
| Package Name | com.welab.wefe.serving.service.api.file.security |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.StringUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.io.IOException', 'java.util.Arrays', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FileSecurityChecker | class |  |



## Class FileSecurityChecker

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | FileSecurityChecker |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(FileSecurityChecker.class) | Logger |  |
| keywords = {"<", ">", "\\"} | String[] |  |
| ALLOW_FILE_TYPES = Arrays.asList(            "json", "zip", "txt"    ) | List<String> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| doCheck | void |  |
| check | void |  |
| checkIsAllowFileType | void |  |




