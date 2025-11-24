# Basic Information

|      |      |
|------|------|
| Name | ApplicationStartedListener |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/listener/ApplicationStartedListener.java |
| Package Name | com.welab.wefe.board.service.listener |
| Dependencies | ['cn.hutool.core.thread.ThreadUtil', 'com.welab.wefe.board.service.cache.CaCertificateCache', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.chat.MessageQueueMySqlModel', 'com.welab.wefe.board.service.database.repository.ChatUnreadMessageRepository', 'com.welab.wefe.board.service.service.DataSetStorageService', 'com.welab.wefe.board.service.service.MemberChatService', 'com.welab.wefe.board.service.service.PrivacyDatabaseEncryptService', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.wefe.dto.global_config.PrivacyConfigModel', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.boot.context.event.ApplicationStartedEvent', 'org.springframework.context.ApplicationListener', 'org.springframework.stereotype.Component', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ApplicationStartedListener | class |  |



## Class ApplicationStartedListener

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | ApplicationStartedListener |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| privacyDatabaseEncryptService | PrivacyDatabaseEncryptService |  |
| dataSetStorageService | DataSetStorageService |  |
| globalConfigService | GlobalConfigService |  |
| config | Config |  |
| LOG = LoggerFactory.getLogger(ApplicationStartedListener.class) | Logger |  |
| memberChatService | MemberChatService |  |
| statUnreadMessageRepository | ChatUnreadMessageRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| startChatListener | void |  |
| onApplicationEvent | void |  |
| loadCaCertificate | void |  |
| privacyDatabaseEncrypt | void |  |




