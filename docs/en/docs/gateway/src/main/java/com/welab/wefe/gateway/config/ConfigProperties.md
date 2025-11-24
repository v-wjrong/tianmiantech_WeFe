# Basic Information

|      |      |
|------|------|
| Name | ConfigProperties |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/config/ConfigProperties.java |
| Package Name | com.welab.wefe.gateway.config |
| Dependencies | ['org.springframework.beans.factory.annotation.Value', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.context.annotation.PropertySource', 'org.springframework.stereotype.Component'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ConfigProperties | class |  |



## Class ConfigProperties

|      |      |
|------|------|
| Access Modifier | @Component;@PropertySource(value = {"file:${config.path}"}, encoding = "utf-8");@ConfigurationProperties;public |
| Type | class |
| Name | ConfigProperties |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| sendTransferMetaPersistentType | String |  |
| sendTransferMetaPersistentTempDir | String |  |
| grpcServerExternalPort | Integer |  |
| recvTransferMetaPersistentType | String |  |
| recvTransferMetaPersistentTempDir | String |  |
| dataSinkCorePoolSize | int |  |
| grpcServerInternalPort | Integer |  |
| persistentStorageBatchInsertSize | double |  |

### Method List

| Name  | Type  | Description |
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




