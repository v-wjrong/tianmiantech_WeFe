# 基础信息

|      |      |
|------|------|
| 名称 | MessageService |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/MessageService.java |
| 包名 | com.welab.wefe.gateway.service |
| 依赖项 | ['com.welab.wefe.gateway.api.meta.basic.BasicMetaProto', 'com.welab.wefe.gateway.api.meta.basic.GatewayMetaProto', 'com.welab.wefe.gateway.common.MessageEntityBuilder', 'com.welab.wefe.gateway.entity.MessageEntity', 'com.welab.wefe.gateway.repository.MessageRepository', 'net.jodah.expiringmap.ExpirationPolicy', 'net.jodah.expiringmap.ExpiringMap', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MessageService | class |  |



## 类 MessageService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | MessageService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(SendTransferMetaService.class) | Logger |  |
| mMessageRepository | MessageRepository |  |
| MESSAGE_CACHE = ExpiringMap            .builder()            .expirationPolicy(ExpirationPolicy.CREATED)            .expiration(60, TimeUnit.SECONDS)            .maxSize(100)            .build() | ExpiringMap<Integer, String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| saveError | void |  |
| save | void |  |
| saveError | void |  |
| saveError | void |  |




