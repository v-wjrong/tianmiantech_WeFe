# 基础信息

|      |      |
|------|------|
| 名称 | TempRsaCache |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/TempRsaCache.java |
| 包名 | com.welab.wefe.common.web |
| 依赖项 | ['com.welab.wefe.common.util.RSAUtil', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'net.jodah.expiringmap.ExpirationPolicy', 'net.jodah.expiringmap.ExpiringMap', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.concurrent.TimeUnit'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TempRsaCache | class |  |



## 类 TempRsaCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TempRsaCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(TempRsaCache.class) | Logger |  |
| KEY_PAIR_MAP_BY_USER = ExpiringMap            .builder()            .expirationPolicy(ExpirationPolicy.ACCESSED)            .expiration(60, TimeUnit.MINUTES)            .build() | ExpiringMap<String, RSAUtil.RsaKeyPair> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getPublicKey | String |  |
| init | void |  |
| decrypt | String |  |
| main | void |  |




