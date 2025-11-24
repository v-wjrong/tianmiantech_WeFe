# Basic Information

|      |      |
|------|------|
| Name | PartnerVerifySignFunction |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/utils/sign/PartnerVerifySignFunction.java |
| Package Name | com.welab.wefe.serving.service.utils.sign |
| Dependencies | ['javax.servlet.http.HttpServletRequest', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.parser.Feature', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.RSAUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.dto.SignedApiInput', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableServiceMySqlModel', 'com.welab.wefe.serving.service.database.repository.TableModelRepository', 'com.welab.wefe.serving.service.database.repository.TableServiceRepository', 'com.welab.wefe.serving.service.service.CacheObjects', 'com.welab.wefe.serving.service.service.ClientServiceService', 'com.welab.wefe.serving.service.service.PartnerService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PartnerVerifySignFunction | class |  |



## Class PartnerVerifySignFunction

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PartnerVerifySignFunction |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| rsaVerify | void |  |
| findPartnerRsaKey | String |  |
| extractServiceUrl | String |  |
| findPartner | String |  |
| extractServiceId | String |  |
| buildParams | void |  |
| findPartnerClientServiceModel | ClientServiceMysqlModel |  |
| verify | void |  |
| isModelService | boolean |  |
| isModelProviderService | boolean |  |




