# Basic Information

|      |      |
|------|------|
| Name | CommonService |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/service/CommonService.java |
| Package Name | com.welab.wefe.union.service.service |
| Dependencies | ['com.mongodb.client.gridfs.GridFSBucket', 'com.mongodb.client.gridfs.GridFSDownloadStream', 'com.mongodb.client.gridfs.model.GridFSFile', 'com.mongodb.client.gridfs.model.GridFSUploadOptions', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.union.MemberFileInfo', 'com.welab.wefe.common.data.mongodb.entity.union.RealnameAuthAgreementTemplate', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNode', 'com.welab.wefe.common.data.mongodb.repo.MemberFileInfoMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.RealnameAuthAgreementTemplateMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.UnionNodeMongoRepo', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.Md5', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.common.util.UrlUtil', 'com.welab.wefe.common.web.dto.AbstractWithFilesApiInput', 'com.welab.wefe.common.web.dto.UploadFileApiOutput', 'com.welab.wefe.common.wefe.enums.FileRurpose', 'com.welab.wefe.union.service.api.common.DownloadFileApi', 'com.welab.wefe.union.service.api.common.MemberFileUploadSyncApi', 'com.welab.wefe.union.service.dto.base.BaseInput', 'com.welab.wefe.union.service.dto.common.RealnameAuthAgreementTemplateOutput', 'org.apache.commons.io.IOUtils', 'org.bson.BsonObjectId', 'org.bson.BsonValue', 'org.bson.Document', 'org.bson.types.ObjectId', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.mongodb.gridfs.GridFsResource', 'org.springframework.data.mongodb.gridfs.GridFsTemplate', 'org.springframework.http', 'org.springframework.stereotype.Service', 'org.springframework.web.client.RestTemplate', 'java.io.ByteArrayInputStream', 'java.net.URLEncoder'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CommonService | class |  |



## Class CommonService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | CommonService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberFileInfoMongoRepo | MemberFileInfoMongoRepo |  |
| gridFSBucket | GridFSBucket |  |
| realnameAuthAgreementTemplateMongoRepo | RealnameAuthAgreementTemplateMongoRepo |  |
| gridFsTemplate | GridFsTemplate |  |
| unionNodeMongoRepo | UnionNodeMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| downloadFile | ResponseEntity<byte[]> |  |
| queryRealNameAuthAgreementTemplate | RealnameAuthAgreementTemplateOutput |  |
| memberFileUpload | UploadFileApiOutput |  |
| queryRealNameAuthAgreementTemplateUploadFile | UploadFileApiOutput |  |
| saveFileToCurrentNode | void |  |
| saveFileToCurrentNode | void |  |
| saveFileToCurrentNode | void |  |




