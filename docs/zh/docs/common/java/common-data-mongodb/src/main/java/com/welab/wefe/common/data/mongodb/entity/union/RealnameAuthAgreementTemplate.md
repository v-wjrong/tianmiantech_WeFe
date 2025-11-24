# 基础信息

|      |      |
|------|------|
| 名称 | RealnameAuthAgreementTemplate |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/RealnameAuthAgreementTemplate.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.RealnameAuthAgreementTemplateExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| RealnameAuthAgreementTemplate | class |  |



## 类 RealnameAuthAgreementTemplate

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.REALNAME_AUTH_AGREEMENT_TEMPLATE);public |
| 类型 | class |
| 名称 | RealnameAuthAgreementTemplate |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| blockchainNodeId | String |  |
| templateFileId | String |  |
| fileName | String |  |
| version | String |  |
| enable = "0" | String |  |
| extJson = new RealnameAuthAgreementTemplateExtJSON() | RealnameAuthAgreementTemplateExtJSON |  |
| templateFileSign | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setBlockchainNodeId | void |  |
| setExtJson | void |  |
| getEnable | String |  |
| getBlockchainNodeId | String |  |
| setFileName | void |  |
| setTemplateFileId | void |  |
| getFileName | String |  |
| setVersion | void |  |
| getTemplateFileId | String |  |
| setTemplateFileSign | void |  |
| getTemplateFileSign | String |  |
| getVersion | String |  |
| getExtJson | RealnameAuthAgreementTemplateExtJSON |  |
| setEnable | void |  |




