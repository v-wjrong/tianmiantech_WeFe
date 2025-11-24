# Basic Information

|      |      |
|------|------|
| Name | CertUtils |
| Language | .java |
| Code Path | WeFe/common/java/common-cert/src/main/java/com/webank/cert/toolkit/utils/CertUtils.java |
| Package Name | com.webank.cert.toolkit.utils |
| Dependencies | ['java.io.ByteArrayOutputStream', 'java.io.File', 'java.io.FileInputStream', 'java.io.FileNotFoundException', 'java.io.FileOutputStream', 'java.io.FileReader', 'java.io.FileWriter', 'java.io.IOException', 'java.io.InputStream', 'java.io.OutputStream', 'java.io.OutputStreamWriter', 'java.io.StringReader', 'java.io.StringWriter', 'java.security.Key', 'java.security.KeyFactory', 'java.security.KeyStore', 'java.security.KeyStoreException', 'java.security.NoSuchAlgorithmException', 'java.security.PrivateKey', 'java.security.PublicKey', 'java.security.Security', 'java.security.cert.CRLException', 'java.security.cert.CertificateEncodingException', 'java.security.cert.CertificateException', 'java.security.cert.X509CRL', 'java.security.cert.X509Certificate', 'java.security.spec.PKCS8EncodedKeySpec', 'java.util.Enumeration', 'java.util.List', 'org.apache.commons.lang3.StringUtils', 'org.bouncycastle.asn1.oiw.OIWObjectIdentifiers', 'org.bouncycastle.asn1.pkcs.PrivateKeyInfo', 'org.bouncycastle.asn1.x509.AlgorithmIdentifier', 'org.bouncycastle.asn1.x509.AuthorityKeyIdentifier', 'org.bouncycastle.asn1.x509.SubjectKeyIdentifier', 'org.bouncycastle.asn1.x509.SubjectPublicKeyInfo', 'org.bouncycastle.cert.X509CRLHolder', 'org.bouncycastle.cert.X509CertificateHolder', 'org.bouncycastle.cert.X509ExtensionUtils', 'org.bouncycastle.cert.jcajce.JcaX509CRLConverter', 'org.bouncycastle.cert.jcajce.JcaX509CertificateConverter', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.openssl.PEMKeyPair', 'org.bouncycastle.openssl.PEMParser', 'org.bouncycastle.openssl.jcajce.JcaPEMWriter', 'org.bouncycastle.openssl.jcajce.JcaPKCS8Generator', 'org.bouncycastle.operator.DigestCalculator', 'org.bouncycastle.operator.OperatorCreationException', 'org.bouncycastle.operator.bc.BcDigestCalculatorProvider', 'org.bouncycastle.pkcs.PKCS10CertificationRequest', 'org.bouncycastle.util.io.pem.PemReader', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CertUtils | class |  |



## Class CertUtils

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CertUtils |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(CertUtils.class) | Logger |  |

### Method List

| Name  | Type  | Description |
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




