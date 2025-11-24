# 基础信息

|      |      |
|------|------|
| 名称 | ServingService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/ServingService.java |
| 包名 | com.welab.wefe.serving.service |
| 依赖项 | ['org.springframework.beans.BeansException', 'org.springframework.boot.autoconfigure.SpringBootApplication', 'org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration', 'org.springframework.context.ApplicationContext', 'org.springframework.context.ApplicationContextAware', 'org.springframework.context.annotation.ComponentScan', 'org.springframework.scheduling.annotation.EnableScheduling', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.config.ApiBeanNameGenerator', 'com.welab.wefe.serving.sdk.manager.ModelProcessorManager', 'com.welab.wefe.serving.service.feature.CodeFeatureDataHandler', 'com.welab.wefe.serving.service.utils.sign.VerifySignUtil'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ServingService | class |  |



## 类 ServingService

|      |      |
|------|------|
| 访问范围 | @EnableScheduling;@SpringBootApplication(exclude = {DataSourceAutoConfiguration.class});@ComponentScan(nameGenerator = ApiBeanNameGenerator.class,;        basePackageClasses = {Launcher.class, ServingService.class});public |
| 类型 | class |
| 名称 | ServingService |
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




