# 基础信息

|      |      |
|------|------|
| 名称 | BlockInfoParser |
| 编码语言 | .java |
| 代码路径 | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/BlockInfoParser.java |
| 包名 | com.welab.wefe.parser |
| 依赖项 | ['com.welab.wefe.bo.contract.ContractInfo', 'com.welab.wefe.bo.contract.EventMetaInfo', 'com.welab.wefe.bo.contract.FieldInfo', 'com.welab.wefe.bo.data.BlockInfoBO', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.bo.data.TransactionResponseBO', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.constant.ContractConstants', 'com.welab.wefe.constant.SyncConstant', 'com.welab.wefe.util.TransactionUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.fisco.bcos.sdk.abi.ABICodecException', 'org.fisco.bcos.sdk.client.protocol.model.JsonTransactionResponse', 'org.fisco.bcos.sdk.client.protocol.response.BcosBlock', 'org.fisco.bcos.sdk.client.protocol.response.BcosTransactionReceipt', 'org.fisco.bcos.sdk.model.TransactionReceipt', 'org.fisco.bcos.sdk.transaction.codec.decode.TransactionDecoderInterface', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.fisco.bcos.sdk.transaction.model.exception.ContractException', 'org.fisco.bcos.sdk.utils.Numeric', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BlockInfoParser | class |  |



## 类 BlockInfoParser

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BlockInfoParser |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| block | BcosBlock.Block |  |
| LOG = LoggerFactory.getLogger(BlockInfoParser.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| parse | BlockInfoBO |  |
| create | BlockInfoParser |  |
| parserEvent | List<EventBO> |  |
| parseTransactionResponse | void |  |




