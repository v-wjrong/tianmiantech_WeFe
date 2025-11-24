# 基础信息

|      |      |
|------|------|
| 名称 | QueryTrustCertApi |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/api/cert/QueryTrustCertApi.java |
| 包名 | com.welab.wefe.union.service.api.cert |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.entity.union.TrustCerts', 'com.welab.wefe.common.data.mongodb.repo.TrustCertsMongoRepo', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.union.service.dto.cert.TrustCertsQueryOutput', 'com.welab.wefe.union.service.util.ModelMapper', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.Date', 'java.util.List', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| QueryTrustCertApi | class |  |



## 类 QueryTrustCertApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "trust/certs/query", name = "trust_cert_query", allowAccessWithSign = true);public |
| 类型 | class |
| 名称 | QueryTrustCertApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| trustCertsMongoRepo | TrustCertsMongoRepo |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| handle | ApiResult<JObject> |  |
| transfer | TrustCertsQueryOutput |  |




