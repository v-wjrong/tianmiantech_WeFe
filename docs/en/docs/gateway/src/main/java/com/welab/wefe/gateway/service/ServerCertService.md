# Basic Information

|      |      |
|------|------|
| Name | ServerCertService |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/ServerCertService.java |
| Package Name | com.welab.wefe.gateway.service |
| Dependencies | ['java.util.List', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.dto.global_config.ServerCertInfoModel', 'com.welab.wefe.gateway.entity.CertInfoEntity', 'com.welab.wefe.gateway.entity.CertKeyInfoEntity', 'com.welab.wefe.gateway.entity.CertRequestInfoEntity', 'com.welab.wefe.gateway.repository.CertInfoRepository', 'com.welab.wefe.gateway.repository.CertKeyInfoRepository', 'com.welab.wefe.gateway.repository.CertRequestInfoRepository', 'com.welab.wefe.gateway.util.DatabaseEncryptUtil'] |
| Brief Description | The ServerCertService class retrieves certificate information in the VALID state, associates it with key and request data, decrypts the information, and returns a ServerCertInfoModel object. |

# Description

ServerCertService is a service class used to retrieve server certificate information. It relies on three repository classes: CertInfoRepository, CertKeyInfoRepository, and CertRequestInfoRepository. The getCertInfo method first queries a list of certificate entities with a status of VALID, sorted in descending order by creation time. If the list is empty, it returns null. Then, it queries the certificate request entity using the csrId from the certificate entity, followed by querying the key entity using the subjectKeyId from the request entity. If any entity does not exist, it returns null. Finally, it constructs a ServerCertInfoModel object, decrypts the key content, sets the certificate content, and returns it.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServerCertService | class | The ServerCertService class retrieves certificate information in the VALID state, associates request and key data, and returns the decrypted key along with the certificate content. |



## Class ServerCertService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ServerCertService |
| Description | The ServerCertService class retrieves certificate information in the VALID state, associates request and key data, and returns the decrypted key along with the certificate content. |


### UML Class Diagram

```mermaid
classDiagram
    class ServerCertService {
        -CertInfoRepository certInfoRepository
        -CertKeyInfoRepository certKeyInfoRepository
        -CertRequestInfoRepository certRequestInfoRepository
        +getCertInfo() ServerCertInfoModel
    }

    class CertInfoEntity {
        <<Entity>>
        -String status
        -Date createdTime
        -String csrId
        -String content
    }

    class CertRequestInfoEntity {
        <<Entity>>
        -String subjectKeyId
    }

    class CertKeyInfoEntity {
        <<Entity>>
        -String keyPem
    }

    class ServerCertInfoModel {
        -String key
        -String content
        +setKey(String key)
        +setContent(String content)
    }

    class DatabaseEncryptUtil {
        <<Utility>>
        +decrypt(String encrypted) String
    }

    ServerCertService --> CertInfoRepository : depends
    ServerCertService --> CertKeyInfoRepository : depends
    ServerCertService --> CertRequestInfoRepository : depends
    ServerCertService --> ServerCertInfoModel : creates
    ServerCertService --> DatabaseEncryptUtil : invokes
    CertInfoRepository --> CertInfoEntity : queries
    CertRequestInfoRepository --> CertRequestInfoEntity : queries
    CertKeyInfoRepository --> CertKeyInfoEntity : queries
```

This class diagram illustrates the relationships between ServerCertService and multiple entity classes as well as utility classes. ServerCertService operates on CertInfoEntity, CertKeyInfoEntity, and CertRequestInfoEntity through three repositories (CertInfoRepository, CertKeyInfoRepository, CertRequestInfoRepository) respectively, ultimately constructing a ServerCertInfoModel object. The DatabaseEncryptUtil utility class is used for key decryption, demonstrating the complete process from querying certificate information in the database to assembling and returning the model.


### Internal Method Call Graph

```mermaid
graph TD
    A["ServerCertService class"]
    B["Dependency Injection: CertInfoRepository"]
    C["Dependency Injection: CertKeyInfoRepository"]
    D["Dependency Injection: CertRequestInfoRepository"]
    E["Method: getCertInfo()"]
    F["Create Specification query conditions"]
    G["Query certificate list in VALID status"]
    H["Check if result is empty"]
    I["Query associated CSR record"]
    J["Check if CSR record exists"]
    K["Query associated key record"]
    L["Check if key record exists"]
    M["Create ServerCertInfoModel"]
    N["Decrypt key and set model attributes"]
    O["Return model object"]

    A --> B
    A --> C
    A --> D
    A --> E
    E --> F
    F --> G
    G --> H
    H --"Not empty"--> I
    H --"Empty"--> O
    I --> J
    J --"Exists"--> K
    J --"Not exists"--> O
    K --> L
    L --"Exists"--> M
    L --"Not exists"--> O
    M --> N
    N --> O
```

This code flowchart illustrates the complete process of obtaining certificate information in the ServerCertService class. The service operates on the database through three Repository components, first querying the list of certificates in VALID status, then sequentially querying associated CSR request records and key records, and finally constructing and returning a model object containing the decrypted key and certificate content. The flow includes three critical null-check nodes to ensure safe return of null when data is missing at any stage. The entire process demonstrates a complete handling chain from data acquisition to business model transformation.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| certKeyInfoRepository | CertKeyInfoRepository | Automatically inject the CertKeyInfoRepository instance. |
| certInfoRepository | CertInfoRepository | Automatically inject the CertInfoRepository instance. |
| certRequestInfoRepository | CertRequestInfoRepository | Using @Autowired to automatically inject an instance of CertRequestInfoRepository. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getCertInfo | ServerCertInfoModel | Obtain valid certificate information, including keys and content, or return empty if it does not exist. |




