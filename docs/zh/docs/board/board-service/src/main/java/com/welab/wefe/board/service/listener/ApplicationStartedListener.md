# 基础信息

|      |      |
|------|------|
| 名称 | ApplicationStartedListener |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/listener/ApplicationStartedListener.java |
| 包名 | com.welab.wefe.board.service.listener |
| 依赖项 | ['cn.hutool.core.thread.ThreadUtil', 'com.welab.wefe.board.service.cache.CaCertificateCache', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.chat.MessageQueueMySqlModel', 'com.welab.wefe.board.service.database.repository.ChatUnreadMessageRepository', 'com.welab.wefe.board.service.service.DataSetStorageService', 'com.welab.wefe.board.service.service.MemberChatService', 'com.welab.wefe.board.service.service.PrivacyDatabaseEncryptService', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.wefe.dto.global_config.PrivacyConfigModel', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.boot.context.event.ApplicationStartedEvent', 'org.springframework.context.ApplicationListener', 'org.springframework.stereotype.Component', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ApplicationStartedListener | class |  |



## 类 ApplicationStartedListener

|      |      |
|------|------|
| 访问范围 | @Component;public |
| 类型 | class |
| 名称 | ApplicationStartedListener |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| privacyDatabaseEncryptService | PrivacyDatabaseEncryptService |  |
| dataSetStorageService | DataSetStorageService |  |
| globalConfigService | GlobalConfigService |  |
| config | Config |  |
| LOG = LoggerFactory.getLogger(ApplicationStartedListener.class) | Logger |  |
| memberChatService | MemberChatService |  |
| statUnreadMessageRepository | ChatUnreadMessageRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| startChatListener | void |  |
| onApplicationEvent | void |  |
| loadCaCertificate | void |  |
| privacyDatabaseEncrypt | void |  |




