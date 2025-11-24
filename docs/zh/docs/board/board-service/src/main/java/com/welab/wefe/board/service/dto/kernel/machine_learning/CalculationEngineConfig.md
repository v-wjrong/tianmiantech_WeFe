# 基础信息

|      |      |
|------|------|
| 名称 | CalculationEngineConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/kernel/machine_learning/CalculationEngineConfig.java |
| 包名 | com.welab.wefe.board.service.dto.kernel.machine_learning |
| 依赖项 | ['com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.CalculationEngineBaseConfigModel', 'com.welab.wefe.common.wefe.dto.global_config.calculation_engine.fc.FunctionComputeBaseConfigModel', 'com.welab.wefe.common.wefe.enums.FcCloudProvider', 'com.welab.wefe.common.wefe.enums.JobBackendType'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CalculationEngineConfig | class |  |



## 类 CalculationEngineConfig

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CalculationEngineConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| CONFIG_SERVICE = Launcher.getBean(GlobalConfigService.class) | GlobalConfigService |  |
| backend | JobBackendType |  |
| fcCloudProvider | FcCloudProvider |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| get | CalculationEngineConfig |  |




