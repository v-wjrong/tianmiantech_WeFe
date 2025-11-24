# 基础信息

|      |      |
|------|------|
| 名称 | PsiServerTask |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/task/PsiServerTask.java |
| 包名 | com.welab.wefe.data.fusion.service.task |
| 依赖项 | ['java.util.concurrent.CountDownLatch', 'com.welab.wefe.data.fusion.service.actuator.rsapsi.PsiServerActuator', 'com.welab.wefe.data.fusion.service.manager.ActuatorManager', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilterUtils', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PsiServerTask | class |  |



## 类 PsiServerTask

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PsiServerTask |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| src | String |  |
| latch | CountDownLatch |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| preprocess | void |  |
| findBloomFilters | BloomFilters |  |
| postprocess | void |  |




