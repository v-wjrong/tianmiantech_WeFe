# 基础信息

|      |      |
|------|------|
| 名称 | MemberChatService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/MemberChatService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.chat.QueryChatDetailApi', 'com.welab.wefe.board.service.api.chat.UpdateToReadApi', 'com.welab.wefe.board.service.base.LoginAccountInfo', 'com.welab.wefe.board.service.constant.ChatConstant', 'com.welab.wefe.board.service.database.entity.chat.ChatLastAccountMysqlModel', 'com.welab.wefe.board.service.database.entity.chat.MemberChatMySqlModel', 'com.welab.wefe.board.service.database.entity.chat.MessageQueueMySqlModel', 'com.welab.wefe.board.service.database.repository.ChatUnreadMessageRepository', 'com.welab.wefe.board.service.database.repository.MemberChatRepository', 'com.welab.wefe.board.service.database.repository.MessageQueueRepository', 'com.welab.wefe.board.service.database.repository.MessageRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.MemberChatOutputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.service.account.SsoAccountInfo', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.GatewayProcessorType', 'com.welab.wefe.common.wefe.enums.ProducerType', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.domain.Page', 'org.springframework.data.domain.PageRequest', 'org.springframework.data.domain.Pageable', 'org.springframework.data.domain.Sort', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'javax.persistence.criteria.Predicate', 'java.util.ArrayList', 'java.util.Date', 'java.util.List', 'java.util.UUID', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberChatService | class |  |



## 类 MemberChatService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | MemberChatService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| messageQueueRepository | MessageQueueRepository |  |
| chatUnreadMessageService | ChatUnreadMessageService |  |
| chatLastAccountService | ChatLastAccountService |  |
| chatUnreadMessageRepository | ChatUnreadMessageRepository |  |
| memberChatRepository | MemberChatRepository |  |
| gatewayService | GatewayService |  |
| messageRepository | MessageRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| queryChatDetail | PagingOutput<MemberChatOutputModel> |  |
| messageUpdateToRead | void |  |
| sendMessage | JObject |  |
| handleChatMessage | void |  |
| getOneMessage | MessageQueueMySqlModel |  |
| resendMessage | void |  |
| sendMessage | JObject |  |
| generateMessageId | String |  |




