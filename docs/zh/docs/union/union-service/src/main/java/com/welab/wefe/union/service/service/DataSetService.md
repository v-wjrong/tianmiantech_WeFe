# 基础信息

|      |      |
|------|------|
| 名称 | DataSetService |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/DataSetService.java |
| 包名 | com.welab.wefe.union.service.service |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.dto.dataset.DataSetQueryOutput', 'com.welab.wefe.common.data.mongodb.entity.union.DataSet', 'com.welab.wefe.common.data.mongodb.repo.DataSetMongoReop', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.enums.DataResourcePublicLevel', 'com.welab.wefe.union.service.api.dataresource.dataset.nomal.DeleteApi', 'com.welab.wefe.union.service.api.dataresource.dataset.nomal.DetailApi', 'com.welab.wefe.union.service.api.dataresource.dataset.nomal.PutApi', 'com.welab.wefe.union.service.api.dataresource.dataset.nomal.QueryApi', 'com.welab.wefe.union.service.dto.dataresource.dataset.table.ApiDataSetQueryOutput', 'com.welab.wefe.union.service.dto.dataresource.dataset.table.DataSetDetailOutput', 'com.welab.wefe.union.service.service.contract.DataSetContractService', 'com.welab.wefe.union.service.service.contract.DataSetMemberPermissionContractService', 'com.welab.wefe.union.service.util.MapperUtil', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetService | class |  |



## 类 DataSetService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | DataSetService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataSetMemberPermissionContractService | DataSetMemberPermissionContractService |  |
| dataSetMongoReop | DataSetMongoReop |  |
| datasetContractService | DataSetContractService |  |
| dataSetContractService | DataSetContractService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| add | void |  |
| delete | void |  |
| detail | DataSetDetailOutput |  |
| query | PageOutput<ApiDataSetQueryOutput> |  |




