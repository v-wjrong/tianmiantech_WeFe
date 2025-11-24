# 基础信息

|      |      |
|------|------|
| 名称 | MailServerModel |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/dto/globalconfig/MailServerModel.java |
| 包名 | com.welab.wefe.serving.service.dto.globalconfig |
| 依赖项 | ['com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.fieldvalidate.secret.MaskStrategy', 'com.welab.wefe.common.fieldvalidate.secret.Secret', 'com.welab.wefe.serving.service.dto.globalconfig.base.AbstractConfigModel', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigGroupConstant', 'com.welab.wefe.serving.service.dto.globalconfig.base.ConfigModel'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MailServerModel | class |  |



## 类 MailServerModel

|      |      |
|------|------|
| 访问范围 | @ConfigModel(group = ConfigGroupConstant.MAIL_SERVER);public |
| 类型 | class |
| 名称 | MailServerModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| username | String |  |
| host | String |  |
| password | String |  |
| port | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getUsername | String |  |
| setHost | void |  |
| setPort | void |  |
| getPort | String |  |
| getHost | String |  |
| setUsername | void |  |
| getPassword | String |  |
| setPassword | void |  |




