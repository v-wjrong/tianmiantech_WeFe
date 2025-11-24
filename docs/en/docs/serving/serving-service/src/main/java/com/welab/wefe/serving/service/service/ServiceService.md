# Basic Information

|      |      |
|------|------|
| Name | ServiceService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ServiceService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['java.io.File', 'java.io.FileOutputStream', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.text.SimpleDateFormat', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.Date', 'java.util.HashMap', 'java.util.HashSet', 'java.util.List', 'java.util.Map', 'java.util.Map.Entry', 'java.util.Optional', 'java.util.Queue', 'java.util.TreeMap', 'java.util.UUID', 'java.util.concurrent.BlockingQueue', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.LinkedBlockingQueue', 'java.util.concurrent.TimeUnit', 'java.util.stream.Collectors', 'org.apache.commons.collections.CollectionUtils', 'org.apache.commons.collections4.MapUtils', 'org.apache.commons.io.FileUtils', 'org.apache.commons.lang3.SerializationUtils', 'org.apache.commons.lang3.StringUtils', 'org.apache.commons.text.StringSubstitutor', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.google.common.cache.Cache', 'com.google.common.cache.CacheBuilder', 'com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.http.HttpRequest', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.Algorithm', 'com.welab.wefe.common.wefe.enums.FederatedLearningType', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostDecisionTreeModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostModel', 'com.welab.wefe.serving.sdk.model.xgboost.XgboostNodeModel', 'com.welab.wefe.serving.service.api.service.AddApi', 'com.welab.wefe.serving.service.api.service.DetailApi', 'com.welab.wefe.serving.service.api.service.QueryApi', 'com.welab.wefe.serving.service.api.service.QueryOneApi', 'com.welab.wefe.serving.service.api.service.RouteApi', 'com.welab.wefe.serving.service.api.service.ServiceSQLTestApi.Output', 'com.welab.wefe.serving.service.api.service.UpdateApi.Input', 'com.welab.wefe.serving.service.config.Config', 'com.welab.wefe.serving.service.database.entity.AccountMySqlModel', 'com.welab.wefe.serving.service.database.entity.BaseServiceMySqlModel', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.entity.DataSourceMySqlModel', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.entity.ServiceCallLogMysqlModel', 'com.welab.wefe.serving.service.database.entity.ServiceOrderMysqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableServiceMySqlModel', 'com.welab.wefe.serving.service.database.repository.AccountRepository', 'com.welab.wefe.serving.service.database.repository.BaseServiceRepository', 'com.welab.wefe.serving.service.database.repository.ModelMemberRepository', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.database.repository.TableServiceRepository', 'com.welab.wefe.serving.service.dto.ModelSqlConfigOutput', 'com.welab.wefe.serving.service.dto.ModelStatusOutput', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.dto.ServiceDetailOutput', 'com.welab.wefe.serving.service.dto.TreeNode', 'com.welab.wefe.serving.service.dto.TreeNodeData', 'com.welab.wefe.serving.service.enums.CallByMeEnum', 'com.welab.wefe.serving.service.enums.ServiceOrderEnum', 'com.welab.wefe.serving.service.enums.ServiceResultEnum', 'com.welab.wefe.serving.service.enums.ServiceStatusEnum', 'com.welab.wefe.serving.service.enums.ServiceTypeEnum', 'com.welab.wefe.serving.service.manager.FeatureManager', 'com.welab.wefe.serving.service.manager.ModelManager', 'com.welab.wefe.serving.service.service_processor.AbstractServiceProcessor', 'com.welab.wefe.serving.service.service_processor.ServiceProcessorUtils', 'com.welab.wefe.serving.service.utils.ServiceUtil', 'com.welab.wefe.serving.service.utils.SignUtils', 'com.welab.wefe.serving.service.utils.ZipUtils', 'com.welab.wefe.serving.service.utils.component.ScoreCardComponentUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServiceService | class |  |



## Class ServiceService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | ServiceService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| serviceOrderService | ServiceOrderService |  |
| dataSourceService | DataSourceService |  |
| SERVICE_PRE_URL = "api/" | String |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| partnerService | PartnerService |  |
| modelRepository | TableModelRepository |  |
| modelMemberRepository | ModelMemberRepository |  |
| config | Config |  |
| modelMemberService | ModelMemberService |  |
| serviceRepository | TableServiceRepository |  |
| unionServiceService | UnionServiceService |  |
| serviceCallLogService | ServiceCallLogService |  |
| baseServiceRepository | BaseServiceRepository<BaseServiceMySqlModel> |  |
| threads = Math.max(Runtime.getRuntime().availableProcessors(), 4) | int |  |
| clientServiceService | ClientServiceService |  |
| caches = CacheBuilder.newBuilder()            .expireAfterAccess(10, TimeUnit.MINUTES).build() | Cache<String, Object> |  |
| accountRepository | AccountRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateIdsTable | String |  |
| query | PagingOutput<QueryApi.Output> |  |
| log | void |  |
| isIpWhiteList | boolean |  |
| sqlTest | Output |  |
| modelServiceSdk | File |  |
| detailModel | com.welab.wefe.serving.service.api.service.DetailApi.Output |  |
| executeService | JObject |  |
| onlineService | void |  |
| exportSdk | File |  |
| detail | com.welab.wefe.serving.service.api.service.DetailApi.Output |  |
| findMyRoles | List<JobMemberRole> |  |
| saveService | com.welab.wefe.serving.service.api.service.AddApi.Output |  |
| callLog | void |  |
| offlineService | void |  |
| generateMySqlIdsTable | String |  |
| check | JObject |  |
| recursive | void |  |
| detailService | com.welab.wefe.serving.service.api.service.DetailApi.Output |  |
| findById | TableServiceMySqlModel |  |
| createOrder | String |  |
| updateService | com.welab.wefe.serving.service.api.service.AddApi.Output |  |
| showSql | com.welab.wefe.serving.service.api.service.ServiceShowSQLApi.Output |  |
| getModelStatus | List<ModelStatusOutput> |  |
| xgboost | List<TreeNode> |  |
| displayServiceQueryParams | String |  |
| mpcServiceSdk | File |  |
| fillReadmeFile | void |  |
| queryById | ServiceDetailOutput |  |
| callOtherPartnerServing | T |  |
| getErrorMessage | String |  |
| checkModelStatus | List<ModelStatusOutput> |  |




