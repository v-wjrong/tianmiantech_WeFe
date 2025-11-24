# Basic Information

|      |      |
|------|------|
| Name | ClassifyImageDataSetParser |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/image_data_set/data_set_parser/ClassifyImageDataSetParser.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.image_data_set.data_set_parser |
| Dependencies | ['com.welab.wefe.board.service.database.entity.data_resource.ImageDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.data_set.ImageDataSetSampleMysqlModel', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.file.compression.impl.Tgz', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.ListUtil', 'com.welab.wefe.common.util.StringUtil', 'java.io.File', 'java.io.IOException', 'java.nio.file.Files', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.util', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClassifyImageDataSetParser | class |  |



## Class ClassifyImageDataSetParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ClassifyImageDataSetParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| SAMPLE_LABEL_PATTERN = Pattern.compile("^(?<sample>.+)\\s+(?<index>\\d+)\\s*$") | Pattern |  |
| TRAIN_LIST_FILE_NAME = "train_list.txt" | String |  |
| LABEL_LIST_FILE_NAME = "label_list.txt" | String |  |
| VAL_LIST_FILE_NAME = "val_list.txt" | String |  |
| IMAGE_DIR_NAME = "jpg" | String |  |
| LABEL_LIST_PATTERN = Pattern.compile("^\\s*(?<index>\\d+)\\s+(?<label>.+)\\s*$") | Pattern |  |
| TEST_LIST_FILE_NAME = "test_list.txt" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getLabelIndexMap | Map<Integer, String> |  |
| getSampleLabelIndexMap | Map<String, Integer> |  |
| emitImageFile | void |  |
| parseFilesToSamples | List<ImageDataSetSampleMysqlModel> |  |
| emitSamples | void |  |
| emitSamplesToDataSetFileDir | void |  |
| emitLabelListFile | List<String> |  |
| createSample | ImageDataSetSampleMysqlModel |  |




