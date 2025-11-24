# Basic Information

|      |      |
|------|------|
| Name | WeFeFileSystem |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/base/file_system/WeFeFileSystem.java |
| Package Name | com.welab.wefe.board.service.base.file_system |
| Dependencies | ['com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.file.compression.impl.Zip', 'com.welab.wefe.common.file.decompression.SuperDecompressor', 'com.welab.wefe.common.file.decompression.dto.DecompressionResult', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| WeFeFileSystem | class |  |



## Class WeFeFileSystem

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | WeFeFileSystem |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| ROOT_DIR = Paths.get(Launcher.getBean(Config.class).getFileUploadDir()) | Path |  |
| LOG = LoggerFactory.getLogger(WeFeFileSystem.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getRootDir | Path |  |
| getFilePath | Path |  |
| getFilePath | Path |  |
| getBaseDir | Path |  |
| getFileDir | Path |  |




