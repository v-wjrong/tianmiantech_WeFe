# 基础信息

|      |      |
|------|------|
| 名称 | MultiPsiServiceProcessor |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service_processor/MultiPsiServiceProcessor.java |
| 包名 | com.welab.wefe.serving.service.service_processor |
| 依赖项 | ['java.util.ArrayList', 'java.util.LinkedList', 'java.util.List', 'java.util.stream.Collectors', 'org.apache.commons.collections.CollectionUtils', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.mpc.config.CommunicationConfig', 'com.welab.wefe.mpc.psi.sdk.Psi', 'com.welab.wefe.mpc.psi.sdk.PsiFactory', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.entity.TableServiceMySqlModel', 'com.welab.wefe.serving.service.service.ClientServiceService'] |
| 概述说明 | MultiPsiServiceProcessor类处理客户端ID和服务配置，验证服务激活状态并生成通信配置，通过PSI查询过滤结果并记录调用日志，最终返回匹配的客户端ID列表。 |

# 说明

MultiPsiServiceProcessor类继承AbstractServiceProcessor，处理TableServiceMySqlModel数据。通过clientServiceService获取激活的客户端服务，构建CommunicationConfig配置列表。解析输入数据中的client_ids，遍历服务配置，验证URL有效性并设置通信参数。使用PsiFactory生成Psi实例，对每个配置执行查询，逐步过滤客户端ID列表。最后记录调用日志并返回结果列表。主要涉及服务配置验证、通信参数设置和PSI查询处理。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MultiPsiServiceProcessor | class | MultiPsiServiceProcessor类处理多PSI服务请求，解析客户端ID和服务配置，验证服务激活状态，生成通信配置并执行PSI查询，返回结果并记录调用日志。 |



## 类 MultiPsiServiceProcessor

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MultiPsiServiceProcessor |
| 说明 | MultiPsiServiceProcessor类处理多PSI服务请求，解析客户端ID和服务配置，验证服务激活状态，生成通信配置并执行PSI查询，返回结果并记录调用日志。 |


### UML类图

```mermaid
classDiagram
    class AbstractServiceProcessor~T~ {
        <<Abstract>>
        +process(JObject data, T model) JObject
    }

    class MultiPsiServiceProcessor {
        -ClientServiceService clientServiceService
        +process(JObject data, TableServiceMySqlModel model) JObject
    }

    class ClientServiceService {
        +findActivateClientServiceByUrl(String url) ClientServiceMysqlModel
    }

    class TableServiceMySqlModel {
        +String serviceConfig
    }

    class ClientServiceMysqlModel {
        +String code
        +String privateKey
        +SecretKeyType secretKeyType
    }

    class CommunicationConfig {
        +String apiName
        +String serverUrl
        +String commercialId
        +String signPrivateKey
        +String secretKeyType
        +String requestId
    }

    class Psi {
        +query(CommunicationConfig config, List~String~ clientIds) List~String~
    }

    class PsiFactory {
        <<Static>>
        +generatePsi() Psi
    }

    AbstractServiceProcessor <|-- MultiPsiServiceProcessor
    MultiPsiServiceProcessor --> ClientServiceService : 依赖
    MultiPsiServiceProcessor --> TableServiceMySqlModel : 处理
    MultiPsiServiceProcessor --> CommunicationConfig : 创建
    MultiPsiServiceProcessor --> Psi : 调用
    ClientServiceService --> ClientServiceMysqlModel : 返回
    PsiFactory --> Psi : 创建实例
```

这段代码展示了一个多PSI服务处理器，继承自抽象服务处理器，主要处理客户端ID和服务配置的匹配逻辑。通过ClientServiceService获取激活的客户端服务模型，构建通信配置对象，利用PSI工厂生成的PSI实例进行查询，最终返回匹配结果。涉及6个核心类和1个接口，展现了从配置解析到服务调用的完整流程。


### 内部方法调用关系图

```mermaid
graph TD
    A["MultiPsiServiceProcessor类"]
    B["属性: ClientServiceService clientServiceService"]
    C["方法: process(JObject data, TableServiceMySqlModel model)"]
    D["获取clientIds: 从data['client_ids']或data['clientIds']"]
    E["解析model.serviceConfig为JSONArray"]
    F["遍历serviceConfigs创建CommunicationConfig列表"]
    G["校验服务是否激活: clientServiceService.findActivateClientServiceByUrl"]
    H["构建CommunicationConfig并添加到列表"]
    I["初始化结果列表result=clientIds"]
    J["使用PsiFactory.generatePsi生成psi实例"]
    K["遍历communicationConfigs执行psi.query过滤结果"]
    L["记录调用日志addCalllog"]
    M["返回JObject包装的result"]

    A --> B
    A --> C
    C --> D
    C --> E
    C --> F
    F --> G
    G -->|否| H
    G -->|是| H
    C --> I
    C --> J
    C --> K
    K --> L
    C --> M
```

```mermaid
sequenceDiagram
    participant Client
    participant MultiPsiServiceProcessor
    participant ClientServiceService
    participant PsiFactory
    participant Psi

    Client->>MultiPsiServiceProcessor: process(data, model)
    MultiPsiServiceProcessor->>MultiPsiServiceProcessor: 解析clientIds
    MultiPsiServiceProcessor->>MultiPsiServiceProcessor: 解析serviceConfigs
    loop 遍历serviceConfigs
        MultiPsiServiceProcessor->>ClientServiceService: findActivateClientServiceByUrl
        ClientServiceService-->>MultiPsiServiceProcessor: activateModel
        MultiPsiServiceProcessor->>MultiPsiServiceProcessor: 构建CommunicationConfig
    end
    MultiPsiServiceProcessor->>PsiFactory: generatePsi()
    PsiFactory-->>MultiPsiServiceProcessor: psi实例
    loop 遍历communicationConfigs
        MultiPsiServiceProcessor->>Psi: query(config, clientIds)
        Psi-->>MultiPsiServiceProcessor: psiResult
        MultiPsiServiceProcessor->>MultiPsiServiceProcessor: 过滤结果并记录日志
    end
    MultiPsiServiceProcessor-->>Client: 返回JObject(result)
```

这段代码实现了一个多PSI服务处理器，主要功能是通过配置的服务信息对客户端ID列表进行隐私集合求交(PSI)处理。流程图展示了从初始化配置、服务验证到PSI查询过滤的全过程，时序图则详细描述了类间交互。处理器会先解析输入参数，验证每个通信配置的有效性，然后使用PSI算法逐步过滤客户端ID列表，最终返回交集结果并记录调用日志。整个过程包含异常处理和服务状态验证等关键环节。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clientServiceService = Launcher.getBean(ClientServiceService.class) | ClientServiceService | 从Launcher获取ClientServiceService实例并赋值给私有常量clientServiceService。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| process | JObject | 处理客户端ID和服务配置，验证服务激活状态，生成通信配置并查询PSI结果，返回过滤后的客户端ID列表。 |




