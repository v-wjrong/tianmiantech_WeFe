# 基础信息

|      |      |
|------|------|
| 名称 | CertInfoMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/cert/CertInfoMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.cert |
| 依赖项 | ['javax.persistence.Column', 'javax.persistence.Entity', 'org.hibernate.annotations.TypeDef', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertInfoMysqlModel | class |  |



## 类 CertInfoMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "cert_info");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| 类型 | class |
| 名称 | CertInfoMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| certContent | String |  |
| status | String |  |
| csrId | String |  |
| serialNumber | String |  |
| memberId | String |  |
| subjectPubKey | String |  |
| subjectCN | String |  |
| subjectOrg | String |  |
| serialVersionUID = 3983194628565221216L | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setSerialNumber | void |  |
| setMemberId | void |  |
| setSubjectPubKey | void |  |
| getSerialNumber | String |  |
| getSubjectCN | String |  |
| getSubjectOrg | String |  |
| getMemberId | String |  |
| setSubjectCN | void |  |
| setSubjectOrg | void |  |
| getCertContent | String |  |
| getSubjectPubKey | String |  |
| setCertContent | void |  |
| getCsrId | String |  |
| setCsrId | void |  |
| getStatus | String |  |
| setStatus | void |  |




