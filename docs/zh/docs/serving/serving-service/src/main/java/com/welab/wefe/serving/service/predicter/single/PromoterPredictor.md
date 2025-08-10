# 基础信息

|      |      |
|------|------|
| 名称 | PromoterPredictor |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/predicter/single/PromoterPredictor.java |
| 包名 | com.welab.wefe.serving.service.predicter.single |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.sdk.dto.ProviderParams', 'com.welab.wefe.serving.sdk.model.BaseModel', 'com.welab.wefe.serving.sdk.model.FeatureDataModel', 'com.welab.wefe.serving.sdk.predicter.single.AbstractSinglePredictor', 'com.welab.wefe.serving.service.manager.FeatureManager', 'com.welab.wefe.serving.service.manager.ModelManager', 'com.welab.wefe.serving.service.service.ClientServiceService', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.collections4.MapUtils', 'java.util.ArrayList', 'java.util.List', 'java.util.Map'] |
| 概述说明 | PromoterPredictor类继承AbstractSinglePredictor，实现纵向联邦预测功能。包含requestId初始化、获取模型参数、调用协作方计算联邦结果及查询特征数据方法。关键点：联邦结果聚合、异常处理及特征数据管理。 |

# 说明

PromoterPredictor类继承自AbstractSinglePredictor，用于实现预测功能。构造函数接收requestId、modelId、userId和featureData参数。类中包含三个主要方法：getModel用于获取模型参数；federatedResultByProviders通过调用协作方服务获取联邦预测结果，若协作方列表为空则抛出异常；findFeatureData用于查找特征数据，优先使用predictParams中的特征数据，若不存在则从FeatureManager获取。该类涉及模型管理、协作方调用和特征数据处理等功能。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PromoterPredictor | class | PromoterPredictor类继承AbstractSinglePredictor，实现纵向联邦预测功能，包含请求ID处理、模型获取、协作方结果聚合及特征数据查询方法。 |



## 类 PromoterPredictor

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PromoterPredictor |
| 说明 | PromoterPredictor类继承AbstractSinglePredictor，实现纵向联邦预测功能，包含请求ID处理、模型获取、协作方结果聚合及特征数据查询方法。 |


### UML类图

```mermaid
classDiagram
    class AbstractSinglePredictor {
        <<Abstract>>
        #String modelId
        #String userId
        #Map~String, Object~ featureData
        +AbstractSinglePredictor(String modelId, String userId, Map~String, Object~ featureData)
        +BaseModel getModel() throws StatusCodeWithException
        +List~JObject~ federatedResultByProviders() throws StatusCodeWithException
        +FeatureDataModel findFeatureData(String userId) throws StatusCodeWithException
    }

    class PromoterPredictor {
        -String requestId
        +PromoterPredictor(String requestId, String modelId, String userId, Map~String, Object~ featureData)
        +BaseModel getModel() throws StatusCodeWithException
        +List~JObject~ federatedResultByProviders() throws StatusCodeWithException
        +FeatureDataModel findFeatureData(String userId) throws StatusCodeWithException
    }

    class ClientServiceService {
        <<Interface>>
        +List~ProviderParams~ findProviderList(String modelId)
    }

    class ModelManager {
        <<Static>>
        +BaseModel getModelParam(String modelId)
    }

    class FeatureManager {
        <<Static>>
        +FeatureDataModel getFeatureData(String modelId, String userId)
    }

    class PromoterPredictHelper {
        <<Static>>
        +String buildFederatedPredictParam(String modelId, String requestId, String userId)
        +JObject callProviders(String modelId, String requestId, ProviderParams provider, String requestParam)
    }

    class ProviderParams {
        // 协作方参数类
    }

    class FeatureDataModel {
        -Map~String, Object~ featureDataMap
        +Map~String, Object~ getFeatureDataMap()
    }

    class JObject {
        // JSON对象类
    }

    class StatusCodeWithException {
        // 自定义异常类
    }

    AbstractSinglePredictor <|-- PromoterPredictor
    PromoterPredictor --> ClientServiceService : 依赖
    PromoterPredictor --> ModelManager : 调用
    PromoterPredictor --> FeatureManager : 调用
    PromoterPredictor --> PromoterPredictHelper : 调用
    PromoterPredictor --> ProviderParams : 使用
    PromoterPredictor --> FeatureDataModel : 返回
    PromoterPredictor --> JObject : 返回
    PromoterPredictor ..> StatusCodeWithException : 抛出
```

该类图展示了PromoterPredictor继承自AbstractSinglePredictor，并实现了联邦预测功能的核心结构。PromoterPredictor通过ClientServiceService获取协作方列表，使用PromoterPredictHelper构建请求参数并调用协作方服务，同时依赖ModelManager和FeatureManager获取模型参数和特征数据。整个设计体现了纵向联邦预测的协作流程，包含异常处理和多种数据类型的交互。


### 内部方法调用关系图

```mermaid
graph TD
    A["类PromoterPredictor"]
    B["继承: AbstractSinglePredictor"]
    C["属性: String requestId"]
    D["构造方法: PromoterPredictor(String requestId, String modelId, String userId, Map<String, Object> featureData)"]
    E["重写方法: BaseModel getModel()"]
    F["重写方法: List<JObject> federatedResultByProviders()"]
    G["重写方法: FeatureDataModel findFeatureData(String userId)"]
    H["调用: ModelManager.getModelParam(modelId)"]
    I["调用: Launcher.CONTEXT.getBean(ClientServiceService.class)"]
    J["调用: service.findProviderList(modelId)"]
    K["循环处理: providerList"]
    L["调用: PromoterPredictHelper.buildFederatedPredictParam"]
    M["调用: PromoterPredictHelper.callProviders"]
    N["调用: FeatureManager.getFeatureData"]
    O["异常处理: StatusCodeWithException"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    E --> H
    F --> I
    I --> J
    J --> K
    K --> L
    L --> M
    G --> N
    F -.-> O
    G -.-> O
```

该流程图展示了PromoterPredictor类的结构和主要方法调用关系。该类继承自AbstractSinglePredictor，包含requestId属性和构造方法，并重写了三个核心方法：getModel()通过ModelManager获取模型参数，federatedResultByProviders()通过ClientServiceService获取提供者列表并进行联邦预测，findFeatureData()从FeatureManager获取特征数据。图中清晰呈现了方法间的调用链和异常处理路径，特别是联邦预测时的循环处理流程。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| requestId | String | 私有字符串变量requestId，用于唯一标识请求。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getModel | BaseModel | 该方法重写getModel，调用ModelManager获取指定modelId的参数，可能抛出StatusCodeWithException异常。 |
| federatedResultByProviders | List<JObject> | 该方法通过服务获取协作方列表，若为空则抛出异常。遍历协作方，构建预测参数并调用其接口，汇总结果后返回。 |
| findFeatureData | FeatureDataModel | 方法`findFeatureData`根据用户ID查找特征数据。若`predictParams`中的特征数据非空则直接返回，否则调用`FeatureManager`获取数据。可能抛出`StatusCodeWithException`异常。 |




