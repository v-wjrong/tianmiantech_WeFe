# Basic Information

|      |      |
|------|------|
| Name | AbstractImageDataSetParser |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/image_data_set/data_set_parser/AbstractImageDataSetParser.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.image_data_set.data_set_parser |
| Dependencies | ['com.welab.wefe.board.service.database.entity.data_resource.ImageDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.data_set.ImageDataSetSampleMysqlModel', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.file.compression.impl.Zip', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'org.apache.commons.io.FileUtils', 'java.io.File', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractImageDataSetParser | class |  |



## Class AbstractImageDataSetParser

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractImageDataSetParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getDataSetFileName | String |  |
| parseFilesToSamples | List<ImageDataSetSampleMysqlModel> |  |
| getDataSetFile | File |  |
| getParser | AbstractImageDataSetParser |  |
| emitSamplesToDataSetFileDir | void |  |
| parseSamplesToDataSetFile | String |  |
| parseFilesToSamples | List<ImageDataSetSampleMysqlModel> |  |
| createSampleModel | ImageDataSetSampleMysqlModel |  |




