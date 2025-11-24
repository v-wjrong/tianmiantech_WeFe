# Basic Information

|      |      |
|------|------|
| Name | MemberService |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/MemberService.java |
| Package Name | com.welab.wefe.union.service.service |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.mongodb.client.gridfs.GridFSBucket', 'com.mongodb.client.gridfs.model.GridFSFile', 'com.mongodb.client.gridfs.model.GridFSUploadOptions', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.dto.member.MemberAuthQueryOutput', 'com.welab.wefe.common.data.mongodb.dto.member.RealnameAuthInfoQueryOutput', 'com.welab.wefe.common.data.mongodb.entity.union.MemberFileInfo', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNode', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.data.mongodb.entity.union.ext.RealnameAuthFileInfo', 'com.welab.wefe.common.data.mongodb.repo.MemberAuthTypeMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.MemberMongoReop', 'com.welab.wefe.common.data.mongodb.repo.UnionNodeMongoRepo', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.Md5', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.dto.UploadFileApiOutput', 'com.welab.wefe.common.wefe.enums.FileRurpose', 'com.welab.wefe.union.service.api.member', 'com.welab.wefe.union.service.cache.UnionNodeConfigCache', 'com.welab.wefe.union.service.constant.CertStatusEnums', 'com.welab.wefe.union.service.dto.base.BaseInput', 'com.welab.wefe.union.service.dto.member.MemberQueryOutput', 'com.welab.wefe.union.service.entity.Member', 'com.welab.wefe.union.service.service.contract.MemberContractService', 'com.welab.wefe.union.service.service.contract.MemberFileInfoContractService', 'com.welab.wefe.union.service.task.UploadFileSyncToUnionTask', 'com.welab.wefe.union.service.util.FileCheckerUtil', 'com.welab.wefe.union.service.util.MapperUtil', 'org.apache.http.entity.ContentType', 'org.apache.http.entity.mime.content.InputStreamBody', 'org.bson.Document', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.mongodb.gridfs.GridFsTemplate', 'org.springframework.stereotype.Service', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'java.io.IOException', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberService | class |  |



## Class MemberService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | MemberService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| gridFsTemplate | GridFsTemplate |  |
| memberContractService | MemberContractService |  |
| memberMongoReop | MemberMongoReop |  |
| gridFSBucket | GridFSBucket |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| memberAuthTypeMongoRepo | MemberAuthTypeMongoRepo |  |
| memberFileInfoContractService | MemberFileInfoContractService |  |
| unionNodeMongoRepo | UnionNodeMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| queryAll | List<MemberQueryOutput> |  |
| queryMap | Map<String, JObject> |  |
| saveFileInfoToBlockchain | void |  |
| add | void |  |
| fileUpload | UploadFileApiOutput |  |
| syncDataToOtherUnionNode | void |  |
| apply | JObject |  |
| putUpdateField | Member |  |
| realNameAuth | void |  |
| query | PageOutput<MemberQueryOutput> |  |
| buildFileStreamBodyMap | Map<String, InputStreamBody> |  |
| update | void |  |
| queryRealNameAuthInfo | RealnameAuthInfoQueryOutput |  |
| queryAllAuthType | List<MemberAuthQueryOutput> |  |




