# 基础信息

|      |      |
|------|------|
| 名称 | TencentCosStorage |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/fc/tencent/TencentCosStorage.java |
| 包名 | com.welab.wefe.common.data.storage.service.fc.tencent |
| 依赖项 | ['com.google.protobuf.ByteString', 'com.qcloud.cos.COSClient', 'com.qcloud.cos.ClientConfig', 'com.qcloud.cos.auth.BasicCOSCredentials', 'com.qcloud.cos.auth.COSCredentials', 'com.qcloud.cos.http.HttpProtocol', 'com.qcloud.cos.model.ObjectMetadata', 'com.qcloud.cos.model.PutObjectRequest', 'com.qcloud.cos.region.Region', 'com.welab.wefe.common.data.storage.common.IntermediateDataFlag', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.service.fc.FcStorage', 'com.welab.wefe.common.proto.IntermediateDataOuterClass', 'net.razorvine.pickle.Pickler', 'org.apache.commons.codec.digest.DigestUtils', 'org.apache.commons.lang.ArrayUtils', 'java.io.ByteArrayInputStream', 'java.math.BigDecimal', 'java.math.BigInteger', 'java.nio.charset.StandardCharsets', 'java.security.MessageDigest', 'java.util', 'java.util.concurrent'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TencentCosStorage | class |  |



## 类 TencentCosStorage

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TencentCosStorage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| config | TencentCosConfig |  |
| SPLIT_EACH_SIZE = 1024 * 1024 | int |  |
| OBJECT_FILE_MAX_SIZE = 1024 * 1024 * 4 | int |  |
| OBJECT_MIN_DATA_COUNT = 500 | int |  |
| OBJECT_MAX_DATA_COUNT = 1000 | int |  |
| SPLIT_MAX_FREFIX = "MAX_" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| putAll | void |  |
| cosPutAll | void |  |
| cosPutAll | void |  |
| getCosFileName | String |  |
| toKeyValueByte | byte[] |  |
| hashKeyToPartition | int |  |
| byteArrayToInt | BigInteger |  |




