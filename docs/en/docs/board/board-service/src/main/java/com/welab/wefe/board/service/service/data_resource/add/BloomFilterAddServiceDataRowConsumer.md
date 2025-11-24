# Basic Information

|      |      |
|------|------|
| Name | BloomFilterAddServiceDataRowConsumer |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/add/BloomFilterAddServiceDataRowConsumer.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.add |
| Dependencies | ['com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.data_resource.BloomFilterMysqlModel', 'com.welab.wefe.board.service.service.data_resource.DataResourceUploadTaskService', 'com.welab.wefe.board.service.service.data_resource.bloom_filter.BloomFilterStorageService', 'com.welab.wefe.board.service.service.fusion.FieldInfoService', 'com.welab.wefe.board.service.util.AbstractBloomFilterReader', 'com.welab.wefe.board.service.util.primarykey.FieldInfo', 'com.welab.wefe.board.service.util.primarykey.PrimaryKeyUtils', 'com.welab.wefe.board.service.util.unique.AbstractDataSetUniqueFilter', 'com.welab.wefe.board.service.util.unique.DataSetBloomUniqueFilter', 'com.welab.wefe.board.service.util.unique.DataSetMemoryUniqueFilter', 'com.welab.wefe.common.BatchConsumer', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.fusion.core.utils.CryptoUtils', 'com.welab.wefe.fusion.core.utils.PSIUtils', 'com.welab.wefe.fusion.core.utils.bf.BloomFilters', 'org.bouncycastle.crypto.AsymmetricCipherKeyPair', 'org.bouncycastle.crypto.params.RSAKeyParameters', 'org.bouncycastle.crypto.params.RSAPrivateCrtKeyParameters', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.io.FileOutputStream', 'java.io.IOException', 'java.math.BigInteger', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilterAddServiceDataRowConsumer | class |  |



## Class BloomFilterAddServiceDataRowConsumer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BloomFilterAddServiceDataRowConsumer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateFilter | void |  |
| accept | void |  |
| waitForFinishAndClose | void |  |
| getRepeatDataCount | long |  |
| saveRowWithDeduplication | void |  |
| createUniqueFilter | AbstractDataSetUniqueFilter |  |




