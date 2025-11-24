# Basic Information

|      |      |
|------|------|
| Name | RealnameAuthAgreementTemplate |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/RealnameAuthAgreementTemplate.java |
| Package Name | com.welab.wefe.common.data.mongodb.entity.union |
| Dependencies | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.RealnameAuthAgreementTemplateExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RealnameAuthAgreementTemplate | class |  |



## Class RealnameAuthAgreementTemplate

|      |      |
|------|------|
| Access Modifier | @Document(collection = MongodbTable.Union.REALNAME_AUTH_AGREEMENT_TEMPLATE);public |
| Type | class |
| Name | RealnameAuthAgreementTemplate |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| blockchainNodeId | String |  |
| templateFileId | String |  |
| fileName | String |  |
| version | String |  |
| enable = "0" | String |  |
| extJson = new RealnameAuthAgreementTemplateExtJSON() | RealnameAuthAgreementTemplateExtJSON |  |
| templateFileSign | String |  |

### Method List

| Name  | Type  | Description |
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




