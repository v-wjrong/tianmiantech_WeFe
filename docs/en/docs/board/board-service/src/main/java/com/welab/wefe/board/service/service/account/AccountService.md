# Basic Information

|      |      |
|------|------|
| Name | AccountService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/account/AccountService.java |
| Package Name | com.welab.wefe.board.service.service.account |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.board.service.api.account.ListAllApi', 'com.welab.wefe.board.service.api.account.QueryMemberAccountsApi', 'com.welab.wefe.board.service.api.account.QueryOnlineApi', 'com.welab.wefe.board.service.api.account.SsoLoginApi', 'com.welab.wefe.board.service.base.LoginAccountInfo', 'com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.database.repository.AccountRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.AccountListAllOutputModel', 'com.welab.wefe.board.service.dto.entity.AccountOutputModel', 'com.welab.wefe.board.service.dto.vo.OnlineAccountOutput', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.GatewayService', 'com.welab.wefe.board.service.service.WebSocketServer', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.SecurityUtil', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.Sha1', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.service.account.SsoAccountInfo', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.DatabaseEncryptUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AccountService | class |  |



## Class AccountService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | AccountService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| globalConfigService | GlobalConfigService |  |
| accountRepository | AccountRepository |  |
| gatewayService | GatewayService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| queryOnlineAccount | List<OnlineAccountOutput> |  |
| exist | boolean |  |
| queryMemberAccounts | PagingOutput<AccountOutputModel> |  |
| listAll | List<AccountListAllOutputModel> |  |
| query | PagingOutput<AccountOutputModel> |  |
| queryAll | List<AccountMysqlModel> |  |
| ssoLogin | SsoLoginApi.Output |  |
| accountToSsoLoginOutput | SsoLoginApi.Output |  |
| updateUiConfig | void |  |




