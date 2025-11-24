# 基础信息

|      |      |
|------|------|
| 名称 | LoginSecurityPolicy |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/LoginSecurityPolicy.java |
| 包名 | com.welab.wefe.common.web |
| 依赖项 | ['net.jodah.expiringmap.ExpiringMap', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| LoginSecurityPolicy | class |  |



## 类 LoginSecurityPolicy

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | LoginSecurityPolicy |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| A_DARK_ROOM = ExpiringMap            .builder()            .expiration(60, TimeUnit.MINUTES)            .build() | ExpiringMap<String, Integer> |  |
| LOGIN_FAIL_COUNT_MAP = ExpiringMap            .builder()            .expiration(10, TimeUnit.MINUTES)            .build() | ExpiringMap<String, Integer> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| onLoginSuccess | void |  |
| onLoginFail | void |  |
| inDarkRoom | boolean |  |




