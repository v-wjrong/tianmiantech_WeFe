# 基础信息

|      |      |
|------|------|
| 名称 | TableDataSetAddInputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/vo/data_resource/TableDataSetAddInputModel.java |
| 包名 | com.welab.wefe.board.service.dto.vo.data_resource |
| 依赖项 | ['com.welab.wefe.board.service.base.file_system.WeFeFileSystem', 'com.welab.wefe.board.service.constant.DataSetAddMethod', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'org.apache.commons.lang3.StringUtils'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TableDataSetAddInputModel | class |  |



## 类 TableDataSetAddInputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TableDataSetAddInputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sql | String |  |
| dataSourceId | String |  |
| dataSetAddMethod | DataSetAddMethod |  |
| filename | String |  |
| deduplication | boolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataSourceId | String |  |
| setDataSourceId | void |  |
| setSql | void |  |
| setDeduplication | void |  |
| checkAndStandardize | void |  |
| setDataSetAddMethod | void |  |
| getDataSetAddMethod | DataSetAddMethod |  |
| getSql | String |  |
| isDeduplication | boolean |  |
| getFilename | String |  |
| setFilename | void |  |




