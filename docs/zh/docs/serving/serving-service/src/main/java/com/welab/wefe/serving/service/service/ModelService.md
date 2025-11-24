# 基础信息

|      |      |
|------|------|
| 名称 | ModelService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ModelService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.common.wefe.enums.PredictFeatureDataSource', 'com.welab.wefe.serving.service.api.model.EnableApi', 'com.welab.wefe.serving.service.api.model.QueryApi', 'com.welab.wefe.serving.service.api.model.SaveModelApi', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.repository.ModelMemberRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.dto.MemberParams', 'com.welab.wefe.serving.service.dto.ModelStatusOutput', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.MemberModelStatusEnum', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum', 'com.welab.wefe.serving.service.manager.ModelManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.util.Date', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelService | class |  |



## 类 ModelService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ModelService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| partnerService | PartnerService |  |
| API_PREFIX_1 = "/api/" | String |  |
| clientServiceService | ClientServiceService |  |
| modelRepository | TableModelRepository |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| modelMemberRepository | ModelMemberRepository |  |
| API_PREFIX_2 = "predict/" | String |  |
| modelMemberService | ModelMemberService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| findOne | TableModelMySqlModel |  |
| activate | void |  |
| convertTo | TableModelMySqlModel |  |
| findByModelIdAndMemberId | List<ModelMemberMySqlModel> |  |
| bulidOutputs | List<QueryApi.Output> |  |
| save | String |  |
| queryModelMembers | PagingOutput<ModelMemberMySqlModel> |  |
| query | PagingOutput<QueryApi.Output> |  |
| setModelServiceUrl | String |  |
| upsertModel | String |  |
| saveModelMembers | void |  |
| buildQueryMemberParam | Specification<ModelMemberMySqlModel> |  |
| openPartnerService | void |  |
| findByModelIdAndMemberIdAndRole | ModelMemberMySqlModel |  |
| openService | void |  |
| activatePartnerService | void |  |
| queryModels | PagingOutput<TableModelMySqlModel> |  |
| buildQueryModelParam | Specification<TableModelMySqlModel> |  |
| enable | void |  |
| getAvailableStatus | MemberModelStatusEnum |  |
| updateConfig | void |  |
| checkAvailable | ModelStatusOutput |  |
| openService | void |  |
| setRole | QueryApi.Output |  |
| addPartners | void |  |




