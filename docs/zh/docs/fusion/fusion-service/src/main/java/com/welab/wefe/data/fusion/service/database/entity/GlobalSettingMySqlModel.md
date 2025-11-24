# 基础信息

|      |      |
|------|------|
| 名称 | GlobalSettingMySqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/database/entity/GlobalSettingMySqlModel.java |
| 包名 | com.welab.wefe.data.fusion.service.database.entity |
| 依赖项 | ['javax.persistence.Entity', 'java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GlobalSettingMySqlModel | class |  |



## 类 GlobalSettingMySqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "global_setting");public |
| 类型 | class |
| 名称 | GlobalSettingMySqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| partnerName | String |  |
| rsaPrivateKey | String |  |
| rsaPublicKey | String |  |
| partnerId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setPartnerId | void |  |
| getPartnerId | String |  |
| setPartnerName | void |  |
| getRsaPrivateKey | String |  |
| getPartnerName | String |  |
| setRsaPrivateKey | void |  |
| getRsaPublicKey | String |  |
| setRsaPublicKey | void |  |




