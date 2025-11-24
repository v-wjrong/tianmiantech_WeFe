# 基础信息

|      |      |
|------|------|
| 名称 | CurrentAccountUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/util/CurrentAccountUtil.java |
| 包名 | com.welab.wefe.common.web.util |
| 依赖项 | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.UrlUtil', 'com.welab.wefe.common.web.service.account.SsoAccountInfo', 'javax.servlet.http.HttpServletRequest'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CurrentAccountUtil | class |  |



## 类 CurrentAccountUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CurrentAccountUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| CURRENT_ACCOUNT_INFO = new InheritableThreadLocal() | ThreadLocal<SsoAccountInfo> |  |
| IAM_HEADER_KEY_USER_ID = "x-jwt-user-id" | String |  |
| DEFAULT_ACCOUNT_ID = "ac1173fef3bc4d8493f660a66e7f004a" | String |  |
| IAM_HEADER_KEY_PHONE_NUMBER = "x-jwt-phone-number" | String |  |
| DEFAULT_ACCOUNT_PHONE_NUMBER = "18888888888" | String |  |
| DEFAULT_ACCOUNT_NAME = "admin" | String |  |
| IAM_HEADER_KEY_EMAIL = "x-jwt-email" | String |  |
| DEFAULT_ACCOUNT_EMAIL = "12346@163.com" | String |  |
| IAM_HEADER_KEY_USER_NAME = "x-jwt-user-name" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| get | SsoAccountInfo |  |
| remove | void |  |
| set | void |  |
| buildAccountInfo | SsoAccountInfo |  |




