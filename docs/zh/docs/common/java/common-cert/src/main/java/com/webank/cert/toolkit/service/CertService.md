# 基础信息

|      |      |
|------|------|
| 名称 | CertService |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-cert/src/main/java/com/webank/cert/toolkit/service/CertService.java |
| 包名 | com.webank.cert.toolkit.service |
| 依赖项 | ['java.io.FileNotFoundException', 'java.math.BigInteger', 'java.security.KeyPair', 'java.security.Principal', 'java.security.PrivateKey', 'java.security.PublicKey', 'java.security.cert.CRLException', 'java.security.cert.X509CRL', 'java.security.cert.X509CRLEntry', 'java.security.cert.X509Certificate', 'java.util.ArrayList', 'java.util.Date', 'java.util.List', 'java.util.Set', 'org.bouncycastle.asn1.x500.X500Name', 'org.bouncycastle.asn1.x509.KeyUsage', 'org.bouncycastle.operator.OperatorCreationException', 'org.bouncycastle.pkcs.PKCS10CertificationRequest', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.webank.cert.toolkit.constants.CertConstants', 'com.webank.cert.toolkit.handler.X509CertHandler', 'com.webank.cert.toolkit.model.X500NameInfo', 'com.webank.cert.toolkit.utils.CertUtils', 'com.webank.cert.toolkit.utils.FileOperationUtils', 'com.webank.cert.toolkit.utils.KeyUtils'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertService | class |  |



## 类 CertService

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CertService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(CertService.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




