# 基础信息

|      |      |
|------|------|
| 名称 | UploadFileSyncToUnionTask |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/task/UploadFileSyncToUnionTask.java |
| 包名 | com.welab.wefe.union.service.task |
| 依赖项 | ['com.alibaba.fastjson.JSONException', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.http.HttpContentType', 'com.welab.wefe.common.http.HttpRequest', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.SM2Util', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.union.service.cache.UnionNodeConfigCache', 'org.apache.http.entity.ContentType', 'org.apache.http.entity.mime.content.InputStreamBody', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'java.io.IOException', 'java.util.Map'] |
| 概述说明 | UploadFileSyncToUnionTask是线程类，用于上传文件到联盟节点。包含重试机制，每次请求间隔递增。使用SM2签名，支持多部分表单数据上传，验证响应状态码和JSON结果。失败时记录错误并重试。 |

# 说明

UploadFileSyncToUnionTask是一个继承Thread的类，用于同步上传文件到联盟节点。它包含baseUrl、api、params和fileStreamBodyMap等属性，通过构造函数初始化。在run方法中，任务会尝试最多3次上传操作，每次失败后等待递增的间隔时间。上传过程包括生成SM2签名、构建包含数据和签名的请求体、设置multipart内容类型、添加文件流参数，并发送POST请求。若响应失败或返回码非0，会记录错误并重试；成功则终止循环。整个过程通过日志记录错误信息。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UploadFileSyncToUnionTask | class | 上传文件同步任务类，包含重试机制，使用SM2签名，发送多部分HTTP请求，处理响应和错误。 |



## 类 UploadFileSyncToUnionTask

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | UploadFileSyncToUnionTask |
| 说明 | 上传文件同步任务类，包含重试机制，使用SM2签名，发送多部分HTTP请求，处理响应和错误。 |


### UML类图

```mermaid
classDiagram
    class UploadFileSyncToUnionTask {
        -Logger LOG
        -String baseUrl
        -String api
        -JObject params
        -Map~String, InputStreamBody~ fileStreamBodyMap
        +UploadFileSyncToUnionTask(String baseUrl, String api, JObject params, Map~String, InputStreamBody~ fileStreamBodyMap)
        +void run()
    }

    class JObject {
        +String toJSONString()
        +void append(String key, String value)
        +static JObject create()
    }

    class InputStreamBody

    class SM2Util {
        +static String sign(String data, String privateKey)
    }

    class UnionNodeConfigCache {
        +static String getSm2PrivateKey()
        +static String currentBlockchainNodeId
    }

    class HttpRequest {
        +static HttpRequest create(String url)
        +HttpRequest setContentType(String contentType)
        +void appendParameters(JObject params)
        +void appendParameter(String key, InputStreamBody value)
        +HttpResponse post()
    }

    class HttpResponse {
        +boolean success()
        +String getMessage()
        +JSONObject getBodyAsJson()
    }

    class ThreadUtil {
        +static void sleep(long millis)
    }

    UploadFileSyncToUnionTask --> JObject : 使用
    UploadFileSyncToUnionTask --> InputStreamBody : 使用
    UploadFileSyncToUnionTask --> SM2Util : 调用签名方法
    UploadFileSyncToUnionTask --> UnionNodeConfigCache : 获取配置
    UploadFileSyncToUnionTask --> HttpRequest : 构造请求
    UploadFileSyncToUnionTask --> HttpResponse : 处理响应
    UploadFileSyncToUnionTask --> ThreadUtil : 重试等待
    HttpRequest --> HttpResponse : 生成
```

类图描述：该图展示了UploadFileSyncToUnionTask线程类的结构及其依赖关系。该类负责文件同步上传任务，包含基础URL、API路径、参数和文件流等私有成员。通过SM2Util进行数据签名，使用HttpRequest构建多部分请求，并处理HttpResponse结果。依赖JObject处理JSON数据，通过UnionNodeConfigCache获取配置信息，利用ThreadUtil实现重试机制。整体呈现了文件上传任务的核心协作关系。


### 内部方法调用关系图

```mermaid
graph TD
    A["类UploadFileSyncToUnionTask"]
    B["属性: Logger LOG"]
    C["属性: String baseUrl"]
    D["属性: String api"]
    E["属性: JObject params"]
    F["属性: Map<String, InputStreamBody> fileStreamBodyMap"]
    G["构造方法: UploadFileSyncToUnionTask(...)"]
    H["重写方法: run()"]
    I["循环3次尝试"]
    J["计算重试间隔retryInterval"]
    K["拼接URL: baseUrl + '/' + api"]
    L["生成JSON字符串: params.toJSONString()"]
    M["SM2签名: SM2Util.sign()"]
    N["构建请求体: JObject.create()"]
    O["设置请求头: HttpRequest.create().setContentType()"]
    P["添加参数: request.appendParameters()"]
    Q["添加文件流: request.appendParameter()"]
    R["发送请求: request.post()"]
    S["检查响应: response.success()"]
    T["解析JSON响应: response.getBodyAsJson()"]
    U["验证状态码: json.getInteger('code')"]
    V["成功则退出循环"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    H --> I
    I --> J
    I --> K
    I --> L
    I --> M
    I --> N
    I --> O
    I --> P
    I --> Q
    I --> R
    I --> S
    S -- 失败 --> J
    S -- 成功 --> T
    T -- 异常 --> J
    T -- 正常 --> U
    U -- 非0 --> J
    U -- 0 --> V
```

这段代码实现了一个多线程文件上传任务，通过3次重试机制将文件同步到联盟节点。流程包括：初始化请求参数、生成SM2签名、构建多部分表单请求、添加文件流、发送POST请求，并对响应进行多层校验（网络状态、JSON解析、业务状态码）。每次失败后会按递增间隔（300*i毫秒）休眠后重试，直到成功或达到最大重试次数。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| fileStreamBodyMap | Map<String, InputStreamBody> | 定义了一个私有Map变量fileStreamBodyMap，键为String类型，值为InputStreamBody类型。 |
| api | String | 声明一个私有字符串变量api。 |
| baseUrl | String | 声明一个私有字符串变量baseUrl。 |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger | 定义当前类的日志记录器实例，用于输出日志信息。 |
| params | JObject | 私有JObject类型参数params。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| run | void | 代码实现重试机制，循环3次发送HTTP请求。每次生成签名，构建请求体并上传文件流。失败时记录错误并延迟重试，成功或达到重试次数后结束。 |




