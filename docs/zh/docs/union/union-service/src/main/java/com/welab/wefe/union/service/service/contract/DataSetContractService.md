# 基础信息

|      |      |
|------|------|
| 名称 | DataSetContractService |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/contract/DataSetContractService.java |
| 包名 | com.welab.wefe.union.service.service.contract |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractMongoModel', 'com.welab.wefe.common.data.mongodb.entity.union.DataResourceLazyUpdateModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataSetExtJSON', 'com.welab.wefe.common.data.mongodb.repo', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.union.service.api.dataresource.LazyUpdateApi', 'com.welab.wefe.union.service.contract.DataSetContract', 'com.welab.wefe.union.service.entity.DataSet', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.fisco.bcos.sdk.model.TransactionReceipt', 'org.fisco.bcos.sdk.transaction.codec.decode.TransactionDecoderService', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetContractService | class |  |



## 类 DataSetContractService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | DataSetContractService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| imageDataSetMongoReop | ImageDataSetMongoReop |  |
| bloomFilterMongoReop | BloomFilterMongoReop |  |
| cryptoSuite | CryptoSuite |  |
| dataSetContract | DataSetContract |  |
| dataResourceLazyUpdateModelMongoReop | DataResourceLazyUpdateModelMongoReop |  |
| tableDataSetMongoReop | TableDataSetMongoReop |  |
| memberContractService | MemberContractService |  |
| dataSetMongoReop | DataSetMongoReop |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| upsert | void |  |
| deleteById | void |  |
| lazyUpdate | void |  |
| generateParams | List<String> |  |




