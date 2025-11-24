# Basic Information

|      |      |
|------|------|
| Name | BlacklistService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/BlacklistService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.blacklist.AddApi', 'com.welab.wefe.board.service.api.blacklist.BlacklistApi', 'com.welab.wefe.board.service.api.blacklist.BlacklistMemberApi', 'com.welab.wefe.board.service.api.blacklist.DeleteApi', 'com.welab.wefe.board.service.database.entity.BlacklistMysqlModel', 'com.welab.wefe.board.service.database.repository.BlacklistRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.BlacklistOutputModel', 'com.welab.wefe.board.service.dto.entity.MemberOutputModel', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.ArrayList', 'java.util.Date', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BlacklistService | class |  |



## Class BlacklistService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | BlacklistService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| blacklistRepository | BlacklistRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| queryBlacklistMember | PagingOutput<MemberOutputModel> |  |
| list | PagingOutput<BlacklistOutputModel> |  |
| deleteFromBlacklist | void |  |
| add | void |  |




