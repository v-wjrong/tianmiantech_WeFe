# Basic Information

|      |      |
|------|------|
| Name | DataSetColumnMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_set/DataSetColumnMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.data_set |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSetColumnMysqlModel | class |  |



## Class DataSetColumnMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "data_set_column");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | DataSetColumnMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| index | Integer |  |
| dataSetId | String |  |
| dataType | ColumnDataType |  |
| comment | String |  |
| valueDistribution | JSONObject |  |
| emptyRows | Long |  |
| name | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getIndex | Integer |  |
| setDataSetId | void |  |
| setEmptyRows | void |  |
| setComment | void |  |
| getEmptyRows | Long |  |
| setName | void |  |
| getComment | String |  |
| getDataType | ColumnDataType |  |
| setIndex | void |  |
| getName | String |  |
| getDataSetId | String |  |
| setDataType | void |  |
| getValueDistribution | JSONObject |  |
| setValueDistribution | void |  |




