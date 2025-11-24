# Basic Information

|      |      |
|------|------|
| Name | AbstractBlockChainBusinessModel |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/base/AbstractBlockChainBusinessModel.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.base |
| Dependencies | ['java.util.Date', 'com.welab.wefe.common.util.DateUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractBlockChainBusinessModel | class |  |



## Class AbstractBlockChainBusinessModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AbstractBlockChainBusinessModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| updatedTime = DateUtil.toStringYYYY_MM_DD_HH_MM_SS2(new Date()) | String |  |
| status | int |  |
| createdTime = DateUtil.toStringYYYY_MM_DD_HH_MM_SS2(new Date()) | String |  |
| dataSyncTime = System.currentTimeMillis() | long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setDataSyncTime | void |  |
| setCreatedTime | void |  |
| getUpdatedTime | String |  |
| setUpdatedTime | void |  |
| getCreatedTime | String |  |
| setStatus | void |  |
| getStatus | int |  |
| getDataSyncTime | long |  |




