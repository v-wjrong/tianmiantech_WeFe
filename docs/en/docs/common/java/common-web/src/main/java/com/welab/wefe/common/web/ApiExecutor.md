# Basic Information

|      |      |
|------|------|
| Name | ApiExecutor |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/ApiExecutor.java |
| Package Name | com.welab.wefe.common.web |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.SamplingLogger', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.FlowLimitByIp', 'com.welab.wefe.common.web.api.base.FlowLimitByMobile', 'com.welab.wefe.common.web.dto.ApiResult', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.slf4j.MDC', 'org.springframework.beans.BeansException', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'javax.servlet.http.HttpServletRequest', 'java.util.Map', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description | The ApiExecutor class implements API execution logic, including functions such as permission checks, traffic control, and logging, processing requests and returning results. |

# Description

The `ApiExecutor` class is a core handler for processing API requests, incorporating functionalities such as logging, permission checks, and traffic control. It dynamically locates and executes corresponding API implementation classes through reflection, supporting request parameter parsing, pre/post-processing hooks, exception handling, and response logging. The class implements IP and mobile number-based traffic control checks and provides a flexible log sampling mechanism to reduce disk usage. The execution process includes API path matching, permission validation, traffic control, business logic execution, and result processing, ultimately returning an `ApiResult` object containing metrics like execution time.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ApiExecutor | class | The ApiExecutor class handles API requests, including API lookup, permission checks, rate limiting, API execution, and logging. It supports pre- and post-operations, and the returned results include execution time and status. |



## Class ApiExecutor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ApiExecutor |
| Description | The ApiExecutor class handles API requests, including API lookup, permission checks, rate limiting, API execution, and logging. It supports pre- and post-operations, and the returned results include execution time and status. |


### UML Class Diagram

```mermaid
classDiagram
    class ApiExecutor {
        -Logger LOG
        -SamplingLogger SLOG
        -String REQUEST_FROM_REFRESH
        -Map~String, Long~ API_LOG_TIME_MAP
        +execute(HttpServletRequest, long, String, JSONObject, MultiValueMap~String, MultipartFile~) ApiResult~?~
        -logResponse(Api, ApiResult~?~) void
        -checkApiPermission(HttpServletRequest, Api, JSONObject) void
        -checkSessionToken(AbstractApi~?, ?~, Api) void
        -checkFlowLimitByIp(HttpServletRequest, AbstractApi~?, ?~, JSONObject) void
        -checkFlowLimitByMobile(HttpServletRequest, AbstractApi~?, ?~, JSONObject) void
    }

    class AbstractApi~T, R~ {
        <<Abstract>>
        +execute(String, JSONObject, HttpServletRequest, MultiValueMap~String, MultipartFile~) ApiResult~R~
        +fail(int, String) ApiResult~R~
    }

    class Api {
        <<Annotation>>
        +path() String
        +forward() boolean
        +logLevel() String
        +logSaplingInterval() long
        +login() boolean
    }

    class Launcher {
        <<Singleton>>
        +CONTEXT: ApplicationContext
        +BEFORE_API_EXECUTE_FUNCTION: ApiExecuteFunction
        +AFTER_API_EXECUTE_FUNCTION: ApiExecuteAfterFunction
        +API_LOGGER: ApiLogger
        +API_PERMISSION_POLICY: ApiPermissionPolicy
        +CHECK_SESSION_TOKEN_FUNCTION: CheckSessionTokenFunction
        +FLOW_LIMIT_BY_IP_FUNCTION: FlowLimitByIpFunction
        +FLOW_LIMIT_BY_MOBILE_FUNCTION: FlowLimitByMobileFunction
    }

    class ApiResult~T~ {
        +spend: long
        +ofErrorWithStatusCode(StatusCode, String) ApiResult~?~
        +toLogString(boolean) String
    }

    class StatusCode {
        <<Enumeration>>
        +REQUEST_API_NOT_FOUND
        +SYSTEM_ERROR
        +LOGIN_REQUIRED
        +getCode() int
    }

    ApiExecutor --> AbstractApi : Invokes execution
    ApiExecutor --> Api : Reads annotation config
    ApiExecutor --> Launcher : Depends on components
    ApiExecutor --> ApiResult : Generates response
    AbstractApi ..|> Api : Implements annotation
    Launcher --> ApiExecuteFunction : Contains pre-function
    Launcher --> ApiExecuteAfterFunction : Contains post-function
    Launcher --> ApiLogger : Contains logger
    Launcher --> ApiPermissionPolicy : Contains permission policy
    Launcher --> CheckSessionTokenFunction : Contains session check
    Launcher --> FlowLimitByIpFunction : Contains IP flow control
    Launcher --> FlowLimitByMobileFunction : Contains mobile flow control
```

This code demonstrates the core structure of an API executor, primarily consisting of the ApiExecutor class and its dependencies. The ApiExecutor retrieves concrete API implementations (AbstractApi) through the Spring context, performs permission checks, flow control, and other operations before and after execution, and integrates various configurable extension features via the Launcher class. The class diagram clearly illustrates the collaboration between components, including key functional modules such as annotation configuration reading, execution flow control, exception handling, and logging, reflecting a highly extensible API gateway design pattern.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class ApiExecutor"]
    B["Static Property: Logger LOG"]
    C["Static Property: SamplingLogger SLOG"]
    D["Static Initialization Block: SLOG Initialization"]
    E["Constant: REQUEST_FROM_REFRESH"]
    F["Main Method: execute"]
    G["Helper Method: logResponse"]
    H["Helper Method: checkApiPermission"]
    I["Helper Method: checkSessionToken"]
    J["Helper Method: checkFlowLimitByIp"]
    K["Helper Method: checkFlowLimitByMobile"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    F --> G
    F --> H
    F --> I
    F --> J
    F --> K
    G -->|Calls| B
    H -->|Calls| C
    J -->|Calls| C
    K -->|Calls| C
```

```mermaid
sequenceDiagram
    participant Client
    participant ApiExecutor
    participant AbstractApi
    participant Launcher
    participant Logger

    Client->>ApiExecutor: execute(request, start, apiName, params, files)
    ApiExecutor->>ApiExecutor: MDC.put('requestId')
    loop Find API Implementation
        ApiExecutor->>Launcher: getBean(apiPath)
        alt Bean Exists
            Launcher-->>ApiExecutor: Returns AbstractApi Instance
        else Bean Not Found
            ApiExecutor->>ApiExecutor: Adjust apiPath
        end
    end
    alt API Not Found
        ApiExecutor-->>Client: Returns 404 Error
    else API Found
        ApiExecutor->>AbstractApi: Get @Api Annotation
        ApiExecutor->>Logger: Log Request
        ApiExecutor->>ApiExecutor: checkApiPermission()
        ApiExecutor->>ApiExecutor: checkFlowLimitByIp()
        ApiExecutor->>ApiExecutor: checkFlowLimitByMobile()
        ApiExecutor->>Launcher: Execute BEFORE_API_EXECUTE_FUNCTION
        ApiExecutor->>AbstractApi: execute()
        alt Execution Success
            AbstractApi-->>ApiExecutor: Returns ApiResult
        else Exception Occurs
            ApiExecutor->>AbstractApi: Generate Error Result
        end
        ApiExecutor->>Launcher: Execute AFTER_API_EXECUTE_FUNCTION
        ApiExecutor->>Launcher: Execute API_LOGGER
        ApiExecutor->>ApiExecutor: logResponse()
        ApiExecutor->>Logger: Log Response
        ApiExecutor->>ApiExecutor: MDC.clear()
        ApiExecutor-->>Client: Returns ApiResult
    end
```

This code demonstrates the complete workflow of an API executor, handling HTTP request parsing, permission validation, flow control, business logic execution, and response logging. The flowchart clearly illustrates the class structure and method invocation relationships, while the sequence diagram details the end-to-end processing from client request to response return, including exception handling and post-execution operations. The design features robust logging, permission control, and rate-limiting mechanisms, showcasing solid API gateway capabilities.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(ApiExecutor.class) | Logger | Define the static constant LOG in the ApiExecutor class for logging purposes. |
| REQUEST_FROM_REFRESH = "request-from-refresh" | String | Static constant string REQUEST_FROM_REFRESH with the value "request-from-refresh". |
| SLOG | SamplingLogger | Protected static constant sampling logger SLOG. |
| API_LOG_TIME_MAP = new ConcurrentHashMap<>() | Map<String, Long> | The private static constant API_LOG_TIME_MAP uses a thread-safe ConcurrentHashMap to store mappings from strings to long integers. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| checkSessionToken | void | Check session token validity: Skip interfaces that do not require login; Do not execute if no check method is set; Comments show the original check logic (not enabled). |
| checkFlowLimitByIp | void | Check IP traffic limit: Skip if no limit function is set or the annotation is invalid; otherwise, call the limit check function. |
| logResponse | void | This method controls the frequency of API response log printing based on annotation configuration to avoid frequent logging. It determines whether to omit logs through time interval checks, reducing disk usage. Finally, it outputs the response content according to the log level, limiting length to prevent excessive size. |
| execute | ApiResult<?> | This method handles API requests: locates the corresponding interface, checks permissions and rate limits, allows custom operations before and after execution, logs the process, and returns the result. Error messages are returned in case of exceptions. |
| checkApiPermission | void | Check API permissions: Skip if no permission policy is set, otherwise invoke the policy check method. |
| checkFlowLimitByMobile | void | Check the mobile number data usage restriction feature; skip if it is not enabled or the parameters are invalid, otherwise perform the restriction check. |




