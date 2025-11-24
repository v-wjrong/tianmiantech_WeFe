# Basic Information

|      |      |
|------|------|
| Name | KeyUtils |
| Language | .java |
| Code Path | WeFe/common/java/common-cert/src/main/java/com/webank/cert/toolkit/utils/KeyUtils.java |
| Package Name | com.webank.cert.toolkit.utils |
| Dependencies | ['java.io.ByteArrayOutputStream', 'java.io.IOException', 'java.io.OutputStreamWriter', 'java.math.BigInteger', 'java.security.InvalidAlgorithmParameterException', 'java.security.KeyFactory', 'java.security.KeyPair', 'java.security.KeyPairGenerator', 'java.security.NoSuchAlgorithmException', 'java.security.NoSuchProviderException', 'java.security.PrivateKey', 'java.security.PublicKey', 'java.security.SecureRandom', 'java.security.interfaces.ECPrivateKey', 'java.security.spec.ECGenParameterSpec', 'java.security.spec.ECParameterSpec', 'java.security.spec.ECPoint', 'java.security.spec.ECPublicKeySpec', 'java.security.spec.InvalidKeySpecException', 'java.security.spec.PKCS8EncodedKeySpec', 'java.security.spec.RSAPrivateKeySpec', 'java.security.spec.RSAPublicKeySpec', 'java.security.spec.X509EncodedKeySpec', 'java.util.Collections', 'org.apache.commons.codec.binary.Base64', 'org.bouncycastle.crypto.AsymmetricCipherKeyPair', 'org.bouncycastle.crypto.generators.ECKeyPairGenerator', 'org.bouncycastle.crypto.params.ECDomainParameters', 'org.bouncycastle.crypto.params.ECKeyGenerationParameters', 'org.bouncycastle.jcajce.provider.asymmetric.ec.BCECPrivateKey', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.math.ec.custom.gm.SM2P256V1Curve', 'org.bouncycastle.openssl.PEMKeyPair', 'org.bouncycastle.util.io.pem.PemObject', 'org.bouncycastle.util.io.pem.PemWriter', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| KeyUtils | class |  |



## Class KeyUtils

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | KeyUtils |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| SM2_ECC_GY = new BigInteger(			"BC3736A2F4F6779C59BDCEE36B692153D0A9877CC62A474002DF32E52139F0A0", 16) | BigInteger |  |
| LOG = LoggerFactory.getLogger(KeyUtils.class) | Logger |  |
| DOMAIN_PARAMS = new ECDomainParameters(CURVE, G_POINT,			SM2_ECC_N, SM2_ECC_H) | ECDomainParameters |  |
| SM2_ECC_H = CURVE.getCofactor() | BigInteger |  |
| random = new SecureRandom() | SecureRandom |  |
| G_POINT = CURVE.createPoint(SM2_ECC_GX, SM2_ECC_GY) | org.bouncycastle.math.ec.ECPoint |  |
| PEM_STRING_ECPRIVATEKEY = "EC PRIVATE KEY" | String |  |
| SM2_ECC_GX = new BigInteger(			"32C4AE2C1F1981195F9904466A39C9948FE30BBFF2660BE1715A4589334C74C7", 16) | BigInteger |  |
| CURVE = new SM2P256V1Curve() | SM2P256V1Curve |  |
| SM2_ECC_N = CURVE.getOrder() | BigInteger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| convertECPrivateKeyPKCS8ToPEM | String |  |
| generateECDSAKeyPair | KeyPair |  |
| generateSM2KeyPairParameter | AsymmetricCipherKeyPair |  |
| generateKeyPair | KeyPair |  |
| convertPKCS8ToECPrivateKey | BCECPrivateKey |  |
| generateKeyPairParameter | AsymmetricCipherKeyPair |  |
| generateSM2KeyPair | KeyPair |  |
| getRSAPublicKey | PublicKey |  |
| generateECKeyPair | KeyPair |  |
| convertEncodedDataToPEM | String |  |
| getRSAPrivateKey | PrivateKey |  |
| getRSAPublicKey | PublicKey |  |
| getECKeyPair | KeyPair |  |
| getRSAKeyPair | KeyPair |  |
| getPublicKey | PublicKey |  |
| tryFindNamedCurveSpec | ECParameterSpec |  |




