# Basic Information

|      |      |
|------|------|
| Name | AbstractUnionService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/sdk/AbstractUnionService.java |
| Package Name | com.welab.wefe.board.service.sdk |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONException', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.api.union.MemberListApi', 'com.welab.wefe.board.service.api.union.member_auth.MemberRealnameAuthApi', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.constant.SecretKeyType', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.http.HttpContentType', 'com.welab.wefe.common.http.HttpRequest', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.util', 'com.welab.wefe.common.wefe.dto.global_config.MemberInfoModel', 'net.jodah.expiringmap.ExpiringMap', 'org.apache.http.entity.ContentType', 'org.apache.http.entity.mime.content.InputStreamBody', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'java.io.IOException', 'java.util.Map', 'java.util.TreeMap', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractUnionService | class |  |



## Class AbstractUnionService

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractUnionService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| config | Config |  |
| globalConfigService | GlobalConfigService |  |
| CACHE_MAP = ExpiringMap            .builder()            .expiration(60, TimeUnit.SECONDS)            .maxSize(500)            .build() | ExpiringMap<String, Object> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| queryMemberByPage | JSONObject |  |
| request | JSONObject |  |
| resetPublicKey | void |  |
| realnameAuth | JSONObject |  |
| uploadMemberInfo | void |  |
| realnameAuthInfoQuery | JSONObject |  |
| uploadMemberInfoExcludeLogo | void |  |
| updateMemberLogo | void |  |
| initializeSystem | void |  |
| request | JSONObject |  |
| realnameAuthAgreementTemplateQuery | JSONObject |  |
| queryMember | JSONObject |  |
| request | JSONObject |  |
| queryMember | JSONObject |  |
| queryMemberById | JSONObject |  |
| queryMemberAuthTypeList | JSONObject |  |
| queryMembers | JSONObject |  |
| uploadFile | JSONObject |  |
| request | JSONObject |  |




