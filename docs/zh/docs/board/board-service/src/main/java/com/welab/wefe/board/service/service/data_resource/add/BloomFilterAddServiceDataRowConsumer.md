# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilterAddServiceDataRowConsumer |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/add/BloomFilterAddServiceDataRowConsumer.java |
| 包名 | com.welab.wefe.board.service.service.data_resource.add |
| 依赖项 | ['com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.data_resource.BloomFilterMysqlModel', 'com.welab.wefe.board.service.service.data_resource.DataResourceUploadTaskService', 'com.welab.wefe.board.service.service.data_resource.bloom_filter.BloomFilterStorageService', 'com.welab.wefe.board.service.service.fusion.FieldInfoService', 'com.welab.wefe.board.service.util.AbstractBloomFilterReader', 'com.welab.wefe.board.service.util.primarykey.FieldInfo', 'com.welab.wefe.board.service.util.primarykey.PrimaryKeyUtils', 'com.welab.wefe.board.service.util.unique.AbstractDataSetUniqueFilter', 'com.welab.wefe.board.service.util.unique.DataSetBloomUniqueFilter', 'com.welab.wefe.board.service.util.unique.DataSetMemoryUniqueFilter', 'com.welab.wefe.common.BatchConsumer', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.fusion.core.utils.CryptoUtils', 'com.welab.wefe.fusion.core.utils.PSIUtils', 'com.welab.wefe.fusion.core.utils.bf.BloomFilters', 'org.bouncycastle.crypto.AsymmetricCipherKeyPair', 'org.bouncycastle.crypto.params.RSAKeyParameters', 'org.bouncycastle.crypto.params.RSAPrivateCrtKeyParameters', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.io.FileOutputStream', 'java.io.IOException', 'java.math.BigInteger', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilterAddServiceDataRowConsumer | class |  |



## 类 BloomFilterAddServiceDataRowConsumer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BloomFilterAddServiceDataRowConsumer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| bloomfilterReader | AbstractBloomFilterReader |  |
| deduplication | boolean |  |
| cp | BigInteger |  |
| rsaD | BigInteger |  |
| rsaN | BigInteger |  |
| config | Config |  |
| LOG = LoggerFactory.getLogger(BloomFilterAddServiceDataRowConsumer.class) | Logger |  |
| keyPair | AsymmetricCipherKeyPair |  |
| bloomfilterStorageService | BloomFilterStorageService |  |
| bloomfilterId | String |  |
| processCount = 0 | Integer |  |
| repeatDataCount = new LongAdder() | LongAdder |  |
| rsaP | BigInteger |  |
| fieldInfoList | List<FieldInfo> |  |
| totalDataCount = 0 | Integer |  |
| uniqueFilter | AbstractDataSetUniqueFilter |  |
| maxBatchSize = 0 | int |  |
| rsaSK | RSAPrivateCrtKeyParameters |  |
| rsaE | BigInteger |  |
| dataResourceUploadTaskService | DataResourceUploadTaskService |  |
| cq | BigInteger |  |
| rsaQ | BigInteger |  |
| rsaPK | RSAKeyParameters |  |
| bf | BloomFilters |  |
| batchConsumer | BatchConsumer<LinkedHashMap<String, Object>> |  |
| bloomfilterPath | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| generateFilter | void |  |
| accept | void |  |
| waitForFinishAndClose | void |  |
| getRepeatDataCount | long |  |
| saveRowWithDeduplication | void |  |
| createUniqueFilter | AbstractDataSetUniqueFilter |  |




