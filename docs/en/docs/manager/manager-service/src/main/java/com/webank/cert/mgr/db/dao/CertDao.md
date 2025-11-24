# Basic Information

|      |      |
|------|------|
| Name | CertDao |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/webank/cert/mgr/db/dao/CertDao.java |
| Package Name | com.webank.cert.mgr.db.dao |
| Dependencies | ['java.util.List', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.entity.manager.CertInfo', 'com.welab.wefe.common.data.mongodb.entity.manager.CertKeyInfo', 'com.welab.wefe.common.data.mongodb.entity.manager.CertRequestInfo', 'com.welab.wefe.common.data.mongodb.repo.CertInfoRepo', 'com.welab.wefe.common.data.mongodb.repo.CertKeyInfoRepo', 'com.welab.wefe.common.data.mongodb.repo.CertRequestInfoRepo'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertDao | class |  |



## Class CertDao

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | CertDao |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| certKeyInfoRepo | CertKeyInfoRepo |  |
| certRequestInfoRepo | CertRequestInfoRepo |  |
| certInfoRepo | CertInfoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findCertRequestList | PageOutput<CertRequestInfo> |  |
| findCertById | CertInfo |  |
| findCertList | List<CertInfo> |  |
| findByPCertIdAndSubjectKeyId | CertRequestInfo |  |
| findCertRequestById | CertRequestInfo |  |
| save | CertRequestInfo |  |
| findKeyByUserId | List<CertKeyInfo> |  |
| updateStatusByUserId | void |  |
| findCertList | PageOutput<CertInfo> |  |
| findKeyByPkId | CertKeyInfo |  |
| findCertKeyById | CertKeyInfo |  |
| updateStatusBySerialNumber | void |  |
| findKeys | PageOutput<CertKeyInfo> |  |
| save | CertInfo |  |
| findBySerialNumber | CertInfo |  |
| updateCanTrust | void |  |
| save | CertKeyInfo |  |




