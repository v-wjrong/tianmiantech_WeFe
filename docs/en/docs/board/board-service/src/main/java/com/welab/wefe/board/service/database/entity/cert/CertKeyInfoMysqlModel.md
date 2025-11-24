# Basic Information

|      |      |
|------|------|
| Name | CertKeyInfoMysqlModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/cert/CertKeyInfoMysqlModel.java |
| Package Name | com.welab.wefe.board.service.database.entity.cert |
| Dependencies | ['javax.persistence.Column', 'javax.persistence.Entity', 'org.hibernate.annotations.TypeDef', 'com.vladmihalcea.hibernate.type.json.JsonStringType', 'com.welab.wefe.board.service.database.entity.base.AbstractBaseMySqlModel', 'com.welab.wefe.common.exception.StatusCodeWithException'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertKeyInfoMysqlModel | class |  |



## Class CertKeyInfoMysqlModel

|      |      |
|------|------|
| Access Modifier | @Entity(name = "cert_key_info");@TypeDef(name = "json", typeClass = JsonStringType.class);public |
| Type | class |
| Name | CertKeyInfoMysqlModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| keyAlg | String |  |
| keyPem | String |  |
| serialVersionUID = -7493726478506825680L | long |  |
| memberId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setKeyPem | void |  |
| getKeyPem | String |  |
| getKeyAlg | String |  |
| getMemberId | String |  |
| setMemberId | void |  |
| setKeyAlg | void |  |




