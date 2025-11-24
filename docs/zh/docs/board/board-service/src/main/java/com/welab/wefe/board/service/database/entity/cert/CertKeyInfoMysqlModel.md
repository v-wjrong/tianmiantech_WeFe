# 基础信息

|      |      |
|------|------|
| 名称 | CertKeyInfoMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/cert/CertKeyInfoMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.cert |
| 依赖项 | ['javax.persistence.Column', 'javax.persistence.Entity', 'org.hibernate.annotations.TypeDef', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.exception.StatusCodeWithException'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertKeyInfoMysqlModel | class |  |



## 类 CertKeyInfoMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "cert_key_info");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | CertKeyInfoMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| keyAlg | String |  |
| keyPem | String |  |
| serialVersionUID = -7493726478506825680L | long |  |
| memberId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setKeyPem | void |  |
| getKeyPem | String |  |
| getKeyAlg | String |  |
| getMemberId | String |  |
| setMemberId | void |  |
| setKeyAlg | void |  |




