# 基础信息

|      |      |
|------|------|
| 名称 | TrustCertsUpdateApi |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/api/cert/TrustCertsUpdateApi.java |
| 包名 | com.welab.wefe.manager.service.api.cert |
| 依赖项 | ['cn.hutool.core.bean.BeanUtil', 'com.webank.cert.mgr.model.vo.CertVO', 'com.webank.cert.mgr.service.CertOperationService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.entity.union.TrustCerts', 'com.welab.wefe.common.data.mongodb.repo.TrustCertsMongoRepo', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.AbstractApiOutput', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.manager.service.service.TrustCertsContractService', 'org.springframework.beans.factory.annotation.Autowired'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TrustCertsUpdateApi | class |  |



## 类 TrustCertsUpdateApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "trust/certs/update", name = "trust_certs_add");public |
| 类型 | class |
| 名称 | TrustCertsUpdateApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| trustCertsContractService | TrustCertsContractService |  |
| trustCertsMongoRepo | TrustCertsMongoRepo |  |
| certService | CertOperationService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| handle | ApiResult<AbstractApiOutput> |  |




