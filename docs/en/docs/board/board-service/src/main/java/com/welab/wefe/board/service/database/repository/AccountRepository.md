# Basic Information

|      |      |
|------|------|
| Name | AccountRepository |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/repository/AccountRepository.java |
| Package Name | com.welab.wefe.board.service.database.repository |
| Dependencies | ['com.welab.wefe.board.service.database.entity.AccountMysqlModel', 'com.welab.wefe.board.service.database.repository.base.BaseRepository', 'org.springframework.data.jpa.repository.Modifying', 'org.springframework.data.jpa.repository.Query', 'org.springframework.stereotype.Repository', 'org.springframework.transaction.annotation.Transactional'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AccountRepository | interface |  |



## Class AccountRepository

|      |      |
|------|------|
| Access Modifier | @Repository;public |
| Type | interface |
| Name | AccountRepository |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| cancelAccountWithoutAction180Days | int |  |
| updateUiConfig | void |  |
| updateLastActionTime | void |  |
| findByPhoneNumber | AccountMysqlModel |  |
| disableAccountWithoutAction90Days | int |  |
| cancelSuperAdmin | void |  |




