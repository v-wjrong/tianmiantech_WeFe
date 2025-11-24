# Basic Information

|      |      |
|------|------|
| Name | BloomFilterAddServiceDataRowConsumer |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/bloomfilter/BloomFilterAddServiceDataRowConsumer.java |
| Package Name | com.welab.wefe.data.fusion.service.service.bloomfilter |
| Dependencies | ['java.io.File', 'java.io.FileOutputStream', 'java.io.IOException', 'java.math.BigInteger', 'java.util.List', 'java.util.Map', 'java.util.concurrent.CopyOnWriteArrayList', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'java.util.concurrent.atomic.AtomicInteger', 'java.util.function.Consumer', 'org.bouncycastle.crypto.AsymmetricCipherKeyPair', 'org.bouncycastle.crypto.params.RSAKeyParameters', 'org.bouncycastle.crypto.params.RSAPrivateCrtKeyParameters', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'com.welab.wefe.common.BatchConsumer', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.database.entity.BloomFilterMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.BloomFilterRepository', 'com.welab.wefe.data.fusion.service.enums.Progress', 'com.welab.wefe.data.fusion.service.service.FieldInfoService', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters', 'com.welab.wefe.data.fusion.service.utils.primarykey.FieldInfo', 'com.welab.wefe.data.fusion.service.utils.primarykey.PrimaryKeyUtils', 'com.welab.wefe.fusion.core.utils.CryptoUtils', 'com.welab.wefe.fusion.core.utils.PSIUtils'] |
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
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| N | BigInteger |  |
| bloomFilterRepository | BloomFilterRepository |  |
| bf | BloomFilters<BigInteger> |  |
| CheckData = new CopyOnWriteArrayList<>() | List<Object> |  |
| e | BigInteger |  |
| pk | RSAKeyParameters |  |
| batchConsumer | BatchConsumer<Map<String, Object>> |  |
| model | BloomFilterMySqlModel |  |
| src | String |  |
| processCount = 0 | Integer |  |
| d | BigInteger |  |
| keyPair | AsymmetricCipherKeyPair |  |
| process | Progress |  |
| fieldInfoList | List<FieldInfo> |  |
| sk | RSAPrivateCrtKeyParameters |  |
| checkCount = new AtomicInteger(0) | AtomicInteger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setD | void |  |
| getD | BigInteger |  |
| generateFilter | void |  |
| setProcess | void |  |
| waitForFinishAndClose | void |  |
| setProcessCount | void |  |
| getE | BigInteger |  |
| getModel | BloomFilterMySqlModel |  |
| setBf | void |  |
| accept | void |  |
| getProcessCount | Integer |  |
| getCheckData | List<Object> |  |
| getN | BigInteger |  |
| getProcess | Progress |  |
| generateFilterSlown | void |  |
| setN | void |  |
| setE | void |  |
| getBf | BloomFilters<BigInteger> |  |
| getCheckCount | AtomicInteger |  |
| setCheckCount | void |  |
| setCheckData | void |  |
| addToBf | void |  |




