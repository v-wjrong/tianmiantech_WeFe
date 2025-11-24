# Basic Information

|      |      |
|------|------|
| Name | DetectionImageDataSetParser |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/image_data_set/data_set_parser/DetectionImageDataSetParser.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.image_data_set.data_set_parser |
| Dependencies | ['com.thoughtworks.xstream.io.StreamException', 'com.welab.wefe.board.service.database.entity.data_resource.ImageDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.data_set.ImageDataSetSampleMysqlModel', 'com.welab.wefe.board.service.dto.vo.data_set.image_data_set.Annotation', 'com.welab.wefe.board.service.dto.vo.data_set.image_data_set.LabelInfo', 'com.welab.wefe.board.service.dto.vo.data_set.image_data_set.Size', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util', 'org.apache.commons.collections4.CollectionUtils', 'javax.imageio.ImageIO', 'java.awt.image.BufferedImage', 'java.io.File', 'java.io.FileInputStream', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.util.ArrayList', 'java.util.Collections', 'java.util.List', 'java.util.Map', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DetectionImageDataSetParser | class |  |



## Class DetectionImageDataSetParser

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | DetectionImageDataSetParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LABEL_LIST_FILE_NAME = "label_list.txt" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| buildAnnotation | Annotation |  |
| parseFilesToSamples | List<ImageDataSetSampleMysqlModel> |  |
| createSample | ImageDataSetSampleMysqlModel |  |
| emitTranValFile | void |  |
| emitSamplesToDataSetFileDir | void |  |
| emitImageFile | void |  |
| emitLabelListFile | void |  |
| emitAnnotationFile | void |  |




