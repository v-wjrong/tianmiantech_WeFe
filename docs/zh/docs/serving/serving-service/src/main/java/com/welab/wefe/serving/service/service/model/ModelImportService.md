# 基础信息

|      |      |
|------|------|
| 名称 | ModelImportService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/model/ModelImportService.java |
| 包名 | com.welab.wefe.serving.service.service.model |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.service.api.model.SaveModelApi', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.dto.MemberParams', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum', 'com.welab.wefe.serving.service.service.CacheObjects', 'com.welab.wefe.serving.service.service.ModelService', 'com.welab.wefe.serving.service.utils.ServingFileUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.io.IOException', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelImportService | class |  |



## 类 ModelImportService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ModelImportService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| modelRepository | TableModelRepository |  |
| modelService | ModelService |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| extractMyRole | JobMemberRole |  |
| parseFileToList | List<String> |  |
| decryptAesKey | String |  |
| decryptModel | JObject |  |
| buildModelParam | SaveModelApi.Input |  |
| saveMachineLearningModel | String |  |
| extractAlgorithm | Algorithm |  |
| extractFlType | FederatedLearningType |  |
| extractMemberParams | List<MemberParams> |  |
| saveDeepLearningModel | String |  |




