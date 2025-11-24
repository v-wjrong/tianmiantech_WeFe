# 基础信息

|      |      |
|------|------|
| 名称 | ImageDataSetMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/ImageDataSetMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.data_resource |
| 依赖项 | ['com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'javax.persistence.Table', 'java.util.List', 'java.util.TreeSet'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ImageDataSetMysqlModel | class |  |



## 类 ImageDataSetMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "image_data_set");@Table(name = "image_data_set");public |
| 类型 | class |
| 名称 | ImageDataSetMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| labelCompleted | boolean |  |
| labeledCount | Long |  |
| forJobType | DeepLearningJobType |  |
| labelList | String |  |
| filesSize | Long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| isLabelCompleted | boolean |  |
| setLabelCompleted | void |  |
| getLabelSet | TreeSet<String> |  |
| getForJobType | DeepLearningJobType |  |
| setForJobType | void |  |
| setLabeledCount | void |  |
| getLabeledCount | Long |  |
| setLabelList | void |  |
| getLabelList | String |  |
| getFilesSize | Long |  |
| setFilesSize | void |  |




