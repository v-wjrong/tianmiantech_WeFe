# Basic Information

|      |      |
|------|------|
| Name | CertInfoMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/cert/CertInfoMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.cert |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Entity', 'org.hibernate.annotations.TypeDef', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertInfoMysqlModel | class |  |



## Class CertInfoMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "cert_info");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | CertInfoMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




