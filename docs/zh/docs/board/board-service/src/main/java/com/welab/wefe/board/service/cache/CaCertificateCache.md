# 基础信息

|      |      |
|------|------|
| 名称 | CaCertificateCache |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/cache/CaCertificateCache.java |
| 包名 | com.welab.wefe.board.service.cache |
| 依赖项 | ['com.welab.wefe.board.service.sdk.union.UnionService', 'com.welab.wefe.common.web.Launcher', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 | CaCertificateCache类是一个单例模式的CA证书缓存，使用ConcurrentHashMap存储证书数据，提供刷新缓存、获取单个或全部证书的功能。内部类CaCertificate包含id、name和content属性。 |

# 说明

CaCertificateCache是一个单例类，用于管理CA证书缓存。它使用ConcurrentHashMap存储CaCertificate对象，提供刷新缓存、获取单个或全部证书的功能。刷新缓存时从UnionService获取最新证书列表，更新并清理无效数据。CaCertificate是内部类，包含id、name和content属性及对应的getter和setter方法。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CaCertificateCache | class | CaCertificateCache类是一个单例缓存，用于存储CaCertificate对象。它提供刷新缓存、获取单个或全部证书的方法。内部使用ConcurrentHashMap存储数据，CaCertificate包含id、name和content属性。 |



## 类 CaCertificateCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CaCertificateCache |
| 说明 | CaCertificateCache类是一个单例缓存，用于存储CaCertificate对象。它提供刷新缓存、获取单个或全部证书的方法。内部使用ConcurrentHashMap存储数据，CaCertificate包含id、name和content属性。 |


### UML类图

```mermaid
classDiagram
    class CaCertificateCache {
        -Logger LOG
        -ConcurrentHashMap~String, CaCertificate~ data
        -CaCertificateCache()
        +getInstance() CaCertificateCache
        +refreshCache() boolean
        +get(String id) CaCertificate
        +getAll() List~CaCertificate~
    }

    class CaCertificate {
        -String id
        -String name
        -String content
        +getId() String
        +setId(String id) void
        +getName() String
        +setName(String name) void
        +getContent() String
        +setContent(String content) void
    }

    class UnionService {
        <<Interface>>
        +findAllCertificate() List~CaCertificate~
    }

    CaCertificateCache --> UnionService : 依赖
    CaCertificateCache *-- CaCertificate : 包含
```

这段代码展示了一个单例模式的CA证书缓存系统，包含CaCertificateCache主类和嵌套的CaCertificate数据类。CaCertificateCache使用ConcurrentHashMap存储证书数据，通过refreshCache方法从UnionService接口获取最新证书列表并同步更新缓存，同时提供get和getAll查询方法。CaCertificate类封装了证书ID、名称和内容等基础属性，采用标准JavaBean设计。整体设计实现了线程安全的证书缓存管理，支持动态更新和查询功能。


### 内部方法调用关系图

```mermaid
graph TD
    A["类CaCertificateCache"]
    B["属性: Logger LOG"]
    C["属性: static CaCertificateCache实例"]
    D["属性: ConcurrentHashMap<String, CaCertificate> data"]
    E["私有构造方法"]
    F["静态方法: getInstance()"]
    G["方法: refreshCache()"]
    H["方法: get(String id)"]
    I["方法: getAll()"]
    J["内部类CaCertificate"]
    K["属性: String id"]
    L["属性: String name"]
    M["属性: String content"]
    N["方法: getId/setId"]
    O["方法: getName/setName"]
    P["方法: getContent/setContent"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
    J --> K
    J --> L
    J --> M
    J --> N
    J --> O
    J --> P

    G --> G1["获取证书列表"]
    G1 --> G2{"列表为空?"}
    G2 -->|是| G3["清空缓存"]
    G2 -->|否| G4["更新缓存数据"]
    G4 --> G5["收集查询ID"]
    G5 --> G6["标记待删除ID"]
    G6 --> G7["删除过期数据"]
```

```mermaid
sequenceDiagram
    participant Client
    participant CaCertificateCache
    participant UnionService
    participant ConcurrentHashMap

    Client->>CaCertificateCache: getInstance()
    CaCertificateCache-->>Client: 返回单例
    Client->>CaCertificateCache: refreshCache()
    CaCertificateCache->>UnionService: findAllCertificate()
    UnionService-->>CaCertificateCache: 返回证书列表
    alt 列表为空
        CaCertificateCache->>ConcurrentHashMap: clear()
    else 列表非空
        loop 遍历证书
            CaCertificateCache->>ConcurrentHashMap: put(id,certificate)
        end
        CaCertificateCache->>ConcurrentHashMap: forEach(检查过期)
        loop 删除过期
            CaCertificateCache->>ConcurrentHashMap: remove(id)
        end
    end
    CaCertificateCache-->>Client: 返回操作结果
```

该流程图展示了CaCertificateCache类的结构和核心方法refreshCache的执行逻辑。这是一个单例模式的证书缓存类，通过ConcurrentHashMap存储证书数据，提供缓存刷新、查询等功能。refreshCache方法通过对比数据库查询结果与现有缓存，实现了增量更新和过期数据清理的机制，确保缓存数据一致性。时序图则详细描述了客户端调用缓存刷新时，与UnionService和内部存储结构的交互过程。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| data = new ConcurrentHashMap<>() | ConcurrentHashMap<String, CaCertificate> | 线程安全的哈希表，存储字符串到CaCertificate对象的映射。 |
| LOG = LoggerFactory.getLogger(CaCertificateCache.class) | Logger | 类CaCertificateCache中定义了一个私有不可变的日志记录器LOG。 |
| caCertificateCache = new CaCertificateCache() | CaCertificateCache | 声明一个静态不可变的CA证书缓存实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | CaCertificateCache | 这是一个静态方法，返回CaCertificateCache类的单例实例caCertificateCache。 |
| refreshCache | boolean | 方法refreshCache用于更新证书缓存：获取所有证书列表，若为空则清空缓存；否则更新缓存数据，移除不存在的证书ID。成功返回true，失败记录错误并返回false。 |
| get | CaCertificate | 方法get通过id从data中获取对应的CaCertificate对象。 |
| getAll | List<CaCertificate> | 该方法返回存储的所有CA证书列表，以ArrayList形式提供数据副本。 |




