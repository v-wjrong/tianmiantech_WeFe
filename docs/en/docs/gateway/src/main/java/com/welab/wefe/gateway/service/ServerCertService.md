# Basic Information

|      |      |
|------|------|
| Name | ServerCertService |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/ServerCertService.java |
| Package Name | com.welab.wefe.gateway.service |
| Dependencies | ['java.util.List', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.dto.global_config.ServerCertInfoModel', 'com.welab.wefe.gateway.entity.CertInfoEntity', 'com.welab.wefe.gateway.entity.CertKeyInfoEntity', 'com.welab.wefe.gateway.entity.CertRequestInfoEntity', 'com.welab.wefe.gateway.repository.CertInfoRepository', 'com.welab.wefe.gateway.repository.CertKeyInfoRepository', 'com.welab.wefe.gateway.repository.CertRequestInfoRepository', 'com.welab.wefe.gateway.util.DatabaseEncryptUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServerCertService | class |  |



## Class ServerCertService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ServerCertService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| certKeyInfoRepository | CertKeyInfoRepository |  |
| certInfoRepository | CertInfoRepository |  |
| certRequestInfoRepository | CertRequestInfoRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getCertInfo | ServerCertInfoModel |  |




