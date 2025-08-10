# 基础信息

|      |      |
|------|------|
| 名称 | AsyncTaskConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/config/AsyncTaskConfig.java |
| 包名 | com.welab.wefe.gateway.config |
| 依赖项 | ['org.springframework.beans.factory.annotation.Autowired', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'org.springframework.core.task.AsyncTaskExecutor', 'org.springframework.scheduling.concurrent.ThreadPoolTaskExecutor', 'java.util.concurrent.ThreadPoolExecutor'] |
| 概述说明 | 配置类AsyncTaskConfig定义异步任务执行器，核心线程数取自配置，最大线程数为核心数乘100，线程名前缀为transferMetaDataAsyncExecutor-Thread-，关闭时等待任务完成，拒绝策略为调用者运行。 |

# 说明

该配置类定义了一个异步任务执行器，用于处理数据传输任务。通过注入的配置属性动态设置线程池参数，包括核心线程数和最大线程数。执行器使用自定义线程名前缀，设置120秒空闲线程存活时间，并确保关闭时等待任务完成。当任务被拒绝时采用调用者运行策略。该执行器专为元数据传输任务优化，核心线程数由配置决定，最大线程数为核心线程数的100倍。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AsyncTaskConfig | class | 配置类AsyncTaskConfig定义了一个异步任务执行器transferMetaDataAsyncExecutor，核心线程数和最大线程数由配置属性决定，线程名前缀为transferMetaDataAsyncExecutor-Thread-，关闭时等待任务完成，拒绝策略为调用者运行。 |



## 类 AsyncTaskConfig

|      |      |
|------|------|
| 访问范围 | @Configuration;public |
| 类型 | class |
| 名称 | AsyncTaskConfig |
| 说明 | 配置类AsyncTaskConfig定义了一个异步任务执行器transferMetaDataAsyncExecutor，核心线程数和最大线程数由配置属性决定，线程名前缀为transferMetaDataAsyncExecutor-Thread-，关闭时等待任务完成，拒绝策略为调用者运行。 |


### UML类图

```mermaid
classDiagram
    class AsyncTaskConfig {
        -ConfigProperties configProperties
        +AsyncTaskExecutor transferMetaDataAsyncExecutor()
        -AsyncTaskExecutor buildExecutor(String prefix, int coreSize, int poolSize)
    }

    class ConfigProperties {
        +int getDataSinkCorePoolSize()
    }

    class ThreadPoolTaskExecutor {
        +setThreadNamePrefix(String prefix)
        +setCorePoolSize(int coreSize)
        +setMaxPoolSize(int maxSize)
        +setKeepAliveSeconds(int seconds)
        +setWaitForTasksToCompleteOnShutdown(boolean wait)
        +setRejectedExecutionHandler(RejectedExecutionHandler handler)
    }

    class ThreadPoolExecutor {
        <<Interface>>
    }

    class RejectedExecutionHandler {
        <<Interface>>
    }

    AsyncTaskConfig --> ConfigProperties : 依赖
    AsyncTaskConfig --> ThreadPoolTaskExecutor : 创建
    ThreadPoolTaskExecutor ..|> AsyncTaskExecutor : 实现
    ThreadPoolTaskExecutor --> ThreadPoolExecutor : 使用
    ThreadPoolTaskExecutor --> RejectedExecutionHandler : 使用
```

这段代码展示了Spring配置类AsyncTaskConfig如何创建线程池执行器。该类通过@Autowired注入ConfigProperties配置，使用buildExecutor方法构建ThreadPoolTaskExecutor实例，设置线程名前缀、核心/最大线程数等参数，并指定拒绝策略为CallerRunsPolicy。类图清晰地呈现了配置类与线程池组件之间的依赖关系，以及接口实现关系。


### 内部方法调用关系图

```mermaid
graph TD
    A["类AsyncTaskConfig"]
    B["自动注入属性: ConfigProperties configProperties"]
    C["Bean方法: AsyncTaskExecutor transferMetaDataAsyncExecutor()"]
    D["私有方法: buildExecutor(String prefix, int coreSize, int poolSize)"]
    E["创建ThreadPoolTaskExecutor实例"]
    F["配置线程名前缀: setThreadNamePrefix"]
    G["配置核心线程数: setCorePoolSize"]
    H["配置最大线程数: setMaxPoolSize"]
    I["配置空闲时间: setKeepAliveSeconds"]
    J["配置关闭策略: setWaitForTasksToCompleteOnShutdown"]
    K["配置拒绝策略: setRejectedExecutionHandler"]

    A --> B
    A --> C
    C --> D
    D --> E
    E --> F
    E --> G
    E --> H
    E --> I
    E --> J
    E --> K
```

这段代码是Spring配置类AsyncTaskConfig的实现，主要功能是创建并配置一个异步任务执行器。通过自动注入的ConfigProperties获取线程池参数，调用buildExecutor方法构建ThreadPoolTaskExecutor实例，设置线程名前缀、核心/最大线程数、空闲存活时间、关闭等待策略和拒绝策略等参数。该配置类提供了可定制化的线程池配置方案，适用于需要异步处理任务的场景。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| configProperties | ConfigProperties | 代码片段使用@Autowired自动注入ConfigProperties配置类实例。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| transferMetaDataAsyncExecutor | AsyncTaskExecutor | 创建异步任务执行器transferMetaDataAsyncExecutor，核心线程数为配置的dataSinkCorePoolSize，最大队列容量为核心线程数的100倍。 |
| buildExecutor | AsyncTaskExecutor | 创建线程池执行器，设置线程名前缀、核心和最大线程数、保活时间、关闭等待任务完成及拒绝策略。 |




