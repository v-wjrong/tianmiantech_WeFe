# Basic Information

|      |      |
|------|------|
| Name | FileSecurityChecker |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/file/security/FileSecurityChecker.java |
| Package Name | com.welab.wefe.board.service.api.file.security |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.StringUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.util.Arrays', 'java.util.List'] |
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
| keywords = {"<", ">", "\\"} | String[] |  |
| ALLOW_FILE_TYPES = Arrays.asList(            "xls", "xlsx", "csv",            "zip", "gz", "tgz", "7z",            "jpg", "jpeg", "png"    ) | List<String> |  |
| LOG = LoggerFactory.getLogger(FileSecurityChecker.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| doCheck | void |  |
| check | void |  |
| checkIsAllowFileType | void |  |




