# Basic Information

|      |      |
|------|------|
| Name | DataResourceLazyUpdateTask |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/scheduler/DataResourceLazyUpdateTask.java |
| Package Name | com.welab.wefe.union.service.scheduler |
| Dependencies | ['com.welab.wefe.common.data.mongodb.entity.union.DataResource', 'com.welab.wefe.common.data.mongodb.entity.union.DataResourceLazyUpdateModel', 'com.welab.wefe.common.data.mongodb.entity.union.ImageDataSet', 'com.welab.wefe.common.data.mongodb.repo.DataResourceLazyUpdateModelMongoReop', 'com.welab.wefe.common.data.mongodb.repo.DataResourceMongoReop', 'com.welab.wefe.common.data.mongodb.repo.ImageDataSetMongoReop', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'com.welab.wefe.union.service.service.contract.DataResourceContractService', 'com.welab.wefe.union.service.service.contract.ImageDataSetContractService', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.context.annotation.Configuration', 'org.springframework.scheduling.annotation.Scheduled', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceLazyUpdateTask | class |  |



## Class DataResourceLazyUpdateTask

|      |      |
|------|------|
| Access Modifier | @Configuration;public |
| Type | class |
| Name | DataResourceLazyUpdateTask |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataResourceMongoReop | DataResourceMongoReop |  |
| imageDataSetMongoReop | ImageDataSetMongoReop |  |
| imageDataSetContractService | ImageDataSetContractService |  |
| dataResourceContractService | DataResourceContractService |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| dataResourceLazyUpdateModelMongoReop | DataResourceLazyUpdateModelMongoReop |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| startTask | void |  |




