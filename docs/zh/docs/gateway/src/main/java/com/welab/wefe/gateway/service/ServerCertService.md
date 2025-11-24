# 基础信息

|      |      |
|------|------|
| 名称 | ServerCertService |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/ServerCertService.java |
| 包名 | com.welab.wefe.gateway.service |
| 依赖项 | ['java.util.List', 'org.apache.commons.collections4.CollectionUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.wefe.dto.global_config.ServerCertInfoModel', 'com.welab.wefe.gateway.entity.CertInfoEntity', 'com.welab.wefe.gateway.entity.CertKeyInfoEntity', 'com.welab.wefe.gateway.entity.CertRequestInfoEntity', 'com.welab.wefe.gateway.repository.CertInfoRepository', 'com.welab.wefe.gateway.repository.CertKeyInfoRepository', 'com.welab.wefe.gateway.repository.CertRequestInfoRepository', 'com.welab.wefe.gateway.util.DatabaseEncryptUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ServerCertService | class |  |



## 类 ServerCertService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ServerCertService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| certKeyInfoRepository | CertKeyInfoRepository |  |
| certInfoRepository | CertInfoRepository |  |
| certRequestInfoRepository | CertRequestInfoRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getCertInfo | ServerCertInfoModel |  |




