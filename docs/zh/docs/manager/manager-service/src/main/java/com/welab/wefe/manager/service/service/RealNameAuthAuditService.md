# 基础信息

|      |      |
|------|------|
| 名称 | RealNameAuthAuditService |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/welab/wefe/manager/service/service/RealNameAuthAuditService.java |
| 包名 | com.welab.wefe.manager.service.service |
| 依赖项 | ['com.webank.cert.mgr.model.vo.CertVO', 'com.webank.cert.mgr.service.CertOperationService', 'com.webank.cert.toolkit.enums.CertStatusEnums', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.entity.manager.CertInfo', 'com.welab.wefe.common.data.mongodb.entity.union.Member', 'com.welab.wefe.common.data.mongodb.entity.union.ext.MemberExtJSON', 'com.welab.wefe.common.data.mongodb.repo.MemberMongoReop', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.manager.service.dto.member.RealNameAuthInput', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'org.springframework.util.CollectionUtils', 'javax.transaction.Transactional', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| RealNameAuthAuditService | class |  |



## 类 RealNameAuthAuditService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | RealNameAuthAuditService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| certOperationService | CertOperationService |  |
| memberMongoReop | MemberMongoReop |  |
| memberContractService | MemberContractService |  |
| LOG = LoggerFactory.getLogger(RealNameAuthAuditService.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| audit | void |  |




