# 基础信息

|      |      |
|------|------|
| 名称 | ImageDataSetSampleMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_set/ImageDataSetSampleMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.data_set |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.annotation.JSONField', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.util.StringUtil', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'java.util.List', 'java.util.TreeSet'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ImageDataSetSampleMysqlModel | class |  |



## 类 ImageDataSetSampleMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "image_data_set_sample");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | ImageDataSetSampleMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| filePath | String |  |
| fileName | String |  |
| dataSetId | String |  |
| xmlAnnotation | String |  |
| labeled | boolean |  |
| fileSize | long |  |
| labelInfo | JSONObject |  |
| labelList | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFileName | String |  |
| getFileSize | long |  |
| setFileSize | void |  |
| getDataSetId | String |  |
| getLabelSet | TreeSet<String> |  |
| setFileName | void |  |
| isLabeled | boolean |  |
| setLabelList | void |  |
| getLabelList | String |  |
| setLabeled | void |  |
| getLabelInfo | JSONObject |  |
| setLabelInfo | void |  |
| getXmlAnnotation | String |  |
| setXmlAnnotation | void |  |
| setFilePath | void |  |
| setDataSetId | void |  |
| getFilePath | String |  |




