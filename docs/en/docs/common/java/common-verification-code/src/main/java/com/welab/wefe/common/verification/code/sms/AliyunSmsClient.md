# Basic Information

|      |      |
|------|------|
| Name | AliyunSmsClient |
| Language | .java |
| Code Path | WeFe/common/java/common-verification-code/src/main/java/com/welab/wefe/common/verification/code/sms/AliyunSmsClient.java |
| Package Name | com.welab.wefe.common.verification.code.sms |
| Dependencies | ['com.aliyun.dysmsapi20170525.Client', 'com.aliyun.dysmsapi20170525.models.SendSmsRequest', 'com.aliyun.dysmsapi20170525.models.SendSmsResponse', 'com.aliyun.teaopenapi.models.Config', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.verification.code.AbstractClient', 'com.welab.wefe.common.verification.code.AbstractResponse', 'java.util.HashMap', 'java.util.Map'] |
| Brief Description | Alibaba Cloud SMS client class, inherits from the abstract client, sends SMS verification codes by configuring keys, signatures, and templates. |

# Description

This is an Alibaba Cloud SMS service client class that inherits from an abstract client class. The class defines four static constants representing configuration parameter key names. The constructor accepts an extended parameter map. Its primary function is to send SMS messages via the send method, which requires a phone number and verification code as input. Internally, it configures the client using Alibaba Cloud SDK and constructs the request, including setting the signature, template code, and template parameters. It also provides a static utility method for building extended parameter maps, which encapsulates configuration information such as access keys, signatures, and template codes.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AliyunSmsClient | class | Alibaba Cloud SMS client class, inherits from the abstract client, includes SMS sending methods, requires configuration of keys, signatures, and template codes. |



## Class AliyunSmsClient

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AliyunSmsClient |
| Description | Alibaba Cloud SMS client class, inherits from the abstract client, includes SMS sending methods, requires configuration of keys, signatures, and template codes. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractClient {
        <<Abstract>>
        +AbstractClient(Map~String, Object~ extendParams)
        +AbstractResponse send(String mobile, String verificationCode) throws Exception
        #Map~String, Object~ getExtendParams()
    }

    class AliyunSmsClient {
        +String ACCESS_KEY_ID
        +String ACCESS_KEY_SECRET
        +String SIGN_NAME
        +String TEMPLATE_CODE
        +AliyunSmsClient(Map~String, Object~ extendParams)
        +AbstractResponse send(String mobile, String verificationCode) throws Exception
        +static Map~String, Object~ buildExtendParams(String accessKeyId, String accessKeySecret, String signName, String templateCode)
    }

    class Config {
        +String endpoint
        +Config setAccessKeyId(String accessKeyId)
        +Config setAccessKeySecret(String accessKeySecret)
    }

    class Client {
        +Client(Config config)
        +SendSmsResponse sendSms(SendSmsRequest sendSmsRequest)
    }

    class SendSmsRequest {
        +setPhoneNumbers(String phoneNumbers)
        +setSignName(String signName)
        +setTemplateCode(String templateCode)
        +setTemplateParam(String templateParam)
    }

    class SendSmsResponse {
        // Alibaba Cloud SMS sending response
    }

    class AliyunSmsResponse {
        +AliyunSmsResponse(SendSmsResponse sendSmsResponse)
    }

    class JObject {
        <<Utility>>
        +static JObject create(Map~String, Object~ map)
        +static JObject create(String key, String value)
        +String getString(String key)
        +String toString()
    }

    AbstractClient <|-- AliyunSmsClient
    AliyunSmsClient --> Config : Create config
    AliyunSmsClient --> Client : Send SMS
    AliyunSmsClient --> SendSmsRequest : Build request
    AliyunSmsClient --> JObject : Parameter processing
    Client --> SendSmsResponse : Return response
    AliyunSmsClient --> AliyunSmsResponse : Wrap response
```

This class diagram illustrates the core structure of the Alibaba Cloud SMS client. AliyunSmsClient inherits from AbstractClient, configures client information through Config, and uses Client to send SMS requests. The process involves parameter processing (JObject), request construction (SendSmsRequest), and response wrapping (AliyunSmsResponse), fully implementing the SMS sending functionality. Each component has clear responsibilities, achieving high cohesion and low coupling design goals through composition.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class AliyunSmsClient"]
    B["Constant: ACCESS_KEY_ID"]
    C["Constant: ACCESS_KEY_SECRET"]
    D["Constant: SIGN_NAME"]
    E["Constant: TEMPLATE_CODE"]
    F["Constructor: AliyunSmsClient(Map<String, Object>)"]
    G["Method: send(String mobile, String verificationCode)"]
    H["Method: buildExtendParams(String accessKeyId, String accessKeySecret, String signName, String templateCode)"]
    I["Step: Create JObject extendParams"]
    J["Step: Initialize Config object"]
    K["Step: Set config.endpoint"]
    L["Step: Create Client instance"]
    M["Step: Create SendSmsRequest object"]
    N["Step: Set request parameters"]
    O["Step: Invoke client.sendSms"]
    P["Step: Return AliyunSmsResponse"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    G --> I
    G --> J
    G --> K
    G --> L
    G --> M
    G --> N
    G --> O
    G --> P
```

This flowchart illustrates the core structure and workflow of the Aliyun SMS client class. The class contains 4 constant fields, 1 constructor, and 2 main methods. The send method's process details the complete SMS sending procedure from parameter processing to final response, including key steps such as configuration initialization, request construction, and API invocation. The buildExtendParams method is used to construct an extended parameter dictionary, providing necessary parameters for client initialization. The overall design demonstrates encapsulation and simplified invocation of the Aliyun SMS API.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| TEMPLATE_CODE = "templateCode" | String | Defined a public static immutable string constant TEMPLATE_CODE with the value "templateCode". |
| ACCESS_KEY_SECRET = "accessKeySecret" | String | Defined an immutable static string constant ACCESS_KEY_SECRET with the value "accessKeySecret". |
| SIGN_NAME = "signName" | String | Defined a public static constant string SIGN_NAME with the value "signName". |
| ACCESS_KEY_ID = "accessKeyId" | String | Define a constant string ACCESS_KEY_ID with the value "accessKeyId". |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| send | AbstractResponse | This method sends verification codes via Alibaba Cloud SMS service by configuring keys, signatures, and templates, then calling the API to send SMS messages and return responses. |
| buildExtendParams | Map<String, Object> | Build an extended parameter Map containing the key ID, key, signature, and template code. |




