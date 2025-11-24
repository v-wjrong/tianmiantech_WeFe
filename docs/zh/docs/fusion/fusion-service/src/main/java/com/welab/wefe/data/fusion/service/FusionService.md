# 基础信息

|      |      |
|------|------|
| 名称 | FusionService |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/FusionService.java |
| 包名 | com.welab.wefe.data.fusion.service |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.RSAUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.config.ApiBeanNameGenerator', 'com.welab.wefe.common.web.dto.SignedApiInput', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.data.fusion.service.database.entity.PartnerMySqlModel', 'com.welab.wefe.data.fusion.service.operation.FusionApiLogger', 'com.welab.wefe.data.fusion.service.service.PartnerService', 'org.springframework.beans.BeansException', 'org.springframework.boot.autoconfigure.SpringBootApplication', 'org.springframework.context.ApplicationContext', 'org.springframework.context.ApplicationContextAware', 'org.springframework.context.annotation.ComponentScan', 'org.springframework.scheduling.annotation.EnableAsync', 'org.springframework.scheduling.annotation.EnableScheduling'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FusionService | class |  |



## 类 FusionService

|      |      |
|------|------|
| 访问范围 | @SpringBootApplication;@EnableScheduling;@EnableAsync;@ComponentScan(;        nameGenerator = ApiBeanNameGenerator.class,;        basePackageClasses = {FusionService.class, Launcher.class};);public |
| 类型 | class |
| 名称 | FusionService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setApplicationContext | void |  |
| main | void |  |
| rsaVerify | void |  |




