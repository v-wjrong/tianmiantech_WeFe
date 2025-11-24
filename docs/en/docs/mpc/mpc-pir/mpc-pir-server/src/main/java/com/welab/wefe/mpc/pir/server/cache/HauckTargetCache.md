# Basic Information

|      |      |
|------|------|
| Name | HauckTargetCache |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir/mpc-pir-server/src/main/java/com/welab/wefe/mpc/pir/server/cache/HauckTargetCache.java |
| Package Name | com.welab.wefe.mpc.pir.server.cache |
| Dependencies | ['com.welab.wefe.mpc.pir.protocol.ot.hauck.HauckTarget', 'java.util.concurrent.ArrayBlockingQueue', 'java.util.concurrent.BlockingQueue'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HauckTargetCache | class |  |



## Class HauckTargetCache

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HauckTargetCache |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| sHauckTargetCache = new HauckTargetCache() | HauckTargetCache |  |
| sHauckTargetCaches = new ArrayBlockingQueue<>(500) | BlockingQueue<HauckTarget> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| get | HauckTarget |  |
| put | boolean |  |
| getInstance | HauckTargetCache |  |
| size | int |  |




