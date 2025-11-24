# Basic Information

|      |      |
|------|------|
| Name | LoginAccountInfo |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/base/LoginAccountInfo.java |
| Package Name | com.welab.wefe.board.service.base |
| Dependencies | ['com.welab.wefe.common.web.service.account.SsoAccountInfo', 'net.jodah.expiringmap.ExpirationPolicy', 'net.jodah.expiringmap.ExpiringMap', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| LoginAccountInfo | class |  |



## Class LoginAccountInfo

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | LoginAccountInfo |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOGIN_ACCOUNT_INFO = ExpiringMap.builder()            .expirationPolicy(ExpirationPolicy.ACCESSED)            .expiration(60, TimeUnit.MINUTES).build() | ExpiringMap<String, SsoAccountInfo> |  |
| loginAccountInfo = new LoginAccountInfo() | LoginAccountInfo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | LoginAccountInfo |  |
| put | void |  |
| get | SsoAccountInfo |  |




