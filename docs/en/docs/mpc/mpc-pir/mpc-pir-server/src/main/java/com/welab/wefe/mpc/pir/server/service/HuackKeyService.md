# Basic Information

|      |      |
|------|------|
| Name | HuackKeyService |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir/mpc-pir-server/src/main/java/com/welab/wefe/mpc/pir/server/service/HuackKeyService.java |
| Package Name | com.welab.wefe.mpc.pir.server.service |
| Dependencies | ['cn.hutool.core.thread.ThreadUtil', 'com.welab.wefe.mpc.commom.Conversion', 'com.welab.wefe.mpc.pir.protocol.ot.hauck.HauckTarget', 'com.welab.wefe.mpc.pir.request.QueryKeysRequest', 'com.welab.wefe.mpc.pir.request.QueryKeysResponse', 'com.welab.wefe.mpc.pir.server.event.PrivateInformationRetrievalEvent', 'com.welab.wefe.mpc.pir.server.flow.PrivateInformationRetrievalFlowServer', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.UUID'] |
| Brief Description | The HuackKeyService class handles key query requests, generates a UUID, and verifies that the request ID is not empty. It processes the request through the PrivateInformationRetrievalFlowServer, records the time taken, and returns the response. |

# Description

The HuackKeyService class is a service class that handles key query requests. It contains two main methods: one generates a random UUID and invokes the other method, while the other method executes the specific processing logic. This method first verifies whether the request ID is empty, then creates a response object and sets the UUID and attempt count. Next, it initializes the PrivateInformationRetrievalFlowServer, retrieves the HauckTarget object, converts its S attribute to a string, and sets it in the response. Finally, it creates an asynchronous processing event, executes the key processing task via a thread pool, and logs the processing time. The entire process involves key operations such as UUID generation, parameter validation, server initialization, asynchronous task processing, and performance monitoring.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HuackKeyService | class | The HuackKeyService class handles key query requests, generates UUIDs, validates that the request ID is not empty, initializes the response and sets parameters, processes the request through the PrivateInformationRetrievalFlowServer, records the time consumed, and then returns the response. |



## Class HuackKeyService

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HuackKeyService |
| Description | The HuackKeyService class handles key query requests, generates UUIDs, validates that the request ID is not empty, initializes the response and sets parameters, processes the request through the PrivateInformationRetrievalFlowServer, records the time consumed, and then returns the response. |


### UML Class Diagram

```mermaid
classDiagram
    class HuackKeyService {
        -Logger LOG
        +QueryKeysResponse handle(QueryKeysRequest request) throws Exception
        +QueryKeysResponse handle(QueryKeysRequest request, String uuid) throws Exception
    }

    class QueryKeysRequest {
        +List~String~ getIds()
        +String getMethod()
    }

    class QueryKeysResponse {
        +setUuid(String uuid)
        +setAttemptCount(int count)
        +setS(String s)
    }

    class PrivateInformationRetrievalFlowServer {
        -String uuid
        +setUuid(String uuid)
        +mObliviousTransfer: ObliviousTransfer
    }

    class ObliviousTransfer {
        +HauckTarget getHauckTarget()
    }

    class HauckTarget {
        -GroupElement s
    }

    class Conversion {
        +groupElementToString(GroupElement element) String
    }

    class PrivateInformationRetrievalEvent {
        -String uuid
        -List~String~ keys
        -PrivateInformationRetrievalFlowServer server
        +getPrivateInformationRetrieval() PrivateInformationRetrieval
        +getKeys() List~String~
    }

    class PrivateInformationRetrieval {
        +process(List~String~ keys, String method)
    }

    class ThreadUtil {
        +execute(Runnable task)
    }

    HuackKeyService --> QueryKeysRequest : depends
    HuackKeyService --> QueryKeysResponse : creates
    HuackKeyService --> PrivateInformationRetrievalFlowServer : creates
    HuackKeyService --> Conversion : invokes
    HuackKeyService --> ThreadUtil : invokes
    PrivateInformationRetrievalFlowServer --> ObliviousTransfer : contains
    ObliviousTransfer --> HauckTarget : returns
    PrivateInformationRetrievalFlowServer --> PrivateInformationRetrievalEvent : creates
    PrivateInformationRetrievalEvent --> PrivateInformationRetrieval : associates
```

This class diagram illustrates the core structure and dependencies of HuackKeyService. The service processes QueryKeysRequest via handle methods to generate QueryKeysResponse, involving collaboration with components like PrivateInformationRetrievalFlowServer and ObliviousTransfer. The workflow includes key operations such as UUID generation, parameter validation, and asynchronous processing, ultimately executing core business logic through PrivateInformationRetrieval. Each component has clearly defined responsibilities, forming a complete processing chain through method invocations and data transfers.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class HuackKeyService"]
    B["Method: handle(QueryKeysRequest request)"]
    C["Generate UUID and remove hyphens"]
    D["Call overloaded method handle(request, uuid)"]
    E["Method: handle(QueryKeysRequest request, String uuid)"]
    F["Record start time 'start'"]
    G["Check if request.ids is empty"]
    H["Throw IllegalArgumentException"]
    I["Create QueryKeysResponse object"]
    J["Set response.uuid and attemptCount"]
    K["Create PrivateInformationRetrievalFlowServer instance"]
    L["Set server.uuid"]
    M["Get HauckTarget object"]
    N["Convert groupElement to string and set response.s"]
    O["Create PrivateInformationRetrievalEvent event"]
    P["Start new thread to process event"]
    Q["Log processing time"]
    R["Return response object"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G -- Yes --> H
    G -- No --> I
    I --> J
    J --> K
    K --> L
    L --> M
    M --> N
    N --> O
    O --> P
    P --> Q
    Q --> R
```

This code flowchart illustrates the invocation process of two main methods in the HuackKeyService class. The first handle method generates a UUID and then calls the second overloaded method, which first validates request parameters, creates a response object and initializes relevant attributes, then performs key processing through PrivateInformationRetrievalFlowServer, and finally asynchronously processes the event in a new thread before returning the response. The entire process includes key steps such as parameter validation, object initialization, service invocation, and asynchronous processing, demonstrating the complete workflow of the key query service.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(HuackKeyService.class) | Logger | The HuackKeyService class defines a static immutable logger LOG. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | QueryKeysResponse | This method processes the query key request, generates a random UUID with hyphens removed, invokes another processing method, and returns the response. |
| handle | QueryKeysResponse | Process the query request, verify that the ID is not empty, generate a response, initialize the private information retrieval service and set parameters, asynchronously handle the retrieval event, record the time consumption, and then return the response. |




