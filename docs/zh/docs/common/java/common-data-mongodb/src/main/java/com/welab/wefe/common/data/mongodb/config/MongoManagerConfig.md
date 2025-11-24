# 基础信息

|      |      |
|------|------|
| 名称 | MongoManagerConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/config/MongoManagerConfig.java |
| 包名 | com.welab.wefe.common.data.mongodb.config |
| 依赖项 | ['com.mongodb.MongoClient', 'com.mongodb.MongoClientURI', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.BeansException', 'org.springframework.beans.factory.config.BeanDefinition', 'org.springframework.beans.factory.config.ConfigurableListableBeanFactory', 'org.springframework.beans.factory.support.BeanDefinitionBuilder', 'org.springframework.beans.factory.support.BeanDefinitionRegistry', 'org.springframework.beans.factory.support.BeanDefinitionRegistryPostProcessor', 'org.springframework.context.ApplicationContext', 'org.springframework.context.ApplicationContextAware', 'org.springframework.context.EnvironmentAware', 'org.springframework.context.annotation.Configuration', 'org.springframework.core.env.Environment', 'org.springframework.data.mongodb.MongoDbFactory', 'org.springframework.data.mongodb.MongoTransactionManager', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.SimpleMongoDbFactory'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MongoManagerConfig | class |  |



## 类 MongoManagerConfig

|      |      |
|------|------|
| 访问范围 | @Configuration;public |
| 类型 | class |
| 名称 | MongoManagerConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| environment | Environment |  |
| CONTEXT = null | ApplicationContext |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| postProcessBeanDefinitionRegistry | void |  |
| postProcessBeanFactory | void |  |
| mongoDbManagerFactory | MongoDbFactory |  |
| setApplicationContext | void |  |
| setEnvironment | void |  |




