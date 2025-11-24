# Basic Information

|      |      |
|------|------|
| Name | PsiServiceProcessor |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service_processor/PsiServiceProcessor.java |
| Package Name | com.welab.wefe.serving.service.service_processor |
| Dependencies | ['java.util.ArrayList', 'java.util.Arrays', 'java.util.HashMap', 'java.util.LinkedHashMap', 'java.util.LinkedList', 'java.util.List', 'java.util.Map', 'java.util.Queue', 'java.util.UUID', 'java.util.concurrent.BlockingQueue', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.LinkedBlockingQueue', 'java.util.concurrent.TimeUnit', 'org.apache.commons.collections.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.mpc.cache.intermediate.CacheOperation', 'com.welab.wefe.mpc.cache.intermediate.CacheOperationFactory', 'com.welab.wefe.mpc.commom.Constants', 'com.welab.wefe.mpc.pir.request.QueryKeysRequest', 'com.welab.wefe.mpc.pir.request.naor.QueryNaorPinkasRandomResponse', 'com.welab.wefe.mpc.pir.server.service.naor.NaorPinkasRandomService', 'com.welab.wefe.mpc.psi.request.QueryPrivateSetIntersectionResponse', 'com.welab.wefe.mpc.psi.sdk.Psi', 'com.welab.wefe.mpc.psi.sdk.dh.DhPsiServer', 'com.welab.wefe.mpc.psi.sdk.ecdh.EcdhPsiServer', 'com.welab.wefe.mpc.psi.sdk.util.EcdhUtil', 'com.welab.wefe.serving.service.config.Config', 'com.welab.wefe.serving.service.database.entity.DataSourceMySqlModel', 'com.welab.wefe.serving.service.database.entity.PsiServiceResultMysqlModel', 'com.welab.wefe.serving.service.database.entity.TableServiceMySqlModel', 'com.welab.wefe.serving.service.service.PsiServiceResultService', 'com.welab.wefe.serving.service.utils.ServiceUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PsiServiceProcessor | class |  |



## Class PsiServiceProcessor

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PsiServiceProcessor |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| numPartitions | int |  |
| batchSize | int |  |
| ECDH_SERVER_MAP = new ConcurrentHashMap<>() | ConcurrentHashMap<String, EcdhPsiServer> |  |
| DATASOURCE_MAP = new ConcurrentHashMap<>() | ConcurrentHashMap<String, DataSourceMySqlModel> |  |
| DH_SERVER_MAP = new ConcurrentHashMap<>() | ConcurrentHashMap<String, DhPsiServer> |  |
| psiServiceResultService = Launcher.getBean(PsiServiceResultService.class) | PsiServiceResultService |  |
| config = Launcher.getBean(Config.class) | Config |  |
| SERVER_DATASET_SIZE = new ConcurrentHashMap<>() | ConcurrentHashMap<String, Integer> |  |
| requestId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| processECDH | JObject |  |
| process | JObject |  |
| queryFieldResults | List<String> |  |
| processPSIResultByPir | JObject |  |
| processDH | JObject |  |
| getMysqlData | List<String> |  |
| processSaveResult | JObject |  |
| processPSIResult | JObject |  |
| getDorisData | List<String> |  |
| getBatchData | List<String> |  |
| initParams | void |  |




