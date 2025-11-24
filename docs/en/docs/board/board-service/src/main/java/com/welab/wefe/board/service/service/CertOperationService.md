# Basic Information

|      |      |
|------|------|
| Name | CertOperationService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/CertOperationService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.webank.cert.toolkit.enums.CertDigestAlgEnums', 'com.webank.cert.toolkit.enums.CertStatusEnums', 'com.webank.cert.toolkit.enums.KeyAlgorithmEnums', 'com.webank.cert.toolkit.model.X500NameInfo', 'com.webank.cert.toolkit.service.CertService', 'com.webank.cert.toolkit.utils.CertUtils', 'com.webank.cert.toolkit.utils.KeyUtils', 'com.welab.wefe.board.service.database.entity.cert.CertInfoMysqlModel', 'com.welab.wefe.board.service.database.entity.cert.CertKeyInfoMysqlModel', 'com.welab.wefe.board.service.database.entity.cert.CertRequestInfoMysqlModel', 'com.welab.wefe.board.service.database.repository.CertInfoRepository', 'com.welab.wefe.board.service.database.repository.CertKeyInfoRepository', 'com.welab.wefe.board.service.database.repository.CertRequestInfoRepository', 'com.welab.wefe.board.service.sdk.union.UnionService', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.AESUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'org.apache.commons.lang3.StringUtils', 'org.bouncycastle.jce.provider.BouncyCastleProvider', 'org.bouncycastle.pkcs.PKCS10CertificationRequest', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.math.BigInteger', 'java.security.KeyPair', 'java.security.PublicKey', 'java.security.Security', 'java.security.cert.CertificateException', 'java.security.cert.X509Certificate', 'java.util.Date', 'java.util.List'] |
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
| certKeyInfoRepository | CertKeyInfoRepository |  |
| certInfoRepository | CertInfoRepository |  |
| LOG = LoggerFactory.getLogger(CertOperationService.class) | Logger |  |
| certRequestInfoRepository | CertRequestInfoRepository |  |
| unionService | UnionService |  |
| gatewayService | GatewayService |  |
| globalConfigService | GlobalConfigService |  |
| certService | CertService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| queryAllCertInfo | List<CertInfoMysqlModel> |  |
| findCertRequestById | CertRequestInfoMysqlModel |  |
| queryCertKeyInfoById | CertKeyInfoMysqlModel |  |
| getCertDigestAlg | CertDigestAlgEnums |  |
| saveCertInfo | void |  |
| exportCertToDerFile | void |  |
| updateStatus | void |  |
| queryAllCertRequestInfo | List<CertRequestInfoMysqlModel> |  |
| queryAllCertKey | List<CertKeyInfoMysqlModel> |  |
| resetCert | void |  |
| queryCertInfoById | CertInfoMysqlModel |  |
| findBySerialNumber | CertInfoMysqlModel |  |
| createCertRequestInfo | CertRequestInfoMysqlModel |  |
| savePrivateKey | CertKeyInfoMysqlModel |  |
| buildCertRequestInfo | CertRequestInfoMysqlModel |  |
| buildCertInfo | CertInfoMysqlModel |  |
| getKeyPair | KeyPair |  |




