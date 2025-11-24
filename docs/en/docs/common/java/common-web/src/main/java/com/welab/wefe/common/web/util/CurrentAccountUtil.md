# Basic Information

|      |      |
|------|------|
| Name | CurrentAccountUtil |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/util/CurrentAccountUtil.java |
| Package Name | com.welab.wefe.common.web.util |
| Dependencies | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.UrlUtil', 'com.welab.wefe.common.web.service.account.SsoAccountInfo', 'javax.servlet.http.HttpServletRequest'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CurrentAccountUtil | class |  |



## Class CurrentAccountUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CurrentAccountUtil |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| get | SsoAccountInfo |  |
| remove | void |  |
| set | void |  |
| buildAccountInfo | SsoAccountInfo |  |




