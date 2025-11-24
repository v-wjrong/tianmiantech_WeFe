# 基础信息

|      |      |
|------|------|
| 名称 | AbstractImageDataSetParser |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/image_data_set/data_set_parser/AbstractImageDataSetParser.java |
| 包名 | com.welab.wefe.board.service.service.data_resource.image_data_set.data_set_parser |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.data_resource.ImageDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.data_set.ImageDataSetSampleMysqlModel', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.file.compression.impl.Zip', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'org.apache.commons.io.FileUtils', 'java.io.File', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.util', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractImageDataSetParser | class |  |



## 类 AbstractImageDataSetParser

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractImageDataSetParser |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataSetFileName | String |  |
| parseFilesToSamples | List<ImageDataSetSampleMysqlModel> |  |
| getDataSetFile | File |  |
| getParser | AbstractImageDataSetParser |  |
| emitSamplesToDataSetFileDir | void |  |
| parseSamplesToDataSetFile | String |  |
| parseFilesToSamples | List<ImageDataSetSampleMysqlModel> |  |
| createSampleModel | ImageDataSetSampleMysqlModel |  |




