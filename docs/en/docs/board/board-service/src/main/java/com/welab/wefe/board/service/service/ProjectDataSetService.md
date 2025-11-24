# Basic Information

|      |      |
|------|------|
| Name | ProjectDataSetService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/ProjectDataSetService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.gateway.GetDerivedDataSetDetailApi', 'com.welab.wefe.board.service.api.project.dataset.QueryDerivedDataSetApi', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.entity.job.ProjectDataSetMySqlModel', 'com.welab.wefe.board.service.database.repository.ProjectDataSetRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.data_resource.output.DataResourceOutputModel', 'com.welab.wefe.board.service.dto.entity.data_resource.output.ImageDataSetOutputModel', 'com.welab.wefe.board.service.dto.entity.data_resource.output.TableDataSetOutputModel', 'com.welab.wefe.board.service.dto.entity.job.JobMemberOutputModel', 'com.welab.wefe.board.service.dto.entity.project.data_set.DerivedProjectDataSetOutputModel', 'com.welab.wefe.board.service.dto.entity.project.data_set.ProjectDataResourceOutputModel', 'com.welab.wefe.board.service.dto.vo.JobMemberWithDataSetOutputModel', 'com.welab.wefe.board.service.service.data_resource.bloom_filter.BloomFilterService', 'com.welab.wefe.board.service.service.data_resource.image_data_set.ImageDataSetService', 'com.welab.wefe.board.service.service.data_resource.table_data_set.TableDataSetService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.common.wefe.enums.DeepLearningJobType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.function.Consumer', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ProjectDataSetService | class |  |



## Class ProjectDataSetService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ProjectDataSetService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| jobMemberService | JobMemberService |  |
| imageDataSetService | ImageDataSetService |  |
| projectDataSetRepo | ProjectDataSetRepository |  |
| tableDataSetService | TableDataSetService |  |
| bloomFilterService | BloomFilterService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findAll | List<ProjectDataSetMySqlModel> |  |
| update | void |  |
| findOne | ProjectDataSetMySqlModel |  |
| list | List<ProjectDataResourceOutputModel> |  |
| findOne | ProjectDataSetMySqlModel |  |
| listByDataSetId | List<ProjectDataSetMySqlModel> |  |
| listRawDataSet | List<ProjectDataResourceOutputModel> |  |
| listRawDataSet | List<ProjectDataResourceOutputModel> |  |
| listAllRawDataSet | List<ProjectDataSetMySqlModel> |  |
| buildDerivedProjectDataSetOutputModel | DerivedProjectDataSetOutputModel |  |
| getDerivedDataSetDetail | DerivedProjectDataSetOutputModel |  |
| findDataSetList | List<ProjectDataSetMySqlModel> |  |
| queryDerivedDataSet | PagingOutput<DerivedProjectDataSetOutputModel> |  |




