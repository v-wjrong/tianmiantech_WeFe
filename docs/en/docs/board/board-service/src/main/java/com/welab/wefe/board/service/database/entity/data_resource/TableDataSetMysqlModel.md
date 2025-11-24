# Basic Information

|      |      |
|------|------|
| Name | TableDataSetMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/TableDataSetMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.data_resource |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.dto.vo.data_set.table_data_set.LabelDistribution', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.hibernate.annotations.Type', 'org.hibernate.annotations.TypeDef', 'javax.persistence.Column', 'javax.persistence.Entity', 'javax.persistence.Table'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TableDataSetMysqlModel | class |  |



## Class TableDataSetMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "table_data_set");@Table(name = "table_data_set");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | TableDataSetMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




