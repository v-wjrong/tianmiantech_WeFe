# 基础信息

|      |      |
|------|------|
| 名称 | MemberQueryOutput |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/dto/member/MemberQueryOutput.java |
| 包名 | com.welab.wefe.union.service.dto.member |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.web.dto.AbstractTimedApiOutput'] |
| 概述说明 | MemberQueryOutput类继承AbstractTimedApiOutput，包含成员ID、姓名、联系方式、状态标志、公钥、网关URI、logo及时间戳等属性，并提供getter和setter方法。 |

# 说明

MemberQueryOutput类继承自AbstractTimedApiOutput，用于封装成员查询结果。包含成员ID、姓名、手机、邮箱等基本信息，以及允许开放数据集、隐藏、冻结、失联等状态标识。还包含公钥、网关URI、LOGO地址等扩展信息，以及日志时间和最后活动时间两个时间戳。最后通过MemberExtJSON类型的extJson字段支持额外扩展属性。所有字段均通过getter和setter方法进行访问和修改。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberQueryOutput | class | MemberQueryOutput类继承AbstractTimedApiOutput，包含成员ID、姓名、联系方式、状态标志、公钥、网关URI、logo及时间戳等属性，并提供getter/setter方法。 |



## 类 MemberQueryOutput

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MemberQueryOutput |
| 说明 | MemberQueryOutput类继承AbstractTimedApiOutput，包含成员ID、姓名、联系方式、状态标志、公钥、网关URI、logo及时间戳等属性，并提供getter/setter方法。 |


### UML类图

```mermaid
classDiagram
    class AbstractTimedApiOutput {
        <<Abstract>>
    }
    
    class MemberQueryOutput {
        -String id
        -String name
        -String mobile
        -String email
        -int allowOpenDataSet
        -int hidden
        -int freezed
        -int lostContact
        -String publicKey
        -String gatewayUri
        -String logo
        -long logTime
        -long lastActivityTime
        -MemberExtJSON extJson
        +String getId()
        +void setId(String id)
        +String getName()
        +void setName(String name)
        // ...其他getter/setter方法省略...
        +MemberExtJSON getExtJson()
        +void setExtJson(MemberExtJSON extJson)
    }
    
    class MemberExtJSON {
        // 假设这是一个包含扩展属性的类
    }
    
    AbstractTimedApiOutput <|-- MemberQueryOutput : 继承
    MemberQueryOutput --> MemberExtJSON : 包含
```

类图描述：MemberQueryOutput继承自AbstractTimedApiOutput，包含成员基本属性（如id、name等）和扩展属性MemberExtJSON。该类通过getter/setter方法提供对私有字段的访问控制，其中状态属性（如hidden、freezed）使用int类型表示，时间相关属性使用long类型存储。MemberExtJSON作为扩展信息容器与主类形成组合关系。


### 内部方法调用关系图

```mermaid
graph TD
    A["类MemberQueryOutput"]
    B["继承自: AbstractTimedApiOutput"]
    C["属性: String id"]
    D["属性: String name"]
    E["属性: String mobile"]
    F["属性: String email"]
    G["属性: int allowOpenDataSet"]
    H["属性: int hidden"]
    I["属性: int freezed"]
    J["属性: int lostContact"]
    K["属性: String publicKey"]
    L["属性: String gatewayUri"]
    M["属性: String logo"]
    N["属性: long logTime"]
    O["属性: long lastActivityTime"]
    P["属性: MemberExtJSON extJson"]
    Q["方法: String getId()"]
    R["方法: void setId(String id)"]
    S["方法: String getName()"]
    T["方法: void setName(String name)"]
    U["方法: String getMobile()"]
    V["方法: void setMobile(String mobile)"]
    W["方法: String getEmail()"]
    X["方法: void setEmail(String email)"]
    Y["方法: int getAllowOpenDataSet()"]
    Z["方法: void setAllowOpenDataSet(int allowOpenDataSet)"]
    AA["方法: int getHidden()"]
    AB["方法: void setHidden(int hidden)"]
    AC["方法: int getFreezed()"]
    AD["方法: void setFreezed(int freezed)"]
    AE["方法: int getLostContact()"]
    AF["方法: void setLostContact(int lostContact)"]
    AG["方法: String getPublicKey()"]
    AH["方法: void setPublicKey(String publicKey)"]
    AI["方法: String getGatewayUri()"]
    AJ["方法: void setGatewayUri(String gatewayUri)"]
    AK["方法: String getLogo()"]
    AL["方法: void setLogo(String logo)"]
    AM["方法: long getLogTime()"]
    AN["方法: void setLogTime(long logTime)"]
    AO["方法: long getLastActivityTime()"]
    AP["方法: void setLastActivityTime(long lastActivityTime)"]
    AQ["方法: MemberExtJSON getExtJson()"]
    AR["方法: void setExtJson(MemberExtJSON extJson)"]

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
    A --> S
    A --> T
    A --> U
    A --> V
    A --> W
    A --> X
    A --> Y
    A --> Z
    A --> AA
    A --> AB
    A --> AC
    A --> AD
    A --> AE
    A --> AF
    A --> AG
    A --> AH
    A --> AI
    A --> AJ
    A --> AK
    A --> AL
    A --> AM
    A --> AN
    A --> AO
    A --> AP
    A --> AQ
    A --> AR
```

该流程图展示了`MemberQueryOutput`类的完整结构，包括其继承关系、14个私有属性以及对应的getter/setter方法。该类作为API输出模型，封装了成员查询结果的所有字段（如基础信息、状态标志、扩展数据等），并通过继承`AbstractTimedApiOutput`获得时间相关功能。每个属性都严格遵循JavaBean规范提供访问方法，确保数据封装性。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| id | String | 私有字符串类型变量id。 |
| mobile | String | 定义私有字符串变量mobile。 |
| lastActivityTime | long | 私有长整型变量，记录最后活动时间。 |
| gatewayUri | String | 私有字符串变量gatewayUri，用于存储网关URI。 |
| logTime | long | 私有长整型变量logTime，用于记录时间。 |
| logo | String | 定义私有字符串变量logo。 |
| lostContact | int | 私有整型变量，记录丢失联系次数。 |
| extJson | MemberExtJSON | 成员扩展JSON数据对象 |
| publicKey | String | 声明一个私有字符串变量publicKey，用于存储公钥。 |
| freezed | int | 私有整型变量freezed，用于表示冻结状态。 |
| email | String | 声明一个私有字符串变量email。 |
| name | String | 声明一个私有字符串变量name。 |
| allowOpenDataSet | int | 私有整型变量，用于控制数据集开放权限。 |
| hidden | int | 私有整型变量hidden。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFreezed | int | 获取冻结状态值的方法，返回整数类型变量freezed。 |
| getId | String | 获取ID的公共方法，返回字符串类型的id。 |
| setName | void | 设置对象名称的方法，将参数name赋值给对象的name属性。 |
| setId | void | 设置对象ID的方法，将参数id赋值给对象的id属性。 |
| getHidden | int | 获取hidden变量的值。 |
| setEmail | void | 这是一个Java方法，用于设置对象的email属性，接收一个字符串参数email并将其赋值给当前对象的email字段。 |
| getLostContact | int | 获取丢失联系次数的整数值。 |
| getAllowOpenDataSet | int | 这是一个Java方法，返回整型变量allowOpenDataSet的值。 |
| getPublicKey | String | 获取公钥的方法，返回publicKey变量。 |
| getGatewayUri | String | 这是一个Java方法，返回字符串类型的gatewayUri成员变量值。 |
| setFreezed | void | 设置冻结状态的方法，参数为整型freezed，赋值给类成员变量freezed。 |
| setAllowOpenDataSet | void | 该方法用于设置允许打开的数据集数量，参数为整型allowOpenDataSet。 |
| getEmail | String | 获取email的字符串方法。 |
| setMobile | void | 这是一个Java方法，用于设置类的mobile属性值。方法接收一个字符串参数mobile，并将其赋值给类的同名成员变量。 |
| getMobile | String | 获取手机号的方法，返回字符串类型变量mobile。 |
| getName | String | 获取名称的方法，返回字符串类型的name变量值。 |
| setPublicKey | void | 设置公钥的方法，将输入字符串赋值给类的publicKey成员变量。 |
| setHidden | void | 设置隐藏状态的方法，参数为整型hidden，赋值给当前对象的hidden属性。 |
| setLastActivityTime | void | 设置最后活动时间的方法，将参数lastActivityTime赋值给类的同名成员变量。 |
| getExtJson | MemberExtJSON | 方法getExtJson返回成员扩展JSON对象extJson。 |
| setExtJson | void | 方法setExtJson用于设置成员扩展JSON数据，参数为MemberExtJSON类型，赋值给当前对象的extJson属性。 |
| getLogo | String | 获取logo字符串的方法。 |
| setLostContact | void | 设置丢失联系状态的方法，参数为整型lostContact。 |
| setGatewayUri | void | 设置网关URI的方法，将输入参数赋值给类的gatewayUri成员变量。 |
| setLogo | void | 设置logo字符串的方法。 |
| getLogTime | long | 获取日志时间的方法，返回长整型数值logTime。 |
| setLogTime | void | 设置日志时间的方法，将参数logTime赋值给成员变量logTime。 |
| getLastActivityTime | long | 获取最后活动时间的方法，返回长整型数值。 |




