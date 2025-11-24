# 基础信息

|      |      |
|------|------|
| 名称 | ClientMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/database/entity/ClientMysqlModel.java |
| 包名 | com.welab.wefe.serving.service.database.entity |
| 依赖项 | ['com.welab.wefe.serving.service.enums.ClientStatusEnum', 'javax.persistence.Column', 'javax.persistence.Entity'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ClientMysqlModel | class |  |



## 类 ClientMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "client");public |
| 类型 | class |
| 名称 | ClientMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| code | String |  |
| name | String |  |
| remark | String |  |
| serialVersionUID = -3524660109499676484L | long |  |
| pubKey | String |  |
| email | String |  |
| status = ClientStatusEnum.NORMAL.getValue() | Integer |  |
| ipAdd | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setCode | void |  |
| setRemark | void |  |
| setName | void |  |
| setEmail | void |  |
| setPubKey | void |  |
| getCode | String |  |
| getEmail | String |  |
| getRemark | String |  |
| getIpAdd | String |  |
| setIpAdd | void |  |
| getPubKey | String |  |
| getName | String |  |
| getStatus | Integer |  |
| setStatus | void |  |




