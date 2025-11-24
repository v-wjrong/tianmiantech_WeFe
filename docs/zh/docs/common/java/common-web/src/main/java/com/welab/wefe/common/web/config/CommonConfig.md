# 基础信息

|      |      |
|------|------|
| 名称 | CommonConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/config/CommonConfig.java |
| 包名 | com.welab.wefe.common.web.config |
| 依赖项 | ['com.welab.wefe.common.wefe.enums.env.EnvBranch', 'com.welab.wefe.common.wefe.enums.env.EnvName', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.stereotype.Component'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CommonConfig | class |  |



## 类 CommonConfig

|      |      |
|------|------|
| 访问范围 | @Component("commonConfig");public |
| 类型 | class |
| 名称 | CommonConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| databaseEncryptEnable | boolean |  |
| databaseEncryptSecretKey | String |  |
| envBranch | EnvBranch |  |
| fileUploadDir | String |  |
| envName | EnvName |  |
| loggingFilePath | String |  |
| unionBaseUrl | String |  |
| corsAllowedOrigins | String[] |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setEnvBranch | void |  |
| getFileUploadDir | String |  |
| setUnionBaseUrl | void |  |
| setCorsAllowedOrigins | void |  |
| getEnvBranch | EnvBranch |  |
| getCorsAllowedOrigins | String[] |  |
| getLoggingFilePath | String |  |
| setLoggingFilePath | void |  |
| getUnionBaseUrl | String |  |
| setEnvName | void |  |
| getEnvName | EnvName |  |
| isOnlineDemo | boolean |  |
| setFileUploadDir | void |  |
| setDatabaseEncryptEnable | void |  |
| getDatabaseEncryptSecretKey | String |  |
| setDatabaseEncryptSecretKey | void |  |
| isDatabaseEncryptEnable | boolean |  |




