# Basic Information

|      |      |
|------|------|
| Name | FieldInfoService |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/FieldInfoService.java |
| Package Name | com.welab.wefe.data.fusion.service.service |
| Dependencies | ['com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.data.fusion.service.database.entity.FieldInfoMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.FieldInfoRepository', 'com.welab.wefe.data.fusion.service.utils.primarykey.FieldInfo', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FieldInfoService | class |  |



## Class FieldInfoService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FieldInfoService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| fieldInfoRepository | FieldInfoRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findByBusinessId | List<FieldInfoMySqlModel> |  |
| fieldInfoList | List<FieldInfo> |  |
| columnList | List<String> |  |
| saveAll | void |  |




