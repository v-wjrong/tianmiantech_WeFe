# 基础信息

|      |      |
|------|------|
| 名称 | ImageDataSetOutputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/data_resource/output/ImageDataSetOutputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.data_resource.output |
| 依赖项 | ['com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'java.util.List', 'java.util.TreeSet'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ImageDataSetOutputModel | class |  |



## 类 ImageDataSetOutputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ImageDataSetOutputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| labeledCount | Long |  |
| forJobType | DeepLearningJobType |  |
| labelCompleted | boolean |  |
| labelList | String |  |
| filesSize | Long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setForJobType | void |  |
| getForJobType | DeepLearningJobType |  |
| setLabelCompleted | void |  |
| setLabeledCount | void |  |
| setLabelList | void |  |
| getLabelList | String |  |
| isLabelCompleted | boolean |  |
| getLabelSet | TreeSet<String> |  |
| getLabeledCount | Long |  |
| getFilesSize | Long |  |
| setFilesSize | void |  |




