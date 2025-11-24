# Basic Information

|      |      |
|------|------|
| Name | SystemInitializeService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/SystemInitializeService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.member.InitializeApi', 'com.welab.wefe.board.service.api.member.UpdateMemberInfoApi', 'com.welab.wefe.board.service.api.member.UpdateMemberLogoApi', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.BloomFilterMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.ImageDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.repository.AccountRepository', 'com.welab.wefe.board.service.database.repository.data_resource.BloomFilterRepository', 'com.welab.wefe.board.service.database.repository.data_resource.ImageDataSetRepository', 'com.welab.wefe.board.service.database.repository.data_resource.TableDataSetRepository', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.SignUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.DatabaseEncryptUtil', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.security.NoSuchAlgorithmException'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SystemInitializeService | class |  |



## Class SystemInitializeService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | SystemInitializeService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| globalConfigService | GlobalConfigService |  |
| bloomFilterRepository | BloomFilterRepository |  |
| imageDataSetRepository | ImageDataSetRepository |  |
| tableDataSetRepository | TableDataSetRepository |  |
| accountRepository | AccountRepository |  |
| config | Config |  |
| servingService | ServingService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| syncMemberToUnion | void |  |
| updateMemberInfo | void |  |
| updateMemberLogo | void |  |
| initialize | void |  |
| isInitialized | boolean |  |
| syncMemberToServing | void |  |
| updateMemberRsaKey | void |  |




