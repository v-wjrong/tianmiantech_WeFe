# 基础信息

|      |      |
|------|------|
| 名称 | ClassifyImageDataSetParser |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/image_data_set/data_set_parser/ClassifyImageDataSetParser.java |
| 包名 | com.welab.wefe.board.service.service.data_resource.image_data_set.data_set_parser |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.data_resource.ImageDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.data_set.ImageDataSetSampleMysqlModel', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.file.compression.impl.Tgz', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.ListUtil', 'com.welab.wefe.common.util.StringUtil', 'java.io.File', 'java.io.IOException', 'java.nio.file.Files', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.util', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClassifyImageDataSetParser | class |  |



## 类 ClassifyImageDataSetParser

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ClassifyImageDataSetParser |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| SAMPLE_LABEL_PATTERN = Pattern.compile("^(?<sample>.+)\\s+(?<index>\\d+)\\s*$") | Pattern |  |
| TRAIN_LIST_FILE_NAME = "train_list.txt" | String |  |
| LABEL_LIST_FILE_NAME = "label_list.txt" | String |  |
| VAL_LIST_FILE_NAME = "val_list.txt" | String |  |
| IMAGE_DIR_NAME = "jpg" | String |  |
| LABEL_LIST_PATTERN = Pattern.compile("^\\s*(?<index>\\d+)\\s+(?<label>.+)\\s*$") | Pattern |  |
| TEST_LIST_FILE_NAME = "test_list.txt" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getLabelIndexMap | Map<Integer, String> |  |
| getSampleLabelIndexMap | Map<String, Integer> |  |
| emitImageFile | void |  |
| parseFilesToSamples | List<ImageDataSetSampleMysqlModel> |  |
| emitSamples | void |  |
| emitSamplesToDataSetFileDir | void |  |
| emitLabelListFile | List<String> |  |
| createSample | ImageDataSetSampleMysqlModel |  |




