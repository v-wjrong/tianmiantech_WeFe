# Basic Information

|      |      |
|------|------|
| Name | CertService |
| Language | .java |
| Code Path | WeFe/common/java/common-cert/src/main/java/com/webank/cert/toolkit/service/CertService.java |
| Package Name | com.webank.cert.toolkit.service |
| Dependencies | ['java.io.FileNotFoundException', 'java.math.BigInteger', 'java.security.KeyPair', 'java.security.Principal', 'java.security.PrivateKey', 'java.security.PublicKey', 'java.security.cert.CRLException', 'java.security.cert.X509CRL', 'java.security.cert.X509CRLEntry', 'java.security.cert.X509Certificate', 'java.util.ArrayList', 'java.util.Date', 'java.util.List', 'java.util.Set', 'org.bouncycastle.asn1.x500.X500Name', 'org.bouncycastle.asn1.x509.KeyUsage', 'org.bouncycastle.operator.OperatorCreationException', 'org.bouncycastle.pkcs.PKCS10CertificationRequest', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.webank.cert.toolkit.constants.CertConstants', 'com.webank.cert.toolkit.handler.X509CertHandler', 'com.webank.cert.toolkit.model.X500NameInfo', 'com.webank.cert.toolkit.utils.CertUtils', 'com.webank.cert.toolkit.utils.FileOperationUtils', 'com.webank.cert.toolkit.utils.KeyUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertService | class |  |



## Class CertService

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CertService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(CertService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateChildCertByDefaultConf | String |  |
| createRootCertificate | X509Certificate |  |
| generateChildCertByDefaultConf | String |  |
| generateCertRequestByDefaultConf | String |  |
| createChildCertificate | X509Certificate |  |
| generateChildCertByDefaultConf | String |  |
| generateRootCertByDefaultConf | String |  |
| createCertRequest | PKCS10CertificationRequest |  |
| generateCertRequestByDefaultConf | String |  |
| generateRootCertByDefaultConf | String |  |
| generateChildCertByDefaultConf | String |  |
| generateKPAndRootCert | void |  |
| generateKPAndRootCert | void |  |
| createCRL | X509CRL |  |
| createCRL | X509CRL |  |
| verify | boolean |  |
| verify | boolean |  |




