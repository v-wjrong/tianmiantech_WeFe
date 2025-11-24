# 基础信息

|      |      |
|------|------|
| 名称 | UnionApiLogger |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/operation/UnionApiLogger.java |
| 包名 | com.welab.wefe.union.service.operation |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.data.mongodb.entity.common.OperationLog', 'com.welab.wefe.common.data.mongodb.repo.UnionOperationLogMongoRepo', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.delegate.api_log.AbstractApiLogger', 'com.welab.wefe.common.web.delegate.api_log.ApiLog', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.service.account.AccountInfo', 'com.welab.wefe.union.service.api.common.MemberFileUploadSyncApi', 'com.welab.wefe.union.service.api.common.RealnameAuthAgreementTemplateSyncApi', 'com.welab.wefe.union.service.api.member.FileUploadApi', 'com.welab.wefe.union.service.util.ModelMapper', 'org.springframework.stereotype.Component', 'javax.servlet.http.HttpServletRequest', 'java.util.Arrays', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UnionApiLogger | class |  |



## 类 UnionApiLogger

|      |      |
|------|------|
| 访问范围 | @Component;public |
| 类型 | class |
| 名称 | UnionApiLogger |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| compress | String |  |
| ignoreWithoutLogin | boolean |  |
| beforeSaveLog | JSONObject |  |
| getIgnoreLogApiList | List<Class<? extends AbstractApi>> |  |
| save | void |  |
| updateAccountLastActionTime | void |  |




