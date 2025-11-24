# 基础信息

|      |      |
|------|------|
| 名称 | CertDao |
| 编码语言 | .java |
| 代码路径 | WeFe/manager/manager-service/src/main/java/com/webank/cert/mgr/db/dao/CertDao.java |
| 包名 | com.webank.cert.mgr.db.dao |
| 依赖项 | ['java.util.List', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mongodb.dto.PageOutput', 'com.welab.wefe.common.data.mongodb.entity.manager.CertInfo', 'com.welab.wefe.common.data.mongodb.entity.manager.CertKeyInfo', 'com.welab.wefe.common.data.mongodb.entity.manager.CertRequestInfo', 'com.welab.wefe.common.data.mongodb.repo.CertInfoRepo', 'com.welab.wefe.common.data.mongodb.repo.CertKeyInfoRepo', 'com.welab.wefe.common.data.mongodb.repo.CertRequestInfoRepo'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CertDao | class |  |



## 类 CertDao

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | CertDao |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| certKeyInfoRepo | CertKeyInfoRepo |  |
| certRequestInfoRepo | CertRequestInfoRepo |  |
| certInfoRepo | CertInfoRepo |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| findCertRequestList | PageOutput<CertRequestInfo> |  |
| findCertById | CertInfo |  |
| findCertList | List<CertInfo> |  |
| findByPCertIdAndSubjectKeyId | CertRequestInfo |  |
| findCertRequestById | CertRequestInfo |  |
| save | CertRequestInfo |  |
| findKeyByUserId | List<CertKeyInfo> |  |
| updateStatusByUserId | void |  |
| findCertList | PageOutput<CertInfo> |  |
| findKeyByPkId | CertKeyInfo |  |
| findCertKeyById | CertKeyInfo |  |
| updateStatusBySerialNumber | void |  |
| findKeys | PageOutput<CertKeyInfo> |  |
| save | CertInfo |  |
| findBySerialNumber | CertInfo |  |
| updateCanTrust | void |  |
| save | CertKeyInfo |  |




