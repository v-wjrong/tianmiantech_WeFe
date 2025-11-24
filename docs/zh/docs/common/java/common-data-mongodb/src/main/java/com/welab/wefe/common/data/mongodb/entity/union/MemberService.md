# 基础信息

|      |      |
|------|------|
| 名称 | MemberService |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/entity/union/MemberService.java |
| 包名 | com.welab.wefe.common.data.mongodb.entity.union |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.constant.MongodbTable', 'com.welab.wefe.common.data.mongodb.entity.base.AbstractBlockChainBusinessModel', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberServiceExtJSON', 'org.springframework.data.mongodb.core.mapping.Document'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberService | class |  |



## 类 MemberService

|      |      |
|------|------|
| 访问范围 | @Document(collection = MongodbTable.Union.MEMBER_SERVICE);public |
| 类型 | class |
| 名称 | MemberService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| name | String |  |
| serviceId | String |  |
| memberId | String |  |
| apiName | String |  |
| serviceType | String |  |
| extJson = new MemberServiceExtJSON() | MemberServiceExtJSON |  |
| baseUrl | String |  |
| queryParams | String |  |
| serviceStatus | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setBaseUrl | void |  |
| getBaseUrl | String |  |
| setApiName | void |  |
| setMemberId | void |  |
| getServiceId | String |  |
| getServiceType | String |  |
| getName | String |  |
| getExtJson | MemberServiceExtJSON |  |
| setServiceId | void |  |
| setExtJson | void |  |
| getApiName | String |  |
| setName | void |  |
| setServiceStatus | void |  |
| getMemberId | String |  |
| getServiceStatus | String |  |
| getQueryParams | String |  |
| setServiceType | void |  |
| setQueryParams | void |  |




