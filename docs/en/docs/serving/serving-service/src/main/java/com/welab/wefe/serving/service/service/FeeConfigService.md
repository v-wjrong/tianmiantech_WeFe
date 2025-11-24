# Basic Information

|      |      |
|------|------|
| Name | FeeConfigService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/FeeConfigService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['java.util.List', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.repository.PartnerRepository', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.serving.service.api.feeconfig.SaveApi', 'com.welab.wefe.serving.service.database.entity.FeeConfigMysqlModel', 'com.welab.wefe.serving.service.database.repository.FeeConfigRepository'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FeeConfigService | class |  |



## Class FeeConfigService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FeeConfigService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerRepository | PartnerRepository |  |
| feeConfigRepository | FeeConfigRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| save | FeeConfigMysqlModel |  |
| queryOne | FeeConfigMysqlModel |  |




