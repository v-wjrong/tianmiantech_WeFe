# Basic Information

|      |      |
|------|------|
| Name | JobMemberService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/JobMemberService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.welab.wefe.board.service.database.entity.job.JobMemberMySqlModel', 'com.welab.wefe.board.service.database.repository.JobMemberRepository', 'com.welab.wefe.board.service.dto.entity.job.JobMemberOutputModel', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.domain.Sort', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| JobMemberService | class |  |



## Class JobMemberService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | JobMemberService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| repo | JobMemberRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findListByJobId | List<JobMemberMySqlModel> |  |
| findOneByJobRole | JobMemberMySqlModel |  |
| list | List<JobMemberOutputModel> |  |
| list | List<JobMemberOutputModel> |  |
| findIdByMemberInfo | JobMemberMySqlModel |  |
| isLocalJob | boolean |  |




