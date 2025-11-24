# 基础信息

|      |      |
|------|------|
| 名称 | PartnerService |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/PartnerService.java |
| 包名 | com.welab.wefe.data.fusion.service.service |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.data.fusion.service.api.partner.AddApi', 'com.welab.wefe.data.fusion.service.api.partner.PagingApi', 'com.welab.wefe.data.fusion.service.api.partner.UpdateApi', 'com.welab.wefe.data.fusion.service.database.entity.PartnerMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.PartnerRepository', 'com.welab.wefe.data.fusion.service.dto.base.PagingOutput', 'org.springframework.beans.BeanUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PartnerService | class |  |



## 类 PartnerService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | PartnerService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| partnerRepository | PartnerRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| existByPartnerIdNotEqId | boolean |  |
| findByPartnerId | PartnerMySqlModel |  |
| add | void |  |
| update | void |  |
| paging | PagingOutput<PartnerMySqlModel> |  |
| delete | void |  |
| list | List<PartnerMySqlModel> |  |




