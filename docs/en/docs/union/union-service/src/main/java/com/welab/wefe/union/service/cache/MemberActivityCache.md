# Basic Information

|      |      |
|------|------|
| Name | MemberActivityCache |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/cache/MemberActivityCache.java |
| Package Name | com.welab.wefe.union.service.cache |
| Dependencies | ['com.welab.wefe.common.data.mongodb.entity.union.Member', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'java.util.Date', 'java.util.concurrent.ConcurrentHashMap'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| MemberActivityCache | class |  |



## Class MemberActivityCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | MemberActivityCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| memberActivityCache = new MemberActivityCache() | MemberActivityCache |  |
| memberMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, Member> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getInstance | MemberActivityCache |  |
| add | void |  |
| isActivePeriod | boolean |  |




