# Basic Information

|      |      |
|------|------|
| Name | AbstractDataResourceAddService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/add/AbstractDataResourceAddService.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.add |
| Dependencies | ['com.welab.wefe.board.service.base.file_system.WeFeFileSystem', 'com.welab.wefe.board.service.database.entity.data_resource.BloomFilterMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.DataResourceMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.DataResourceUploadTaskMysqlModel', 'com.welab.wefe.board.service.database.entity.data_resource.TableDataSetMysqlModel', 'com.welab.wefe.board.service.dto.vo.data_resource.AbstractDataResourceUpdateInputModel', 'com.welab.wefe.board.service.dto.vo.data_resource.DataResourceAddOutputModel', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.DataSetStorageService', 'com.welab.wefe.board.service.service.ServiceCheckService', 'com.welab.wefe.board.service.service.checkpoint.StorageCheckpoint', 'com.welab.wefe.board.service.service.data_resource.DataResourceService', 'com.welab.wefe.board.service.service.data_resource.DataResourceUploadTaskService', 'com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.wefe.checkpoint.dto.ServiceCheckPointOutput', 'com.welab.wefe.common.wefe.enums.DataResourceStorageServiceType', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'org.modelmapper.ModelMapper', 'org.springframework.beans.factory.annotation.Autowired'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractDataResourceAddService | class |  |



## Class AbstractDataResourceAddService

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractDataResourceAddService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataResourceService | DataResourceService |  |
| storageCheckpoint | StorageCheckpoint |  |
| dataResourceUploadTaskService | DataResourceUploadTaskService |  |
| serviceCheckService | ServiceCheckService |  |
| dataSetStorageService | DataSetStorageService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getDataResourceType | DataResourceType |  |
| doAdd | void |  |
| getMysqlModelClass | Class<? extends DataResourceMysqlModel> |  |
| add | DataResourceAddOutputModel |  |
| checkAndSetStorageLocation | void |  |




