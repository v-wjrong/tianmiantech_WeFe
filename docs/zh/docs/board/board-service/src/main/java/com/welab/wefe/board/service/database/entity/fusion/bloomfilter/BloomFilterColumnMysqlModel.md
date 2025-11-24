# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilterColumnMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/fusion/bloomfilter/BloomFilterColumnMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.fusion.bloomfilter |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.EnumType', 'javax.persistence.Enumerated'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilterColumnMysqlModel | class |  |



## 类 BloomFilterColumnMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "bloom_filter_column");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | BloomFilterColumnMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataType | ColumnDataType |  |
| bloomFilterId | String |  |
| comment | String |  |
| name | String |  |
| valueDistribution | JSONObject |  |
| emptyRows | Long |  |
| index | Integer |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




