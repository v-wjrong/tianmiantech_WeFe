# 基础信息

|      |      |
|------|------|
| 名称 | DataSetContractEventParser |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/DataSetContractEventParser.java |
| 包名 | com.welab.wefe.parser |
| 依赖项 | ['org.apache.commons.lang3.StringUtils', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.BlockchainDataSyncApp', 'com.welab.wefe.common.data.mongodb.entity.union.DataSet', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataSetExtJSON', 'com.welab.wefe.common.data.mongodb.repo.DataSetMongoReop', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetContractEventParser | class |  |



## 类 DataSetContractEventParser

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DataSetContractEventParser |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataSetMongoReop = BlockchainDataSyncApp.CONTEXT.getBean(DataSetMongoReop.class) | DataSetMongoReop |  |
| extJSON | DataSetExtJSON |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| parseDeleteByDataSetIdEvent | void |  |
| parseUpdateExtJson | void |  |
| parseContractEvent | void |  |
| parseInsertAndUpdateEvent | void |  |




