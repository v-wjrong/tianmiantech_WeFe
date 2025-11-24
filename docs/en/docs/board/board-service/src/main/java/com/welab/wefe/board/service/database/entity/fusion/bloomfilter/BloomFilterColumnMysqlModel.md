# Basic Information

|      |      |
|------|------|
| Name | BloomFilterColumnMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/fusion/bloomfilter/BloomFilterColumnMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.fusion.bloomfilter |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilterColumnMysqlModel | class |  |



## Class BloomFilterColumnMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "bloom_filter_column");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | BloomFilterColumnMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataType | ColumnDataType |  |
| bloomFilterId | String |  |
| comment | String |  |
| name | String |  |
| valueDistribution | JSONObject |  |
| emptyRows | Long |  |
| index | Integer |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setBloomFilterId | void |  |
| setIndex | void |  |
| getValueDistribution | JSONObject |  |
| getEmptyRows | Long |  |
| getComment | String |  |
| setComment | void |  |
| getName | String |  |
| getDataType | ColumnDataType |  |
| setDataType | void |  |
| getBloomFilterId | String |  |
| getIndex | Integer |  |
| setName | void |  |
| setEmptyRows | void |  |
| setValueDistribution | void |  |




