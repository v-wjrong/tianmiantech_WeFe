# Basic Information

|      |      |
|------|------|
| Name | UploadRealnameAuthAgreementTemplateApi |
| Language | .java |
| Code Path | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/agreement/UploadRealnameAuthAgreementTemplateApi.java |
| Package Name | com.welab.wefe.manager.service.api.agreement |
| Dependencies | ['com.mongodb.client.gridfs.GridFSBucket', 'com.mongodb.client.gridfs.model.GridFSUploadOptions', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.union.RealnameAuthAgreementTemplate', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNode', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNodeSm2Config', 'com.welab.wefe.common.data.mongodb.repo.RealnameAuthAgreementTemplateMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.UnionNodeConfigMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.UnionNodeMongoRepo', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.Md5', 'com.welab.wefe.common.util.SM2Util', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.dto.UploadFileApiOutput', 'com.welab.wefe.manager.service.dto.common.UploadFileInput', 'com.welab.wefe.manager.service.service.RealnameAuthAgreementTemplateContractService', 'com.welab.wefe.manager.service.task.UploadFileSyncToUnionTask', 'com.welab.wefe.manager.service.util.FileCheckerUtil', 'com.welab.wefe.manager.service.util.VersionUtil', 'org.apache.http.entity.ContentType', 'org.apache.http.entity.mime.content.InputStreamBody', 'org.bson.Document', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'java.io.IOException', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| UploadRealnameAuthAgreementTemplateApi | class |  |



## Class UploadRealnameAuthAgreementTemplateApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "realname/auth/agreement/template/upload", name = "realname_auth_agreement_template_upload");public |
| Type | class |
| Name | UploadRealnameAuthAgreementTemplateApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| gridFSBucket | GridFSBucket |  |
| realnameAuthAgreementTemplateMongoRepo | RealnameAuthAgreementTemplateMongoRepo |  |
| unionNodeMongoRepo | UnionNodeMongoRepo |  |
| unionNodeConfigMongoRepo | UnionNodeConfigMongoRepo |  |
| currentBlockchainNodeId | String |  |
| contractService | RealnameAuthAgreementTemplateContractService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| handle | ApiResult<UploadFileApiOutput> |  |
| syncFileToUnion | void |  |
| buildFileStreamBodyMap | Map<String, InputStreamBody> |  |




