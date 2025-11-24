# 基础信息

|      |      |
|------|------|
| 名称 | CertRequestInfoMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/cert/CertRequestInfoMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.cert |
| 依赖项 | ['javax.persistence.Column', 'javax.persistence.Entity', 'org.hibernate.annotations.TypeDef', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertRequestInfoMysqlModel | class |  |



## 类 CertRequestInfoMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "cert_request_info");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | CertRequestInfoMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| issue | Boolean |  |
| certRequestContent | String |  |
| subjectOrg | String |  |
| subjectKeyId | String |  |
| subjectCN | String |  |
| serialVersionUID = -6973794829218983299L | long |  |
| memberId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setMemberId | void |  |
| setSubjectOrg | void |  |
| getSubjectCN | String |  |
| setSubjectCN | void |  |
| getMemberId | String |  |
| setCertRequestContent | void |  |
| getCertRequestContent | String |  |
| getSubjectKeyId | String |  |
| getSubjectOrg | String |  |
| setSubjectKeyId | void |  |
| getIssue | Boolean |  |
| setIssue | void |  |




