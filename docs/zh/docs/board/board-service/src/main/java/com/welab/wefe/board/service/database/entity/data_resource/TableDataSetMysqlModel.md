# 基础信息

|      |      |
|------|------|
| 名称 | TableDataSetMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/TableDataSetMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.data_resource |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.dto.vo.data_set.table_data_set.LabelDistribution', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.Table'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TableDataSetMysqlModel | class |  |



## 类 TableDataSetMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "table_data_set");@Table(name = "table_data_set");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | TableDataSetMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| featureCount | Integer |  |
| yPositiveSampleCount | Long |  |
| yCount | Integer |  |
| featureNameList | String |  |
| columnCount | Integer |  |
| columnNameList | String |  |
| labelDistribution | JSONObject |  |
| primaryKeyColumn | String |  |
| positiveSampleValue | String |  |
| containsY | boolean |  |
| yNameList | String |  |
| yPositiveSampleRatio | Double |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFeatureNameList | String |  |
| setyPositiveSampleCount | void |  |
| setPositiveSampleValue | void |  |
| getFeatureCount | Integer |  |
| getPositiveSampleValue | String |  |
| getColumnNameList | String |  |
| setColumnCount | void |  |
| setContainsY | void |  |
| setLabelDistribution | void |  |
| getyNameList | String |  |
| setFeatureCount | void |  |
| setPrimaryKeyColumn | void |  |
| setyCount | void |  |
| getyPositiveSampleRatio | Double |  |
| isContainsY | boolean |  |
| getColumnCount | Integer |  |
| setColumnNameList | void |  |
| getyCount | Integer |  |
| getLabelDistribution | JSONObject |  |
| setFeatureNameList | void |  |
| setyNameList | void |  |
| getPrimaryKeyColumn | String |  |
| getyPositiveSampleCount | Long |  |
| setyPositiveSampleRatio | void |  |
| setLabelDistribution | void |  |




