# 基础信息

|      |      |
|------|------|
| 名称 | ConfigProperties |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/config/ConfigProperties.java |
| 包名 | com.welab.wefe.gateway.config |
| 依赖项 | ['org.springframework.beans.factory.annotation.Value', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.PropertySource', 'org.springframework.stereotype.Component'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ConfigProperties | class |  |



## 类 ConfigProperties

|      |      |
|------|------|
| 访问范围 | @Component;@PropertySource(value = {"file:${config.path}"}, encoding = "utf-8");@ConfigurationProperties;public |
| 类型 | class |
| 名称 | ConfigProperties |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sendTransferMetaPersistentType | String |  |
| sendTransferMetaPersistentTempDir | String |  |
| grpcServerExternalPort | Integer |  |
| recvTransferMetaPersistentType | String |  |
| recvTransferMetaPersistentTempDir | String |  |
| dataSinkCorePoolSize | int |  |
| grpcServerInternalPort | Integer |  |
| persistentStorageBatchInsertSize | double |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setDataSinkCorePoolSize | void |  |
| setRecvTransferMetaPersistentTempDir | void |  |
| getGrpcServerInternalPort | Integer |  |
| setGrpcServerExternalPort | void |  |
| getDataSinkCorePoolSize | int |  |
| getRecvTransferMetaPersistentType | String |  |
| setPersistentStorageBatchInsertSize | void |  |
| getSendTransferMetaPersistentTempDir | String |  |
| getPersistentStorageBatchInsertSize | double |  |
| getRecvTransferMetaPersistentTempDir | String |  |
| setSendTransferMetaPersistentType | void |  |
| setRecvTransferMetaPersistentType | void |  |
| setSendTransferMetaPersistentTempDir | void |  |
| getSendTransferMetaPersistentType | String |  |
| setGrpcServerInternalPort | void |  |
| getGrpcServerExternalPort | Integer |  |




