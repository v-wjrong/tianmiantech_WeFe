# Basic Information

|      |      |
|------|------|
| Name | PartnerConfigService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/PartnerConfigService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'com.welab.wefe.board.service.api.partner_config.AddApi', 'com.welab.wefe.board.service.api.partner_config.QueryApi', 'com.welab.wefe.board.service.database.entity.PartnerConfigMysqlModel', 'com.welab.wefe.board.service.database.repository.PartnerConfigRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.PartnerConfigOutputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PartnerConfigService | class |  |



## Class PartnerConfigService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | PartnerConfigService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerConfigRepository | PartnerConfigRepository |  |
| gatewayService | GatewayService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| add | String |  |
| query | PagingOutput<PartnerConfigOutputModel> |  |
| delete | void |  |




