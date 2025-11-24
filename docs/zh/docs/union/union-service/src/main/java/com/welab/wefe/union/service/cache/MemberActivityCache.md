# 基础信息

|      |      |
|------|------|
| 名称 | MemberActivityCache |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/cache/MemberActivityCache.java |
| 包名 | com.welab.wefe.union.service.cache |
| 依赖项 | ['com.welab.wefe.common.data.mongodb.entity.union.Member', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'java.util.Date', 'java.util.concurrent.ConcurrentHashMap'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MemberActivityCache | class |  |



## 类 MemberActivityCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MemberActivityCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| memberActivityCache = new MemberActivityCache() | MemberActivityCache |  |
| memberMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, Member> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getInstance | MemberActivityCache |  |
| add | void |  |
| isActivePeriod | boolean |  |




