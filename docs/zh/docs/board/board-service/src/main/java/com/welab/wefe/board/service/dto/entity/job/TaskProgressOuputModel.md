# 基础信息

|      |      |
|------|------|
| 名称 | TaskProgressOuputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/entity/job/TaskProgressOuputModel.java |
| 包名 | com.welab.wefe.board.service.dto.entity.job |
| 依赖项 | ['com.welab.wefe.board.service.dto.entity.AbstractOutputModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'javax.persistence.EnumType', 'javax.persistence.Enumerated', 'java.util.Date'] |
| 概述说明 | 任务进度输出模型类，包含项目ID、流程号、任务ID、角色、流程节点ID、子任务类型、预计和实际工程量、进度及百分比、耗时和预计结束时间等字段。 |

# 说明

TaskProgressOuputModel类继承AbstractOutputModel，包含任务进度相关属性：项目id、流程号、任务id、角色、流程节点id、子任务类型枚举、预计和实际工程量、进度值及百分比、耗时毫秒数、预计结束时间。所有字段均有getter和setter方法，部分字段通过注解进行校验或枚举类型映射。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TaskProgressOuputModel | class | 任务进度输出模型类，包含项目ID、流程号、任务ID、角色、流程节点ID、子任务类型、预计和实际工程量、进度及百分比、耗时和预计结束时间等字段。 |



## 类 TaskProgressOuputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TaskProgressOuputModel |
| 说明 | 任务进度输出模型类，包含项目ID、流程号、任务ID、角色、流程节点ID、子任务类型、预计和实际工程量、进度及百分比、耗时和预计结束时间等字段。 |


### UML类图

```mermaid
classDiagram
    class AbstractOutputModel {
        <<Abstract>>
    }

    class TaskProgressOuputModel {
        -String projectId
        -String flowId
        -String jobId
        -JobMemberRole role
        -String flowNodeId
        -String taskId
        -ComponentType taskType
        -int expectWorkAmount
        -int reallyWorkAmount
        -int progress
        -double progressRate
        -int spend
        -Date expectEndTime
        +String getProjectId()
        +void setProjectId(String projectId)
        +String getFlowId()
        +void setFlowId(String flowId)
        +String getJobId()
        +void setJobId(String jobId)
        +JobMemberRole getRole()
        +void setRole(JobMemberRole role)
        +String getFlowNodeId()
        +void setFlowNodeId(String flowNodeId)
        +String getTaskId()
        +void setTaskId(String taskId)
        +ComponentType getTaskType()
        +void setTaskType(ComponentType taskType)
        +int getExpectWorkAmount()
        +void setExpectWorkAmount(int expectWorkAmount)
        +int getReallyWorkAmount()
        +void setReallyWorkAmount(int reallyWorkAmount)
        +int getProgress()
        +void setProgress(int progress)
        +double getProgressRate()
        +void setProgressRate(double progressRate)
        +int getSpend()
        +void setSpend(int spend)
        +Date getExpectEndTime()
        +void setExpectEndTime(Date expectEndTime)
    }

    class JobMemberRole {
        <<Enumeration>>
    }

    class ComponentType {
        <<Enumeration>>
    }

    AbstractOutputModel <|-- TaskProgressOuputModel : 继承
    TaskProgressOuputModel --> JobMemberRole : 包含
    TaskProgressOuputModel --> ComponentType : 包含
```

类图描述：TaskProgressOuputModel继承自抽象类AbstractOutputModel，用于跟踪任务进度信息。包含项目ID、流程ID、任务ID等核心标识字段，以及工程量、进度百分比、预计结束时间等统计指标。通过JobMemberRole和ComponentType两个枚举类定义角色和任务类型，所有字段均通过getter/setter方法访问，符合JavaBean规范。


### 内部方法调用关系图

```mermaid
graph TD
    A["类TaskProgressOuputModel"]
    B["继承: AbstractOutputModel"]
    C["属性: String projectId"]
    D["属性: String flowId"]
    E["属性: String jobId"]
    F["属性: JobMemberRole role"]
    G["属性: String flowNodeId"]
    H["属性: String taskId"]
    I["属性: ComponentType taskType"]
    J["属性: int expectWorkAmount"]
    K["属性: int reallyWorkAmount"]
    L["属性: int progress"]
    M["属性: double progressRate"]
    N["属性: int spend"]
    O["属性: Date expectEndTime"]
    P["方法: getProjectId()"]
    Q["方法: setProjectId(String)"]
    R["方法: getFlowId()"]
    S["方法: setFlowId(String)"]
    T["方法: getJobId()"]
    U["方法: setJobId(String)"]
    V["方法: getRole()"]
    W["方法: setRole(JobMemberRole)"]
    X["方法: getFlowNodeId()"]
    Y["方法: setFlowNodeId(String)"]
    Z["方法: getTaskId()"]
    AA["方法: setTaskId(String)"]
    AB["方法: getTaskType()"]
    AC["方法: setTaskType(ComponentType)"]
    AD["方法: getExpectWorkAmount()"]
    AE["方法: setExpectWorkAmount(int)"]
    AF["方法: getReallyWorkAmount()"]
    AG["方法: setReallyWorkAmount(int)"]
    AH["方法: getProgress()"]
    AI["方法: setProgress(int)"]
    AJ["方法: getProgressRate()"]
    AK["方法: setProgressRate(double)"]
    AL["方法: getSpend()"]
    AM["方法: setSpend(int)"]
    AN["方法: getExpectEndTime()"]
    AO["方法: setExpectEndTime(Date)"]

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
```

这段代码定义了一个名为TaskProgressOuputModel的类，继承自AbstractOutputModel，用于跟踪和管理任务进度相关的数据。类中包含多个属性，如项目ID、流程ID、任务ID等，以及对应的getter和setter方法。这些属性用于存储任务的详细信息，包括预计和实际工程量、进度百分比、预计结束时间等。通过枚举类型JobMemberRole和ComponentType，可以明确角色和任务类型的取值范围，确保数据的准确性和一致性。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| taskType | ComponentType | 定义枚举类型字段taskType，使用字符串形式存储枚举值。 |
| flowId | String | 定义流程号字段，使用@Check注解校验。 |
| expectEndTime | Date | 代码定义了一个私有日期类型变量expectEndTime，并用@Check注解标记其名称为"预计结束时间"。 |
| taskId | String | 定义私有字符串变量taskId，使用@Check注解校验任务id。 |
| flowNodeId | String | 定义私有字符串变量flowNodeId，使用@Check注解校验流程节点id。 |
| progress | int | 进度检查的私有整型变量progress。 |
| spend | int | 字段spend存储updated_time与created_time的时间差，单位为毫秒。 |
| reallyWorkAmount | int | 字段reallyWorkAmount标注为实际总工程量检查项。 |
| role | JobMemberRole | 定义枚举类型字段role，使用字符串值存储枚举常量。 |
| jobId | String | 定义私有字符串变量jobId，使用@Check注解标记任务id。 |
| projectId | String | 定义私有字符串变量projectId，使用@Check注解校验项目id。 |
| expectWorkAmount | int | 定义私有整型变量expectWorkAmount，使用@Check注解标记为"预计总工程量"。 |
| progressRate | double | 进度百分比检查项，私有双精度变量progressRate。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFlowNodeId | String | 方法返回flowNodeId字符串。 |
| setFlowId | void | 设置流程ID的方法，将参数flowId赋值给当前对象的flowId属性。 |
| setProjectId | void | 这是一个Java方法，用于设置类的projectId属性。方法接收一个字符串参数projectId，并将其赋值给类的同名成员变量。 |
| setExpectWorkAmount | void | 这是一个Java方法，用于设置期望工作量的整数值。方法接受一个整数参数expectWorkAmount，并将其赋值给类的同名成员变量。 |
| setReallyWorkAmount | void | 设置实际工作量的方法，将参数赋值给成员变量reallyWorkAmount。 |
| getFlowId | String | 获取flowId的公共方法，返回字符串类型的flowId值。 |
| getProjectId | String | 获取项目ID的方法，返回字符串类型的projectId。 |
| getReallyWorkAmount | int | 获取实际工作量的整数值方法。 |
| getJobId | String | 获取当前任务的唯一标识符jobId。 |
| getProgress | int | 获取当前进度值的方法，返回整数类型变量progress的值。 |
| setRole | void | 方法setRole用于设置成员角色，参数为JobMemberRole类型，赋值给当前对象的role属性。 |
| getRole | JobMemberRole | 这是一个Java方法，返回JobMemberRole类型的role字段值。 |
| setProgressRate | void | 设置进度率方法，接收双精度参数并赋值给成员变量progressRate。 |
| setTaskId | void | 设置任务ID的方法，将参数taskId赋值给当前对象的taskId属性。 |
| setFlowNodeId | void | 设置流程节点ID的方法，将传入的字符串参数赋值给类的成员变量flowNodeId。 |
| setProgress | void | 设置进度值的方法，参数为整型progress，直接赋值给类成员变量progress。 |
| setJobId | void | 设置任务ID的方法，将输入参数jobId赋值给当前对象的jobId属性。 |
| getExpectWorkAmount | int | 这是一个Java方法，返回名为expectWorkAmount的整型变量值。 |
| getProgressRate | double | 获取进度率的方法，返回double类型的progressRate值。 |
| getSpend | int | 获取spend变量的整型值。 |
| setSpend | void | 这是一个Java方法，用于设置类成员变量spend的值。方法接受一个整数参数，并将其赋值给当前对象的spend属性。 |
| getExpectEndTime | Date | 获取预期结束时间的方法，返回Date类型值expectEndTime。 |
| setExpectEndTime | void | 设置预期结束时间的方法，参数为Date类型，赋值给类成员变量expectEndTime。 |
| setTaskType | void | 设置任务类型的方法，将参数taskType赋值给当前对象的taskType属性。 |
| getTaskType | ComponentType | 方法返回任务类型ComponentType。 |
| getTaskId | String | 获取任务ID的方法，返回字符串类型的taskId。 |




