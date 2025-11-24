# Basic Information

|      |      |
|------|------|
| Name | TencentCosStorage |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/fc/tencent/TencentCosStorage.java |
| Package Name | com.welab.wefe.common.data.storage.service.fc.tencent |
| Dependencies | ['com.google.protobuf.ByteString', 'com.qcloud.cos.COSClient', 'com.qcloud.cos.ClientConfig', 'com.qcloud.cos.auth.BasicCOSCredentials', 'com.qcloud.cos.auth.COSCredentials', 'com.qcloud.cos.http.HttpProtocol', 'com.qcloud.cos.model.ObjectMetadata', 'com.qcloud.cos.model.PutObjectRequest', 'com.qcloud.cos.region.Region', 'com.welab.wefe.common.data.storage.common.IntermediateDataFlag', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.service.fc.FcStorage', 'com.welab.wefe.common.proto.IntermediateDataOuterClass', 'net.razorvine.pickle.Pickler', 'org.apache.commons.codec.digest.DigestUtils', 'org.apache.commons.lang.ArrayUtils', 'java.io.ByteArrayInputStream', 'java.math.BigDecimal', 'java.math.BigInteger', 'java.nio.charset.StandardCharsets', 'java.security.MessageDigest', 'java.util', 'java.util.concurrent'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TencentCosStorage | class |  |



## Class TencentCosStorage

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | TencentCosStorage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| config | TencentCosConfig |  |
| SPLIT_EACH_SIZE = 1024 * 1024 | int |  |
| OBJECT_FILE_MAX_SIZE = 1024 * 1024 * 4 | int |  |
| OBJECT_MIN_DATA_COUNT = 500 | int |  |
| OBJECT_MAX_DATA_COUNT = 1000 | int |  |
| SPLIT_MAX_FREFIX = "MAX_" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| putAll | void |  |
| cosPutAll | void |  |
| cosPutAll | void |  |
| getCosFileName | String |  |
| toKeyValueByte | byte[] |  |
| hashKeyToPartition | int |  |
| byteArrayToInt | BigInteger |  |




