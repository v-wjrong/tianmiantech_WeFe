# 基础信息

|      |      |
|------|------|
| 名称 | BlockUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/util/BlockUtil.java |
| 包名 | com.welab.wefe.util |
| 依赖项 | ['cn.hutool.core.collection.CollectionUtil', 'cn.hutool.core.util.StrUtil', 'com.welab.wefe.bo.contract.EventMetaInfo', 'com.welab.wefe.bo.contract.FieldInfo', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.enums.JavaTypeEnum', 'org.apache.commons.lang3.StringUtils', 'org.fisco.bcos.sdk.abi.wrapper.ABIDefinition', 'org.fisco.bcos.sdk.client.Client', 'org.fisco.bcos.sdk.client.protocol.response.BcosBlock', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.math.BigInteger', 'java.util.ArrayList', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BlockUtil | class |  |



## 类 BlockUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BlockUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(BlockUtil.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setSqlAttribute | FieldInfo |  |
| getBlock | BcosBlock.Block |  |
| parseToEventMetaInfoList | List<EventMetaInfo> |  |




