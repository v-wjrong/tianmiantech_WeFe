# 基础信息

|      |      |
|------|------|
| 名称 | CertUtils |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-cert/src/main/java/com/webank/cert/toolkit/utils/CertUtils.java |
| 包名 | com.webank.cert.toolkit.utils |
| 依赖项 | ['java.io.ByteArrayOutputStream', 'java.io.File', 'java.io.FileInputStream', 'java.io.FileNotFoundException', 'java.io.FileOutputStream', 'java.io.FileReader', 'java.io.FileWriter', 'java.io.IOException', 'java.io.InputStream', 'java.io.OutputStream', 'java.io.OutputStreamWriter', 'java.io.StringReader', 'java.io.StringWriter', 'java.security.Key', 'java.security.KeyFactory', 'java.security.KeyStore', 'java.security.KeyStoreException', 'java.security.NoSuchAlgorithmException', 'java.security.PrivateKey', 'java.security.PublicKey', 'java.security.Security', 'java.security.cert.CRLException', 'java.security.cert.CertificateEncodingException', 'java.security.cert.CertificateException', 'java.security.cert.X509CRL', 'java.security.cert.X509Certificate', 'java.security.spec.PKCS8EncodedKeySpec', 'java.util.Enumeration', 'java.util.List', 'org.apache.commons.lang3.StringUtils', 'org.bouncycastle.asn1.oiw.OIWObjectIdentifiers', 'org.bouncycastle.asn1.pkcs.PrivateKeyInfo', 'org.bouncycastle.asn1.x509.AlgorithmIdentifier', 'org.bouncycastle.asn1.x509.AuthorityKeyIdentifier', 'org.bouncycastle.asn1.x509.SubjectKeyIdentifier', 'org.bouncycastle.asn1.x509.SubjectPublicKeyInfo', 'org.bouncycastle.cert.X509CRLHolder', 'org.bouncycastle.cert.X509CertificateHolder', 'org.bouncycastle.cert.X509ExtensionUtils', 'org.bouncycastle.cert.jcajce.JcaX509CRLConverter', 'org.bouncycastle.cert.jcajce.JcaX509CertificateConverter', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.openssl.PEMKeyPair', 'org.bouncycastle.openssl.PEMParser', 'org.bouncycastle.openssl.jcajce.JcaPEMWriter', 'org.bouncycastle.openssl.jcajce.JcaPKCS8Generator', 'org.bouncycastle.operator.DigestCalculator', 'org.bouncycastle.operator.OperatorCreationException', 'org.bouncycastle.operator.bc.BcDigestCalculatorProvider', 'org.bouncycastle.pkcs.PKCS10CertificationRequest', 'org.bouncycastle.util.io.pem.PemReader', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertUtils | class |  |



## 类 CertUtils

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CertUtils |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(CertUtils.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| convertStrToCsr | PKCS10CertificationRequest |  |
| readPEMAsString | String |  |
| writeCsr | void |  |
| convertStrToCert | X509Certificate |  |
| importCertToTrustStore | void |  |
| writeKey | void |  |
| writeToFileByDer | void |  |
| readCrt | X509Certificate |  |
| writeCer | void |  |
| writeDer | void |  |
| readPriKeyFromJks | PrivateKey |  |
| readCsr | PKCS10CertificationRequest |  |
| writeToPKCS8File | void |  |
| writeCrt | void |  |
| toBytes | byte[] |  |
| readRSAPrivateKey | Key |  |
| readKey | PEMKeyPair |  |
| writeToFileByPem | void |  |
| writeCrl | void |  |
| writePublicKey | void |  |
| getAuthorityKeyId | AuthorityKeyIdentifier |  |
| readCrl | X509CRL |  |
| convertPemStrToObject | Object |  |
| getSubjectKeyId | SubjectKeyIdentifier |  |
| readPriKeyFromPfx | PrivateKey |  |
| savePfx | void |  |
| readRSAKey | Key |  |
| readPEMObjectFromFile | Object |  |




