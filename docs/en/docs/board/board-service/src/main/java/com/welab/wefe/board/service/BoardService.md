# Basic Information

|      |      |
|------|------|
| Name | BoardService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/BoardService.java |
| Package Name | com.welab.wefe.board.service |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.base.OnlineDemoApi', 'com.welab.wefe.board.service.constant.Config', 'com.welab.wefe.board.service.exception.FlowNodeException', 'com.welab.wefe.board.service.service.CacheObjects', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.RSAUtil', 'com.welab.wefe.common.util.SignUtil', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.common.web.config.ApiBeanNameGenerator', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.dto.SignedApiInput', 'com.welab.wefe.common.web.service.flowlimit.FlowLimitByIpService', 'com.welab.wefe.common.web.service.flowlimit.FlowLimitByMobileService', 'com.welab.wefe.common.wefe.checkpoint.CheckpointManager', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.BeansException', 'org.springframework.boot.autoconfigure.SpringBootApplication', 'org.springframework.context.ApplicationContext', 'org.springframework.context.ApplicationContextAware', 'org.springframework.context.annotation.ComponentScan', 'org.springframework.scheduling.annotation.EnableAsync', 'org.springframework.scheduling.annotation.EnableScheduling', 'java.nio.charset.StandardCharsets'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BoardService | class |  |



## Class BoardService

|      |      |
|------|------|
| Access Modifier | @SpringBootApplication;@EnableScheduling;@EnableAsync;@ComponentScan(;        lazyInit = true,;        nameGenerator = ApiBeanNameGenerator.class,;        basePackageClasses = {;                BoardService.class,;                Launcher.class,;                CheckpointManager.class;        };);public |
| Type | class |
| Name | BoardService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(BoardService.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| main | void |  |
| setApplicationContext | void |  |
| rsaVerify | void |  |




