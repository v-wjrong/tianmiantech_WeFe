# 基础信息

|      |      |
|------|------|
| 名称 | MemberContractService |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/contract/MemberContractService.java |
| 包名 | com.welab.wefe.union.service.service.contract |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberMongoReop', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.union.service.api.member.UpdateExcludeLogoApi', 'com.welab.wefe.union.service.contract.MemberContract', 'com.welab.wefe.union.service.entity.Member', 'org.apache.commons.collections4.CollectionUtils', 'org.fisco.bcos.sdk.abi.datatypes.generated.tuples.generated.Tuple2', 'org.fisco.bcos.sdk.crypto.CryptoSuite', 'org.fisco.bcos.sdk.model.TransactionReceipt', 'org.fisco.bcos.sdk.transaction.codec.decode.TransactionDecoderService', 'org.fisco.bcos.sdk.transaction.model.dto.TransactionResponse', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.lang.reflect.Field', 'java.math.BigInteger', 'java.util.ArrayList', 'java.util.Date', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberContractService | class |  |



## 类 MemberContractService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | MemberContractService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| memberMongoReop | MemberMongoReop |  |
| cryptoSuite | CryptoSuite |  |
| LOG = LoggerFactory.getLogger(MemberContractService.class) | Logger |  |
| memberContract | MemberContract |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| updateLastActivityTimeById | void |  |
| updateLogoById | void |  |
| queryAll | List<Member> |  |
| isExist | boolean |  |
| upsert | void |  |
| dataStrListToMember | List<Member> |  |
| updateExcludeLogo | void |  |
| add | void |  |
| buildExtJson | JObject |  |
| updatePublicKey | void |  |
| dataStrToMember | Member |  |
| generateParams | List<String> |  |
| updateExtJson | void |  |




