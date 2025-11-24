# Basic Information

|      |      |
|------|------|
| Name | AliyunOssStorage |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/fc/aliyun/AliyunOssStorage.java |
| Package Name | com.welab.wefe.common.data.storage.service.fc.aliyun |
| Dependencies | ['com.alicloud.openservices.tablestore', 'com.alicloud.openservices.tablestore.model', 'com.alicloud.openservices.tablestore.writer.WriterConfig', 'com.aliyun.oss.ClientBuilderConfiguration', 'com.aliyun.oss.OSS', 'com.aliyun.oss.OSSClientBuilder', 'com.google.protobuf.ByteString', 'com.welab.wefe.common.data.storage.common.IntermediateDataFlag', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.service.fc.FcStorage', 'com.welab.wefe.common.proto.IntermediateDataOuterClass', 'net.razorvine.pickle.Pickler', 'org.apache.commons.codec.digest.DigestUtils', 'org.apache.commons.lang.ArrayUtils', 'java.io.ByteArrayInputStream', 'java.io.IOException', 'java.math.BigDecimal', 'java.math.BigInteger', 'java.nio.charset.StandardCharsets', 'java.security.MessageDigest', 'java.util', 'java.util.concurrent', 'java.util.concurrent.atomic.AtomicLong'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AliyunOssStorage | class |  |



## Class AliyunOssStorage

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AliyunOssStorage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| SPLIT_MAX_FREFIX = "MAX_" | String |  |
| OBJECT_MIN_DATA_COUNT = 500 | int |  |
| OBJECT_MAX_DATA_COUNT = 1000 | int |  |
| SPLIT_EACH_SIZE = 1024 * 1024 | int |  |
| config | AliyunOssConfig |  |
| OBJECT_FILE_MAX_SIZE = 1024 * 1024 * 4 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getOssFileName | String |  |
| otsPutAll | void |  |
| otsPutAll | void |  |
| putAll | void |  |
| ossPutAll | void |  |
| ossPutAll | void |  |
| splitValue | List<byte[]> |  |
| toKeyValueByte | byte[] |  |
| hashKeyToPartition | int |  |
| byteArrayToInt | BigInteger |  |




