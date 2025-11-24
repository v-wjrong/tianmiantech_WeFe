# Basic Information

|      |      |
|------|------|
| Name | X509CertHandler |
| Language | .java |
| Code Path | WeFe/common/java/common-cert/src/main/java/com/webank/cert/toolkit/handler/X509CertHandler.java |
| Package Name | com.webank.cert.toolkit.handler |
| Dependencies | ['java.math.BigInteger', 'java.security.PrivateKey', 'java.security.PublicKey', 'java.security.Security', 'java.security.cert.CRLException', 'java.security.cert.X509CRL', 'java.security.cert.X509Certificate', 'java.util.ArrayList', 'java.util.Date', 'java.util.List', 'java.util.Random', 'org.bouncycastle.asn1.x500.X500Name', 'org.bouncycastle.asn1.x509.BasicConstraints', 'org.bouncycastle.asn1.x509.Extension', 'org.bouncycastle.asn1.x509.GeneralName', 'org.bouncycastle.asn1.x509.GeneralNames', 'org.bouncycastle.asn1.x509.KeyUsage', 'org.bouncycastle.cert.CertIOException', 'org.bouncycastle.cert.X509CRLHolder', 'org.bouncycastle.cert.X509v2CRLBuilder', 'org.bouncycastle.cert.X509v3CertificateBuilder', 'org.bouncycastle.cert.jcajce.JcaX509CRLConverter', 'org.bouncycastle.cert.jcajce.JcaX509CertificateConverter', 'org.bouncycastle.cert.jcajce.JcaX509v3CertificateBuilder', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.operator.ContentSigner', 'org.bouncycastle.operator.OperatorCreationException', 'org.bouncycastle.operator.jcajce.JcaContentSignerBuilder', 'org.bouncycastle.pkcs.PKCS10CertificationRequest', 'org.bouncycastle.pkcs.PKCS10CertificationRequestBuilder', 'org.bouncycastle.pkcs.jcajce.JcaPKCS10CertificationRequest', 'org.bouncycastle.pkcs.jcajce.JcaPKCS10CertificationRequestBuilder'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| X509CertHandler | class |  |



## Class X509CertHandler

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | X509CertHandler |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| buildCertExtension | void |  |
| createCSR | PKCS10CertificationRequest |  |
| createChildCert | X509Certificate |  |
| createRootCert | X509Certificate |  |
| createCert | X509Certificate |  |
| makeContentSignerBuilder | JcaContentSignerBuilder |  |
| revokeCert | X509CRL |  |




