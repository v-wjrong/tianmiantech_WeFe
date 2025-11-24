# 基础信息

|      |      |
|------|------|
| 名称 | Member |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/Member.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| Member | class |  |



## 类 Member

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.MEMBER);public |
| 类型 | class |
| 名称 | Member |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| extJson = new MemberExtJSON() | MemberExtJSON |  |
| lastActivityTime | String |  |
| gatewayUri | String |  |
| name | String |  |
| mobile | String |  |
| freezed | String |  |
| hidden | String |  |
| email | String |  |
| lostContact | String |  |
| memberId | String |  |
| logo | String |  |
| publicKey | String |  |
| allowOpenDataSet | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getMemberId | String |  |
| setLogo | void |  |
| setEmail | void |  |
| getEmail | String |  |
| setPublicKey | void |  |
| getLostContact | String |  |
| getHidden | String |  |
| setGatewayUri | void |  |
| setLostContact | void |  |
| setName | void |  |
| getName | String |  |
| setHidden | void |  |
| getPublicKey | String |  |
| setFreezed | void |  |
| getGatewayUri | String |  |
| setAllowOpenDataSet | void |  |
| getFreezed | String |  |
| getLogo | String |  |
| setMobile | void |  |
| getAllowOpenDataSet | String |  |
| setMemberId | void |  |
| getMobile | String |  |
| getLastActivityTime | String |  |
| setLastActivityTime | void |  |
| getExtJson | MemberExtJSON |  |
| setExtJson | void |  |




