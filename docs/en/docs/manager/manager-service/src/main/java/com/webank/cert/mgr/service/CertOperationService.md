# Basic Information

|      |      |
|------|------|
| Name | CertOperationService |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/webank/cert/mgr/service/CertOperationService.java |
| Package Name | com.webank.cert.mgr.service |
| Dependencies | ['java.math.BigInteger', 'java.security.KeyPair', 'java.security.PublicKey', 'java.security.Security', 'java.security.cert.CertificateExpiredException', 'java.security.cert.CertificateNotYetValidException', 'java.security.cert.X509Certificate', 'java.util.Date', 'java.util.List', 'javax.transaction.Transactional', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'org.apache.commons.lang3.StringUtils', 'org.bouncycastle.asn1.x500.RDN', 'org.bouncycastle.asn1.x500.style.BCStyle', 'org.bouncycastle.asn1.x509.KeyUsage', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.pkcs.PKCS10CertificationRequest', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'com.webank.cert.mgr.db.dao.CertDao', 'com.webank.cert.mgr.enums.MgrExceptionCodeEnums', 'com.webank.cert.mgr.exception.CertMgrException', 'com.webank.cert.mgr.model.vo.CertKeyVO', 'com.webank.cert.mgr.model.vo.CertRequestVO', 'com.webank.cert.mgr.model.vo.CertVO', 'com.webank.cert.mgr.utils.TransformUtils', 'com.webank.cert.toolkit.constants.CertConstants', 'com.webank.cert.toolkit.enums.CertDigestAlgEnums', 'com.webank.cert.toolkit.enums.CertStatusEnums', 'com.webank.cert.toolkit.enums.KeyAlgorithmEnums', 'com.webank.cert.toolkit.model.X500NameInfo', 'com.webank.cert.toolkit.service.CertService', 'com.webank.cert.toolkit.utils.CertUtils', 'com.webank.cert.toolkit.utils.KeyUtils', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.entity.manager.CertInfo', 'com.welab.wefe.common.data.mongodb.entity.manager.CertKeyInfo', 'com.welab.wefe.common.data.mongodb.entity.manager.CertRequestInfo', 'com.welab.wefe.common.web.util.DatabaseEncryptUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertOperationService | class |  |



## Class CertOperationService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | CertOperationService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(CertOperationService.class) | Logger |  |
| certDao | CertDao |  |
| certService | CertService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| updateCanTrust | void |  |
| savePrivateKey | CertKeyInfo |  |
| updateStatusByUserId | void |  |
| findCertRequestById | CertRequestVO |  |
| findKeys | PageOutput<CertKeyInfo> |  |
| queryCertRequestList | PageOutput<CertRequestInfo> |  |
| findCertList | List<CertInfo> |  |
| createUserCertRequest | CertRequestInfo |  |
| findBySerialNumber | CertVO |  |
| initRootCert | CertVO |  |
| queryCertInfoByCertId | CertVO |  |
| createUserCert | CertVO |  |
| findCertList | PageOutput<CertInfo> |  |
| buildCertRequestInfo | CertRequestInfo |  |
| buildCertInfo | CertInfo |  |
| getCertDigestAlg | CertDigestAlgEnums |  |
| getKeyPair | KeyPair |  |
| createIssuerCert | CertVO |  |
| findCertKeyById | CertKeyVO |  |
| updateStatusBySerialNumber | void |  |
| exportCertToDerFile | void |  |




