# 基础信息

|      |      |
|------|------|
| 名称 | LoginAccountInfo |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/base/LoginAccountInfo.java |
| 包名 | com.welab.wefe.board.service.base |
| 依赖项 | ['com.welab.wefe.common.web.service.account.SsoAccountInfo', 'net.jodah.expiringmap.ExpirationPolicy', 'net.jodah.expiringmap.ExpiringMap', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| LoginAccountInfo | class |  |



## 类 LoginAccountInfo

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | LoginAccountInfo |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOGIN_ACCOUNT_INFO = ExpiringMap.builder()            .expirationPolicy(ExpirationPolicy.ACCESSED)            .expiration(60, TimeUnit.MINUTES).build() | ExpiringMap<String, SsoAccountInfo> |  |
| loginAccountInfo = new LoginAccountInfo() | LoginAccountInfo |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | LoginAccountInfo |  |
| put | void |  |
| get | SsoAccountInfo |  |




