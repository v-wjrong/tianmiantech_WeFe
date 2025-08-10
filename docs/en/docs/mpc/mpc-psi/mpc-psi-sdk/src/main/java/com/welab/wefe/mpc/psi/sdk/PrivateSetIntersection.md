# Basic Information

|      |      |
|------|------|
| Name | PrivateSetIntersection |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/PrivateSetIntersection.java |
| Package Name | com.welab.wefe.mpc.psi.sdk |
| Dependencies | ['java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.Set', 'java.util.stream.Collectors', 'org.apache.commons.collections4.CollectionUtils', 'com.welab.wefe.mpc.config.CommunicationConfig', 'com.welab.wefe.mpc.psi.request.QueryPrivateSetIntersectionRequest', 'com.welab.wefe.mpc.psi.request.QueryPrivateSetIntersectionResponse', 'com.welab.wefe.mpc.psi.sdk.dh.DhPsiClient', 'com.welab.wefe.mpc.psi.sdk.service.PrivateSetIntersectionService', 'com.welab.wefe.mpc.psi.sdk.util.EcdhUtil', 'cn.hutool.core.collection.CollectionUtil', 'cn.hutool.core.util.StrUtil'] |
| Brief Description | The PrivateSetIntersection class implements multi-party ID intersection functionality, ensuring data privacy through encryption and batch processing, while supporting resumable transfers and result storage. |

# Description

The `PrivateSetIntersection` class inherits from `Psi` and implements multi-party intersection functionality. The `query` method accepts a list of server configurations and a local ID set, computing the intersection through iterative processing. The specific workflow includes: initializing the result set, iterating through server configurations, invoking single-server query methods, and progressively filtering the intersection.  

The single-server query method handles batch requests, encrypts client data using the DH-PSI protocol, sends requests to the server, processes responses, decrypts results, and stores batch outcomes. It supports resumable transfers, logging batch information and processing time. Ultimately, it returns the intersection results from all batches.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PrivateSetIntersection | class | The PrivateSetIntersection class implements multi-party private set intersection, ensuring data security through encryption and batch processing, supporting resumable transfers, and returning the intersection results. |



## Class PrivateSetIntersection

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PrivateSetIntersection |
| Description | The PrivateSetIntersection class implements multi-party private set intersection, ensuring data security through encryption and batch processing, supporting resumable transfers, and returning the intersection results. |


### UML Class Diagram

```mermaid
classDiagram
    class Psi {
        <<Interface>>
        +query(CommunicationConfig config, List~String~ clientIds, int currentBatch, int batchSize) List~String~
    }

    class PrivateSetIntersection {
        -clientDatasetMap Map~String, String~
        +query(List~CommunicationConfig~ configs, List~String~ ids) List~String~
        +query(CommunicationConfig config, List~String~ clientIds, int currentBatch, int batchSize) List~String~
        -saveLastCurrentBatchAndSize(String requestId, int currentBatch, int batchSize) void
        -savePsiResult(Set~String~ batchResult, String requestId) void
        -isContinue() boolean
        -readLastCurrentBatchAndSize(String requestId) int[]
    }

    class CommunicationConfig {
        -String serverUrl
        -String requestId
        +getServerUrl() String
        +getRequestId() String
    }

    class DhPsiClient {
        -Map~Long, String~ clientEncryptedDatasetMap
        +encryptClientOriginalDataset(List~String~ clientIds) Map~Long, String~
        +encryptServerDataset(List~String~ serverIds) void
        +setClientIdByServerKeys(Map~String, String~ clientIdByServerKeys) void
        +psi() Set~String~
    }

    class QueryPrivateSetIntersectionRequest {
        -String p
        -List~String~ clientIds
        -String requestId
        -int currentBatch
        -int batchSize
        -String type
        +setP(String p) void
        +setClientIds(List~String~ clientIds) void
        +setRequestId(String requestId) void
        +setCurrentBatch(int currentBatch) void
        +setBatchSize(int batchSize) void
        +setType(String type) void
        +getRequestId() String
        +getCurrentBatch() int
        +getBatchSize() int
    }

    class QueryPrivateSetIntersectionResponse {
        -int code
        -String message
        -boolean hasNext
        -List~String~ serverEncryptIds
        -List~String~ clientIdByServerKeys
        +getCode() int
        +getMessage() String
        +isHasNext() boolean
        +getServerEncryptIds() List~String~
        +getClientIdByServerKeys() List~String~
    }

    class PrivateSetIntersectionService {
        +handle(CommunicationConfig config, QueryPrivateSetIntersectionRequest request) QueryPrivateSetIntersectionResponse
    }

    PrivateSetIntersection --|> Psi : Implements
    PrivateSetIntersection --> CommunicationConfig : Uses
    PrivateSetIntersection --> DhPsiClient : Uses
    PrivateSetIntersection --> QueryPrivateSetIntersectionRequest : Creates
    PrivateSetIntersection --> QueryPrivateSetIntersectionResponse : Processes
    PrivateSetIntersection --> PrivateSetIntersectionService : Invokes
    DhPsiClient --> QueryPrivateSetIntersectionRequest : Depends on
    DhPsiClient --> QueryPrivateSetIntersectionResponse : Depends on
    PrivateSetIntersectionService --> QueryPrivateSetIntersectionRequest : Handles
    PrivateSetIntersectionService --> QueryPrivateSetIntersectionResponse : Returns
```

This code implements a multi-party Private Set Intersection (PSI) functionality, enabling secure computation of data intersections through the Diffie-Hellman key exchange protocol. The `PrivateSetIntersection` class inherits from the `Psi` interface and primarily includes two query methods: one for handling multi-party queries and another for single queries. During single queries, it creates a `DhPsiClient` to encrypt data and interacts with the server via `PrivateSetIntersectionService` to process batch queries and save intermediate results. The entire workflow involves encrypted dataset processing, server communication, and result consolidation, ensuring intersection computation of multi-party data without exposing raw data.


### Internal Method Call Graph

```mermaid
graph TD
    A["query(List<CommunicationConfig>, List<String>)"]
    B["Initialize result set result=ids"]
    C["Iterate through configs"]
    D["Call query(config, ids)"]
    E["Is result empty?"]
    F["Filter result: retain items with PSI matches"]
    G["Return result"]
    H["query(CommunicationConfig, List<String>, int, int)"]
    I["Check isContinue"]
    J["Read last batch info"]
    K["Parameter validation"]
    L["Create DhPsiClient"]
    M["Encrypt client data"]
    N["Build request object"]
    O["Send request to server"]
    P["Process response"]
    Q["Encrypt server data"]
    R["Calculate PSI result"]
    S["Save batch result"]
    T["Check hasNext"]
    U["Update request batch"]
    V["Process next batch iteratively"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --Yes--> G
    E --No--> F
    F --> C
    D -.-> H
    H --> I
    I --Yes--> J
    I --No--> K
    J --> K
    K --> L
    L --> M
    M --> N
    N --> O
    O --> P
    P --> Q
    Q --> R
    R --> S
    S --> T
    T --Yes--> U
    U --> O
    T --No--> H
```

The flowchart describes two core methods of the PrivateSetIntersection class. The main query method iterates through configuration lists, obtains PSI results by invoking another query method, and progressively filters them. The detailed query method handles individual PSI requests, including parameter validation, data encryption, request construction, server interaction, result decryption, and batch processing. The entire process implements multi-party private set intersection functionality, supports batch processing of large datasets, and maintains intermediate states.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| query | List<String> | The method receives a communication configuration list and an ID list, iterates through the configurations to query matching IDs one by one, and finally returns the intersection of IDs that match all configurations. If the result set becomes empty during the process, it terminates early. |
| query | List<String> | This method implements private set intersection queries based on the DH algorithm. The main workflow includes: validating parameters, encrypting client data, sending requests to the server, and processing response results. If subsequent batches exist, the process loops until completion. Finally, it returns the intersection results and saves batch information. |




