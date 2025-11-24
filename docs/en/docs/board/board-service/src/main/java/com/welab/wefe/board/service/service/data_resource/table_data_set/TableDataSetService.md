# Basic Information

|      |      |
|------|------|
| Name | TableDataSetService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/table_data_set/TableDataSetService.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.table_data_set |
| Dependencies | ['com.welab.wefe.board.service.api.data_resource.table_data_set.TableDataSetDeleteApi', 'com.welab.wefe.board.service.base.file_system.WeFeFileSystem', 'com.welab.wefe.board.service.constant.DataSetAddMethod', 'com.welab.wefe.board.service.database.entity.DataSourceMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.DataResourceMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.database.repository.DataSourceRepository', 'com.welab.wefe.board.service.database.repository.JobMemberRepository', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.database.repository.data_resource.TableDataSetRepository', 'com.welab.wefe.board.service.dto.entity.data_resource.output.TableDataSetOutputModel', 'com.welab.wefe.board.service.dto.vo.data_resource.AbstractDataResourceUpdateInputModel', 'com.welab.wefe.board.service.dto.vo.data_resource.TableDataSetUpdateInputModel', 'com.welab.wefe.board.service.onlinedemo.OnlineDemoBranchStrategy', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.DataSetColumnService', 'com.welab.wefe.board.service.service.DataSetStorageService', 'com.welab.wefe.board.service.service.data_resource.DataResourceService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.JdbcClient', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.io.File', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TableDataSetService | class |  |



## Class TableDataSetService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | TableDataSetService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| jobRepository | JobRepository |  |
| tableDataSetRepository | TableDataSetRepository |  |
| jobMemberRepository | JobMemberRepository |  |
| featureJobRepository | JobRepository |  |
| dataSourceRepo | DataSourceRepository |  |
| dataSetStorageService | DataSetStorageService |  |
| dataSetColumnService | DataSetColumnService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| beforeUpdate | void |  |
| testSqlQuery | String |  |
| delete | void |  |
| findOneById | TableDataSetMysqlModel |  |
| delete | void |  |
| delete | void |  |
| getDataSetFile | File |  |
| findDataSetFromLocalOrUnion | TableDataSetOutputModel |  |
| getDataSourceById | DataSourceMysqlModel |  |
| query | TableDataSetMysqlModel |  |
| queryAll | List<TableDataSetMysqlModel> |  |
| save | void |  |




