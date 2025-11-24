# 基础信息

|      |      |
|------|------|
| 名称 | ModelMemberService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/ModelMemberService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.google.common.collect.Lists', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'com.welab.wefe.serving.sdk.dto.ProviderParams', 'com.welab.wefe.serving.service.database.entity.ModelMemberBaseModel', 'com.welab.wefe.serving.service.database.entity.ModelMemberMySqlModel', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.repository.ModelMemberBaseRepository', 'com.welab.wefe.serving.service.database.repository.ModelMemberRepository', 'com.welab.wefe.serving.service.dto.MemberParams', 'com.welab.wefe.serving.service.dto.ModelStatusOutput', 'com.welab.wefe.serving.service.enums.MemberModelStatusEnum', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.List', 'java.util.TreeMap', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelMemberService | class |  |



## 类 ModelMemberService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ModelMemberService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| serviceService | ServiceService |  |
| modelMemberBaseRepository | ModelMemberBaseRepository |  |
| LOG = LoggerFactory.getLogger(getClass()) | Logger |  |
| modelMemberRepository | ModelMemberRepository |  |
| partnerService | PartnerService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| findListByModelIdAndMemberId | List<ModelMemberMySqlModel> |  |
| isProvider | boolean |  |
| checkAvailableByModelIdAndMemberId | List<ModelStatusOutput> |  |
| checkAvailable | ModelStatusOutput |  |
| save | void |  |
| save | void |  |
| findProviders | List<ProviderParams> |  |
| findPartnerUrl | String |  |
| updateModelStatus | void |  |
| findModelMemberBase | List<ModelMemberBaseModel> |  |
| callProvider | ModelStatusOutput |  |
| findServingBaseUrl | String |  |




