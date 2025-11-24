# Basic Information

|      |      |
|------|------|
| Name | ChatLastAccountService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ChatLastAccountService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.chat.AddChatLastAccountApi', 'com.welab.wefe.board.service.api.chat.DeleteChatLastAccountApi', 'com.welab.wefe.board.service.base.LoginAccountInfo', 'com.welab.wefe.board.service.database.entity.chat.ChatLastAccountMysqlModel', 'com.welab.wefe.board.service.database.entity.chat.ChatUnreadMessageMySqlModel', 'com.welab.wefe.board.service.database.repository.ChatLastAccountRepository', 'com.welab.wefe.board.service.database.repository.ChatUnreadMessageRepository', 'com.welab.wefe.board.service.dto.entity.ChatLastAccountOutputModel', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.ArrayList', 'java.util.Date', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ChatLastAccountService | class |  |



## Class ChatLastAccountService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ChatLastAccountService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| chatLastAccountRepository | ChatLastAccountRepository |  |
| chatUnreadMessageRepository | ChatUnreadMessageRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| add | void |  |
| add | void |  |
| query | List<ChatLastAccountOutputModel> |  |
| delete | void |  |
| refreshLoginAccountCache | void |  |




