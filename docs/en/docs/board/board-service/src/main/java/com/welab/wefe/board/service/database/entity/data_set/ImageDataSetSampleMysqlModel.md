# Basic Information

|      |      |
|------|------|
| Name | ImageDataSetSampleMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_set/ImageDataSetSampleMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.data_set |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.annotation.JSONField', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.util.StringUtil', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'java.util.List', 'java.util.TreeSet'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ImageDataSetSampleMysqlModel | class |  |



## Class ImageDataSetSampleMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "image_data_set_sample");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | ImageDataSetSampleMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| filePath | String |  |
| fileName | String |  |
| dataSetId | String |  |
| xmlAnnotation | String |  |
| labeled | boolean |  |
| fileSize | long |  |
| labelInfo | JSONObject |  |
| labelList | String |  |

### Method List

| Name  | Type  | Description |
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




