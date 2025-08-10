# 基础信息

|      |      |
|------|------|
| 名称 | AppConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/config/AppConfig.java |
| 包名 | com.welab.wefe.common.web.config |
| 依赖项 | ['com.alibaba.fastjson.PropertyNamingStrategy', 'com.alibaba.fastjson.serializer.SerializeConfig', 'com.alibaba.fastjson.serializer.SerializeFilter', 'com.alibaba.fastjson.serializer.SerializerFeature', 'com.alibaba.fastjson.support.config.FastJsonConfig', 'com.alibaba.fastjson.support.spring.FastJsonHttpMessageConverter', 'com.welab.wefe.common.TimeSpan', 'com.welab.wefe.common.fieldvalidate.secret.SecretValueFilter', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.boot.autoconfigure.http.HttpMessageConverters', 'org.springframework.boot.web.servlet.FilterRegistrationBean', 'org.springframework.context.ApplicationListener', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'org.springframework.context.event.ContextRefreshedEvent', 'org.springframework.http.MediaType', 'org.springframework.web.cors.CorsConfiguration', 'java.util.ArrayList', 'java.util.List'] |
| 概述说明 | AppConfig配置类实现跨域过滤器，允许指定源或全部源访问，设置FastJson为JSON序列化组件，支持蛇形命名和空值输出。 |

# 说明

这是一个Spring Boot应用配置类，主要实现跨域配置和JSON序列化设置。类实现了ApplicationListener接口监听容器刷新事件。跨域配置通过FilterRegistrationBean注册CORS过滤器，支持动态配置允许的域名，默认允许所有来源，设置允许所有方法和头部，缓存10分钟，允许凭证。JSON序列化使用FastJson，配置全局下划线命名策略，支持UTF-8 JSON媒体类型，启用字段排序、空值输出和错误getter忽略特性，并添加了敏感值过滤处理。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AppConfig | class | AppConfig配置类实现跨域过滤器与FastJSON消息转换器。跨域配置允许指定源或全部，设置头、方法、缓存及凭证。FastJSON配置下划线命名策略，支持空字段输出，并添加SecretValueFilter。 |



## 类 AppConfig

|      |      |
|------|------|
| 访问范围 | @Configuration;public |
| 类型 | class |
| 名称 | AppConfig |
| 说明 | AppConfig配置类实现跨域过滤器与FastJSON消息转换器。跨域配置允许指定源或全部，设置头、方法、缓存及凭证。FastJSON配置下划线命名策略，支持空字段输出，并添加SecretValueFilter。 |


### UML类图

```mermaid
classDiagram
    class AppConfig {
        -CommonConfig commonConfig
        +onApplicationEvent(ContextRefreshedEvent contextRefreshedEvent) void
        +corsFilter() FilterRegistrationBean
        +fastJsonHttpMessageConverters() HttpMessageConverters
    }

    class CommonConfig {
        +getCorsAllowedOrigins() String[]
    }

    class CorsConfiguration {
        +addAllowedOrigin(String origin) void
        +addAllowedHeader(String header) void
        +addAllowedMethod(String method) void
        +setMaxAge(long maxAge) void
        +setAllowCredentials(boolean allowCredentials) void
    }

    class FilterRegistrationBean {
        +setOrder(int order) void
    }

    class MyCorsFilter {
        +MyCorsFilter(CorsConfiguration config)
    }

    class HttpMessageConverters {
        +HttpMessageConverters(HttpMessageConverter~?~... converters)
    }

    class FastJsonHttpMessageConverter {
        +setSupportedMediaTypes(List~MediaType~ mediaTypes) void
        +setFastJsonConfig(FastJsonConfig config) void
    }

    class FastJsonConfig {
        +setSerializerFeatures(SerializerFeature... features) void
        +getSerializeFilters() SerializeFilter[]
        +setSerializeFilters(SerializeFilter[] filters) void
    }

    class SerializeConfig {
        <<Interface>>
        +propertyNamingStrategy PropertyNamingStrategy
    }

    class SerializeFilter {
        <<Interface>>
    }

    class SecretValueFilter {
        +instance SerializeFilter
    }

    AppConfig --> CommonConfig : "依赖"
    AppConfig --> CorsConfiguration : "创建"
    AppConfig --> FilterRegistrationBean : "创建"
    AppConfig --> HttpMessageConverters : "创建"
    FilterRegistrationBean --> MyCorsFilter : "包含"
    HttpMessageConverters --> FastJsonHttpMessageConverter : "包含"
    FastJsonHttpMessageConverter --> FastJsonConfig : "配置"
    FastJsonConfig --> SerializeFilter : "使用"
    SerializeConfig ..|> PropertyNamingStrategy : "实现"
    SecretValueFilter ..|> SerializeFilter : "实现"
```

这段代码是一个Spring Boot配置类，主要实现了跨域过滤器配置和FastJSON消息转换器配置。类图中展示了AppConfig与多个组件的关系，包括CommonConfig用于获取跨域配置、CorsConfiguration设置跨域规则、FilterRegistrationBean注册过滤器、以及FastJsonHttpMessageConverter处理JSON序列化。通过依赖注入和对象创建，实现了跨域请求处理和JSON响应格式的自定义配置。


### 内部方法调用关系图

```mermaid
graph TD
    A["类AppConfig"]
    B["属性: CommonConfig commonConfig"]
    C["方法: onApplicationEvent(ContextRefreshedEvent)"]
    D["方法: corsFilter()"]
    E["方法: fastJsonHttpMessageConverters()"]
    F["创建CorsConfiguration对象"]
    G["获取corsAllowedOrigins配置"]
    H["循环添加允许的origin"]
    I["设置CORS通用配置"]
    J["创建FilterRegistrationBean"]
    K["设置FastJson全局命名策略"]
    L["创建FastJsonHttpMessageConverter"]
    M["配置MediaType支持"]
    N["配置FastJson序列化特性"]
    O["追加SecretValueFilter"]
    P["组装HttpMessageConverters"]

    A --> B
    A --> C
    A --> D
    A --> E
    D --> F
    D --> G
    G -->|有配置| H
    G -->|无配置| I
    H --> I
    I --> J
    E --> K
    E --> L
    L --> M
    L --> N
    N --> O
    O --> P
```

这段代码是Spring Boot的配置类，主要实现两个核心功能：1) 配置跨域过滤器(CORS)，通过读取CommonConfig中的允许来源列表，设置跨域访问规则；2) 配置FastJson作为JSON消息转换器，设置全局序列化策略、支持媒体类型和自定义过滤器。流程图清晰展示了配置初始化和处理逻辑的分支路径，特别是跨域配置的优先级处理和FastJson的多层配置过程。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| commonConfig | CommonConfig | 代码片段使用@Autowired注解自动注入CommonConfig依赖。 |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| onApplicationEvent | void | 这是一个Spring框架中的事件监听方法，用于处理应用上下文刷新完成事件。 |
| corsFilter | FilterRegistrationBean | 定义一个CORS过滤器Bean，配置允许的源、头、方法，设置缓存时间和凭证许可，注册为优先级最高的过滤器。 |
| fastJsonHttpMessageConverters | HttpMessageConverters | 配置FastJson转换器，全局使用下划线命名策略，支持UTF-8 JSON格式，启用字段排序、空值输出和错误忽略功能，并添加SecretValueFilter过滤器。 |




