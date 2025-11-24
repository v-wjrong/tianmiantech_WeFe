# 基础信息

|      |      |
|------|------|
| 名称 | DataSetColumnMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_set/DataSetColumnMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.data_set |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetColumnMysqlModel | class |  |



## 类 DataSetColumnMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "data_set_column");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | DataSetColumnMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| index | Integer |  |
| dataSetId | String |  |
| dataType | ColumnDataType |  |
| comment | String |  |
| valueDistribution | JSONObject |  |
| emptyRows | Long |  |
| name | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




