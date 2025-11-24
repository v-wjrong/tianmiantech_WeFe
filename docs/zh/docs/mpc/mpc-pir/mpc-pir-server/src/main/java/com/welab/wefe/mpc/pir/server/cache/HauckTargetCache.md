# 基础信息

|      |      |
|------|------|
| 名称 | HauckTargetCache |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-pir/mpc-pir-server/src/main/java/com/welab/wefe/mpc/pir/server/cache/HauckTargetCache.java |
| 包名 | com.welab.wefe.mpc.pir.server.cache |
| 依赖项 | ['com.welab.wefe.mpc.pir.protocol.ot.hauck.HauckTarget', 'java.util.concurrent.ArrayBlockingQueue', 'java.util.concurrent.BlockingQueue'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| HauckTargetCache | class |  |



## 类 HauckTargetCache

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | HauckTargetCache |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sHauckTargetCache = new HauckTargetCache() | HauckTargetCache |  |
| sHauckTargetCaches = new ArrayBlockingQueue<>(500) | BlockingQueue<HauckTarget> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| get | HauckTarget |  |
| put | boolean |  |
| getInstance | HauckTargetCache |  |
| size | int |  |




