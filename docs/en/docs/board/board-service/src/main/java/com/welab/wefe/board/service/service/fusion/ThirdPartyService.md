# Basic Information

|      |      |
|------|------|
| Name | ThirdPartyService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/fusion/ThirdPartyService.java |
| Package Name | com.welab.wefe.board.service.service.fusion |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.project.fusion.task.AuditCallbackApi', 'com.welab.wefe.board.service.api.project.fusion.task.DeleteCallbackApi', 'com.welab.wefe.board.service.api.project.fusion.task.ReceiveApi', 'com.welab.wefe.board.service.database.entity.fusion.FusionTaskMySqlModel', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.GatewayService', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.fusion.core.enums.CallbackType', 'com.welab.wefe.fusion.core.enums.PSIActuatorRole', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service'] |
| Brief Description | The ThirdPartyService class provides request alignment, task deletion, and callback functionalities. It invokes other member interfaces through gatewayService to handle task parameters and status. |

# Description

ThirdPartyService is a service class that interacts with other member boards through GatewayService. Its main functionalities include the alignApply method, which aligns requests by constructing a JSON object containing parameters such as project ID, member ID, business ID, name, PSI execution role, algorithm, description, and data resource information, and then sending the request. The delete method is used to delete tasks by constructing a JSON object with the business ID and sending the request. The callback method has three overloaded versions for handling callback requests, with parameters including target member ID, business ID, approval status, approval comments, hash function, URL, callback type, and data count, among others. It constructs the corresponding JSON object and sends the request. The internal request method encapsulates the logic for calling other member boards, ensuring consistent parameter order to avoid validation failures.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ThirdPartyService | class | The ThirdPartyService class provides request alignment and callback functionalities, including alignApply, delete, and multiple callback methods. It invokes interfaces of other members via gatewayService to handle task parameters and status. |



## Class ThirdPartyService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ThirdPartyService |
| Description | The ThirdPartyService class provides request alignment and callback functionalities, including alignApply, delete, and multiple callback methods. It invokes interfaces of other members via gatewayService to handle task parameters and status. |


### UML Class Diagram

```mermaid
classDiagram
    class ThirdPartyService {
        -GatewayService gatewayService
        +alignApply(FusionTaskMySqlModel task) void
        +delete(FusionTaskMySqlModel task) void
        +callback(String dstMemberId, String businessId, AuditStatus auditStatus, String auditComment) void
        +callback(String dstMemberId, String businessId, AuditStatus auditStatus, String auditComment, String hashFunction) void
        +callback(String url, String businessId, CallbackType callbackType, Integer dataCount) void
        -request(String dstMemberId, Class<?> api, JSONObject params) JSONObject
    }

    class GatewayService {
        <<Interface>>
        +callOtherMemberBoard(String dstMemberId, Class<?> api, JSONObject params, Class~T~ clazz) JSONObject
    }

    class FusionTaskMySqlModel {
        +String getProjectId()
        +String getBusinessId()
        +String getName()
        +PSIActuatorRole getPsiActuatorRole()
        +String getAlgorithm()
        +String getDescription()
        +String getPartnerDataResourceId()
        +String getPartnerDataResourceType()
        +String getDataResourceId()
        +String getDataResourceType()
        +int getRowCount()
        +String getHashFunction()
        +String getDstMemberId()
    }

    class JObject {
        +static JObject create()
        +JObject put(String key, Object value) JObject
    }

    ThirdPartyService --> GatewayService : depends
    ThirdPartyService --> FusionTaskMySqlModel : uses
    ThirdPartyService --> JObject : uses
```

This code describes a third-party service class `ThirdPartyService` that interacts with external systems through the `GatewayService` interface, primarily handling three types of callback operations: alignment application (`alignApply`), task deletion (`delete`), and status callbacks (`callback`). The class uses `FusionTaskMySqlModel` as its data model and constructs request parameters via `JObject`. The core private method `request` uniformly processes gateway calls, ensuring parameter order consistency. The overall design encapsulates business logic related to the PSI (Private Set Intersection) protocol, providing flexible callback interfaces through method overloading.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class ThirdPartyService"]
    B["Property: GatewayService gatewayService"]
    C["Method: alignApply(FusionTaskMySqlModel task)"]
    D["Method: delete(FusionTaskMySqlModel task)"]
    E["Method: callback(String dstMemberId, String businessId, AuditStatus auditStatus, String auditComment)"]
    F["Method: callback(String dstMemberId, String businessId, AuditStatus auditStatus, String auditComment, String hashFunction)"]
    G["Method: callback(String url, String businessId, CallbackType callbackType, Integer dataCount)"]
    H["Private Method: request(String dstMemberId, Class<?> api, JSONObject params)"]
    I["Invocation: gatewayService.callOtherMemberBoard"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    H --> I
    C --> H
    D --> H
    E --> F
    F --> H
    G -.->|Annotation Method| H
```

```mermaid
sequenceDiagram
    participant A as ThirdPartyService
    participant B as GatewayService
    participant C as FusionTaskMySqlModel

    A->>C: Retrieve task parameters
    A->>A: Create JSONObject params
    A->>B: callOtherMemberBoard(dstMemberId, api, params)
    B-->>A: Return JSONObject result
```

This flowchart illustrates the structure and method invocation relationships of the ThirdPartyService class, containing 6 public methods and 1 private method. The core private method request() is invoked by alignApply(), delete(), and overloaded callback() methods, ultimately achieving cross-member communication through gatewayService.callOtherMemberBoard. The sequence diagram specifically depicts the execution flow of the alignApply() method: retrieving parameters from the task object, constructing the request parameter object, initiating remote calls via the gateway service, and returning results. The class design employs the Facade pattern to encapsulate various third-party service callback operations.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| gatewayService | GatewayService | Automatically inject the GatewayService instance. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| callback | void | The method implements an audit callback function, which receives the target member ID, business ID, audit status, audit comments, and hash function parameters, constructs a JSON request, and invokes the audit callback API. |
| callback | void | Java callback method that accepts target member ID, business ID, review status, and review comment parameters, may throw exceptions, internally calls an overloaded method and passes null values. |
| callback | void | Define callback methods to receive URL, business ID, callback type, and data volume parameters, construct a JSON object, and comment out the code for requesting third-party callbacks. |
| request | JSONObject | The private method `request` invokes other member boards via `gatewayService`, passing in the target member ID, API class, and ordered parameters, and returns a `JSONObject`. It may throw a `StatusCodeWithException` exception. |
| alignApply | void | This method is used to handle task alignment requests, constructing a JSON object containing parameters such as project ID, member ID, and business ID. It adjusts the PSI execution role based on the task role and finally sends the request to the target member. |
| delete | void | This method deletes a specified task by constructing parameters with the business ID and sending a deletion callback request to the target member ID. |




