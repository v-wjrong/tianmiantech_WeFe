# 基础信息

|      |      |
|------|------|
| 名称 | AbstractBlockChainBusinessModel |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/base/AbstractBlockChainBusinessModel.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.base |
| 依赖项 | ['java.util.Date', 'com.welab.wefe.common.util.DateUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractBlockChainBusinessModel | class |  |



## 类 AbstractBlockChainBusinessModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AbstractBlockChainBusinessModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| updatedTime = DateUtil.toStringYYYY_MM_DD_HH_MM_SS2(new Date()) | String |  |
| status | int |  |
| createdTime = DateUtil.toStringYYYY_MM_DD_HH_MM_SS2(new Date()) | String |  |
| dataSyncTime = System.currentTimeMillis() | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setDataSyncTime | void |  |
| setCreatedTime | void |  |
| getUpdatedTime | String |  |
| setUpdatedTime | void |  |
| getCreatedTime | String |  |
| setStatus | void |  |
| getStatus | int |  |
| getDataSyncTime | long |  |




