# Basic Information

|      |      |
|------|------|
| Name | LoginSecurityPolicy |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/LoginSecurityPolicy.java |
| Package Name | com.welab.wefe.common.web |
| Dependencies | ['net.jodah.expiringmap.ExpiringMap', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| LoginSecurityPolicy | class |  |



## Class LoginSecurityPolicy

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | LoginSecurityPolicy |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| A_DARK_ROOM = ExpiringMap            .builder()            .expiration(60, TimeUnit.MINUTES)            .build() | ExpiringMap<String, Integer> |  |
| LOGIN_FAIL_COUNT_MAP = ExpiringMap            .builder()            .expiration(10, TimeUnit.MINUTES)            .build() | ExpiringMap<String, Integer> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| onLoginSuccess | void |  |
| onLoginFail | void |  |
| inDarkRoom | boolean |  |




