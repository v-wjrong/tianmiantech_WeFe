# Basic Information

|      |      |
|------|------|
| Name | GlobalSettingMySqlModel |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/GlobalSettingMySqlModel.java |
| Package Name | com.welab.wefe.data.fusion.service.database.entity |
| Dependencies | ['javax.persistence.Entity', 'java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GlobalSettingMySqlModel | class |  |



## Class GlobalSettingMySqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "global_setting");public |
| Type | class |
| Name | GlobalSettingMySqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerName | String |  |
| rsaPrivateKey | String |  |
| rsaPublicKey | String |  |
| partnerId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setPartnerId | void |  |
| getPartnerId | String |  |
| setPartnerName | void |  |
| getRsaPrivateKey | String |  |
| getPartnerName | String |  |
| setRsaPrivateKey | void |  |
| getRsaPublicKey | String |  |
| setRsaPublicKey | void |  |




