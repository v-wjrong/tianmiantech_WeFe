# Basic Information

|      |      |
|------|------|
| Name | ServingFileUtil |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/utils/ServingFileUtil.java |
| Package Name | com.welab.wefe.serving.service.utils |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.file.compression.impl.Zip', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.service.config.Config', 'java.io.File', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServingFileUtil | class |  |



## Class ServingFileUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ServingFileUtil |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| ROOT_DIR = Paths.get(Launcher.getBean(Config.class).getFileUploadDir()) | Path |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getRootDir | Path |  |
| getBaseDir | Path |  |




