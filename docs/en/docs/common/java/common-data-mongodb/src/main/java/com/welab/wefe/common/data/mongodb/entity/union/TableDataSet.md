# Basic Information

|      |      |
|------|------|
| Name | TableDataSet |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/TableDataSet.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceExtJSON', 'com.welab.wefe.common.data.mongodb.entity.union.ext.TableDataSetExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TableDataSet | class |  |



## Class TableDataSet

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.TABLE_DATASET);public |
| Type | class |
| Name | TableDataSet |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| containsY | String |  |
| dataResourceId | String |  |
| columnCount | String |  |
| extJson = new TableDataSetExtJSON() | TableDataSetExtJSON |  |
| columnNameList | String |  |
| featureCount | String |  |
| featureNameList | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setFeatureCount | void |  |
| getFeatureCount | String |  |
| setContainsY | void |  |
| getExtJson | TableDataSetExtJSON |  |
| getContainsY | String |  |
| getFeatureNameList | String |  |
| getColumnCount | String |  |
| setColumnNameList | void |  |
| setDataResourceId | void |  |
| setFeatureNameList | void |  |
| getColumnNameList | String |  |
| setColumnCount | void |  |
| getDataResourceId | String |  |
| setExtJson | void |  |




