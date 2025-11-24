# 基础信息

|      |      |
|------|------|
| 名称 | AliyunOssStorage |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/fc/aliyun/AliyunOssStorage.java |
| 包名 | com.welab.wefe.common.data.storage.service.fc.aliyun |
| 依赖项 | ['com.alicloud.openservices.tablestore', 'com.alicloud.openservices.tablestore.model', 'com.alicloud.openservices.tablestore.writer.WriterConfig', 'com.aliyun.oss.ClientBuilderConfiguration', 'com.aliyun.oss.OSS', 'com.aliyun.oss.OSSClientBuilder', 'com.google.protobuf.ByteString', 'com.welab.wefe.common.data.storage.common.IntermediateDataFlag', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.service.fc.FcStorage', 'com.welab.wefe.common.proto.IntermediateDataOuterClass', 'net.razorvine.pickle.Pickler', 'org.apache.commons.codec.digest.DigestUtils', 'org.apache.commons.lang.ArrayUtils', 'java.io.ByteArrayInputStream', 'java.io.IOException', 'java.math.BigDecimal', 'java.math.BigInteger', 'java.nio.charset.StandardCharsets', 'java.security.MessageDigest', 'java.util', 'java.util.concurrent', 'java.util.concurrent.atomic.AtomicLong'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AliyunOssStorage | class |  |



## 类 AliyunOssStorage

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AliyunOssStorage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| SPLIT_MAX_FREFIX = "MAX_" | String |  |
| OBJECT_MIN_DATA_COUNT = 500 | int |  |
| OBJECT_MAX_DATA_COUNT = 1000 | int |  |
| SPLIT_EACH_SIZE = 1024 * 1024 | int |  |
| config | AliyunOssConfig |  |
| OBJECT_FILE_MAX_SIZE = 1024 * 1024 * 4 | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




