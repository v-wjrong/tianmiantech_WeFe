# 基础信息

|      |      |
|------|------|
| 名称 | ApiDataResourceQueryOutput |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/dto/dataresource/ApiDataResourceQueryOutput.java |
| 包名 | com.welab.wefe.union.service.dto.dataresource |
| 依赖项 | ['com.welab.wefe.common.web.dto.AbstractTimedApiOutput', 'com.welab.wefe.common.wefe.enums.DataResourceType'] |
| 概述说明 | ApiDataResourceQueryOutput类继承AbstractTimedApiOutput，包含数据资源ID、成员信息、名称、描述、标签、数据量、公开级别、使用统计等属性及其getter/setter方法。 |

# 说明

ApiDataResourceQueryOutput类继承自AbstractTimedApiOutput，包含数据资源查询输出的详细信息。主要属性包括数据资源ID、成员ID和名称、资源名称、描述、标签、总数据量、公开级别、公开成员列表、在作业/流程/项目/成员中的使用次数、启用状态以及数据资源类型。每个属性都有对应的getter和setter方法用于访问和修改。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ApiDataResourceQueryOutput | class | ApiDataResourceQueryOutput类继承AbstractTimedApiOutput，包含数据资源ID、成员信息、名称、描述、标签、数据量、公开级别、使用统计等属性及其getter/setter方法。 |



## 类 ApiDataResourceQueryOutput

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ApiDataResourceQueryOutput |
| 说明 | ApiDataResourceQueryOutput类继承AbstractTimedApiOutput，包含数据资源ID、成员信息、名称、描述、标签、数据量、公开级别、使用统计等属性及其getter/setter方法。 |


### UML类图

```mermaid
classDiagram
    class AbstractTimedApiOutput {
        <<Abstract>>
    }
    
    class ApiDataResourceQueryOutput {
        -String dataResourceId
        -String memberId
        -String memberName
        -String name
        -String description
        -String tags
        -String totalDataCount
        -String publicLevel
        -String publicMemberList
        -String usageCountInJob
        -String usageCountInFlow
        -String usageCountInProject
        -String usageCountInMember
        -String enable
        -DataResourceType dataResourceType
        +String getDataResourceId()
        +void setDataResourceId(String dataResourceId)
        +String getMemberId()
        +void setMemberId(String memberId)
        +String getMemberName()
        +void setMemberName(String memberName)
        +String getName()
        +void setName(String name)
        +String getDescription()
        +void setDescription(String description)
        +String getTags()
        +void setTags(String tags)
        +String getTotalDataCount()
        +void setTotalDataCount(String totalDataCount)
        +String getPublicLevel()
        +void setPublicLevel(String publicLevel)
        +String getPublicMemberList()
        +void setPublicMemberList(String publicMemberList)
        +String getUsageCountInJob()
        +void setUsageCountInJob(String usageCountInJob)
        +String getUsageCountInFlow()
        +void setUsageCountInFlow(String usageCountInFlow)
        +String getUsageCountInProject()
        +void setUsageCountInProject(String usageCountInProject)
        +String getUsageCountInMember()
        +void setUsageCountInMember(String usageCountInMember)
        +String getEnable()
        +void setEnable(String enable)
        +DataResourceType getDataResourceType()
        +void setDataResourceType(DataResourceType dataResourceType)
    }
    
    class DataResourceType {
        <<Enum>>
    }
    
    AbstractTimedApiOutput <|-- ApiDataResourceQueryOutput : 继承
    ApiDataResourceQueryOutput --> DataResourceType : 包含
```

类图描述：ApiDataResourceQueryOutput类继承自AbstractTimedApiOutput抽象类，包含数据资源ID、成员信息、名称、描述、标签、数据统计量、公开级别、使用计数等私有字段，以及对应的getter和setter方法。该类与DataResourceType枚举类存在关联关系，表示数据资源类型。整体结构展示了数据资源查询输出的完整属性集合和类型关系。


### 内部方法调用关系图

```mermaid
graph TD
    A["类ApiDataResourceQueryOutput"]
    B["继承自: AbstractTimedApiOutput"]
    C["属性: String dataResourceId"]
    D["属性: String memberId"]
    E["属性: String memberName"]
    F["属性: String name"]
    G["属性: String description"]
    H["属性: String tags"]
    I["属性: String totalDataCount"]
    J["属性: String publicLevel"]
    K["属性: String publicMemberList"]
    L["属性: String usageCountInJob"]
    M["属性: String usageCountInFlow"]
    N["属性: String usageCountInProject"]
    O["属性: String usageCountInMember"]
    P["属性: String enable"]
    Q["属性: DataResourceType dataResourceType"]
    R["Getter/Setter方法组"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
    A --> K
    A --> L
    A --> M
    A --> N
    A --> O
    A --> P
    A --> Q
    A --> R
```

这段代码定义了一个ApiDataResourceQueryOutput类，继承自AbstractTimedApiOutput基类。该类包含15个私有属性，主要描述数据资源的相关信息，如资源ID、成员信息、名称、描述、标签、数据总量、公开级别、使用统计等。每个属性都配有对应的getter和setter方法，用于封装属性的访问和修改。这是一个典型的数据传输对象(DTO)设计，用于在系统不同层之间传递结构化数据。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| enable | String | 定义私有字符串变量enable。 |
| name | String | 私有字符串类型变量name。 |
| memberName | String | 成员变量名称为memberName，类型为String。 |
| usageCountInMember | String | 成员使用次数统计字段。 |
| usageCountInProject | String | 项目中的使用次数统计变量。 |
| description | String | 私有字符串类型变量description。 |
| dataResourceId | String | 私有字符串类型变量dataResourceId，用于标识数据资源。 |
| tags | String | 私有字符串变量tags，用于存储标签信息。 |
| dataResourceType | DataResourceType | 私有数据资源类型变量。 |
| usageCountInJob | String | 私有字符串变量，记录作业中的使用次数。 |
| memberId | String | 成员ID字符串类型私有变量。 |
| usageCountInFlow | String | 私有字符串变量usageCountInFlow，用于记录流程中的使用次数。 |
| publicMemberList | String | 私有字符串变量publicMemberList，用于存储公共成员列表。 |
| totalDataCount | String | 私有字符串变量totalDataCount，用于存储数据总数。 |
| publicLevel | String | 私有字符串变量publicLevel，用于存储公开级别信息。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setName | void | 设置对象名称的方法，将输入参数name赋值给对象的name属性。 |
| getMemberId | String | 获取成员ID的方法，返回成员ID字符串。 |
| getDataResourceType | DataResourceType | 获取数据资源类型的方法，返回dataResourceType对象。 |
| setEnable | void | 这是一个Java方法，用于设置成员变量enable的值。方法接收一个字符串参数enable，并将其赋值给类的同名成员变量。 |
| getEnable | String | 获取enable值的公共方法，返回字符串类型。 |
| getName | String | 获取对象名称的方法，返回字符串类型的name属性值。 |
| setDataResourceType | void | 设置数据资源类型的方法，参数为DataResourceType类型，赋值给类的成员变量dataResourceType。 |
| setPublicLevel | void | 设置公共级别的方法，将输入参数赋值给类的公共级别属性。 |
| getTags | String | 方法getTags返回字符串变量tags的值。 |
| setTags | void | 这是一个Java方法，用于设置对象的tags属性值。方法接收一个字符串参数tags，并将其赋值给当前对象的tags字段。 |
| getTotalDataCount | String | 这是一个Java方法，返回字符串类型的totalDataCount变量值。 |
| setUsageCountInProject | void | 设置项目内使用次数的公共方法，参数为字符串类型。 |
| setTotalDataCount | void | 这是一个Java方法，用于设置totalDataCount属性的值。方法接收一个字符串参数，并将其赋值给类的成员变量totalDataCount。 |
| setPublicMemberList | void | 设置公共成员列表的方法，将输入字符串赋值给类的成员变量publicMemberList。 |
| setDataResourceId | void | 设置数据资源ID的方法，将输入参数赋值给类的成员变量dataResourceId。 |
| getPublicLevel | String | 方法getPublicLevel返回publicLevel字符串值。 |
| getUsageCountInFlow | String | 获取流程中的使用次数。 |
| getPublicMemberList | String | 获取公共成员列表的方法，返回字符串类型变量publicMemberList。 |
| setMemberName | void | 设置成员名称的方法，将输入参数赋值给成员变量memberName。 |
| getUsageCountInProject | String | 获取项目内使用次数的字符串方法。 |
| setMemberId | void | Java方法：设置成员ID，参数为字符串memberId，赋值给当前对象的memberId属性。 |
| getUsageCountInMember | String | 获取成员使用次数的方法，返回字符串类型的usageCountInMember值。 |
| getUsageCountInJob | String | 这是一个Java方法，返回字符串类型的usageCountInJob变量值。 |
| getDescription | String | 获取描述信息的方法，返回字符串类型的描述内容。 |
| getDataResourceId | String | 获取数据资源ID的方法，返回字符串类型值dataResourceId。 |
| setDescription | void | 这是一个Java方法，用于设置对象的描述属性，将传入的字符串赋值给成员变量description。 |
| getMemberName | String | 这是一个Java方法，返回成员变量memberName的值。 |
| setUsageCountInJob | void | 这是一个Java方法，用于设置作业中的使用次数属性值。方法接受一个字符串参数，并将其赋值给类的成员变量usageCountInJob。 |
| setUsageCountInFlow | void | 设置流程内使用次数的字符串值方法。 |
| setUsageCountInMember | void | 设置成员内使用次数的公共方法，参数为字符串类型的usageCountInMember，将其赋值给类成员变量。 |




