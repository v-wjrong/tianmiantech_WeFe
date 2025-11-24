# Basic Information

|      |      |
|------|------|
| Name | ProjectDataSetAuditService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectDataSetAuditService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.api.project.dataset.AuditDataSetApi', 'com.welab.wefe.board.service.api.project.dataset.AuditDataSetApi.Input', 'com.welab.wefe.board.service.database.entity.job.ProjectDataSetMySqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectMySqlModel', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.AuditStatus', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectDataSetAuditService | class |  |



## Class ProjectDataSetAuditService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ProjectDataSetAuditService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| projectService | ProjectService |  |
| projectMemberService | ProjectMemberService |  |
| messageService | MessageService |  |
| projectDataSetService | ProjectDataSetService |  |
| tableDataSetService | TableDataSetService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| auditDataSet | void |  |




