# 基础信息

|      |      |
|------|------|
| 名称 | Config |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/config/Config.java |
| 包名 | com.welab.wefe.serving.service.config |
| 依赖项 | ['com.welab.wefe.common.web.config.CommonConfig', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.PropertySource', 'org.springframework.stereotype.Component'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| Config | class |  |



## 类 Config

|      |      |
|------|------|
| 访问范围 | @Component;@PropertySource(value = {"file:${config.path}"}, ignoreResourceNotFound=true, encoding = "utf-8");@ConfigurationProperties;public |
| 类型 | class |
| 名称 | Config |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| emailAccountForgetPasswordSubject | String |  |
| emailAccountForgetPasswordContent | String |  |
| psiBatchSize | int |  |
| fileBasePath | String |  |
| initializeSecretKeyType | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFileBasePath | String |  |
| getPsiBatchSize | int |  |
| getEmailAccountForgetPasswordContent | String |  |
| setPsiBatchSize | void |  |
| getEmailAccountForgetPasswordSubject | String |  |
| setFileBasePath | void |  |
| setEmailAccountForgetPasswordSubject | void |  |
| getInitializeSecretKeyType | String |  |
| setEmailAccountForgetPasswordContent | void |  |
| setInitializeSecretKeyType | void |  |




