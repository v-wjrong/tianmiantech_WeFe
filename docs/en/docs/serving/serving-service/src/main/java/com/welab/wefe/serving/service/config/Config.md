# Basic Information

|      |      |
|------|------|
| Name | Config |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/config/Config.java |
| Package Name | com.welab.wefe.serving.service.config |
| Dependencies | ['com.welab.wefe.common.web.config.CommonConfig', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.PropertySource', 'org.springframework.stereotype.Component'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Config | class |  |



## Class Config

|      |      |
|------|------|
| Access Modifier | @Component;@PropertySource(value = {"file:${config.path}"}, ignoreResourceNotFound=true, encoding = "utf-8");@ConfigurationProperties;public |
| Type | class |
| Name | Config |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| emailAccountForgetPasswordSubject | String |  |
| emailAccountForgetPasswordContent | String |  |
| psiBatchSize | int |  |
| fileBasePath | String |  |
| initializeSecretKeyType | String |  |

### Method List

| Name  | Type  | Description |
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




