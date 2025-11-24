# 基础信息

|      |      |
|------|------|
| 名称 | FeeConfigService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/FeeConfigService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['java.util.List', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.repository.PartnerRepository', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.data.mysql.enums.OrderBy', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.serving.service.api.feeconfig.SaveApi', 'com.welab.wefe.serving.service.database.entity.FeeConfigMysqlModel', 'com.welab.wefe.serving.service.database.repository.FeeConfigRepository'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FeeConfigService | class |  |



## 类 FeeConfigService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | FeeConfigService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| partnerRepository | PartnerRepository |  |
| feeConfigRepository | FeeConfigRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| save | FeeConfigMysqlModel |  |
| queryOne | FeeConfigMysqlModel |  |




