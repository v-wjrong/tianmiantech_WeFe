# Basic Information

|      |      |
|------|------|
| Name | CertRequestInfoMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/cert/CertRequestInfoMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.cert |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Entity', 'org.hibernate.annotations.TypeDef', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertRequestInfoMysqlModel | class |  |



## Class CertRequestInfoMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "cert_request_info");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | CertRequestInfoMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| issue | Boolean |  |
| certRequestContent | String |  |
| subjectOrg | String |  |
| subjectKeyId | String |  |
| subjectCN | String |  |
| serialVersionUID = -6973794829218983299L | long |  |
| memberId | String |  |

### Method List

| Name  | Type  | Description |
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




