# Basic Information

|      |      |
|------|------|
| Name | ServingService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/ServingService.java |
| Package Name | com.welab.wefe.serving.service |
| Dependencies | ['org.springframework.beans.BeansException', 'org.springframework.boot.autoconfigure.SpringBootApplication', 'org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration', 'org.springframework.context.ApplicationContext', 'org.springframework.context.ApplicationContextAware', 'org.springframework.context.annotation.ComponentScan', 'org.springframework.scheduling.annotation.EnableScheduling', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.config.ApiBeanNameGenerator', 'com.welab.wefe.serving.sdk.manager.ModelProcessorManager', 'com.welab.wefe.serving.service.feature.CodeFeatureDataHandler', 'com.welab.wefe.serving.service.utils.sign.VerifySignUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ServingService | class |  |



## Class ServingService

|      |      |
|------|------|
| Access Modifier | @EnableScheduling;@SpringBootApplication(exclude = {DataSourceAutoConfiguration.class});@ComponentScan(nameGenerator = ApiBeanNameGenerator.class,;        basePackageClasses = {Launcher.class, ServingService.class});public |
| Type | class |
| Name | ServingService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| setApplicationContext | void |  |
| main | void |  |




