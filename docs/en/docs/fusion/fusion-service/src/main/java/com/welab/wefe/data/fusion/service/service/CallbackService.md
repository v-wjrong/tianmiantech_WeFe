# Basic Information

|      |      |
|------|------|
| Name | CallbackService |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/CallbackService.java |
| Package Name | com.welab.wefe.data.fusion.service.service |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.data.fusion.service.actuator.rsapsi.PsiClientActuator', 'com.welab.wefe.data.fusion.service.api.thirdparty.CallbackApi', 'com.welab.wefe.data.fusion.service.database.entity.PartnerMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.TaskMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.TaskRepository', 'com.welab.wefe.data.fusion.service.dto.entity.PartnerOutputModel', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus', 'com.welab.wefe.data.fusion.service.enums.TaskStatus', 'com.welab.wefe.data.fusion.service.manager.ActuatorManager', 'com.welab.wefe.data.fusion.service.task.AbstractTask', 'com.welab.wefe.data.fusion.service.task.PsiClientTask', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.data.fusion.service.task.PsiServerTask', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.net.URL', 'com.welab.wefe.common.StatusCode.DATA_NOT_FOUND'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CallbackService | class |  |



## Class CallbackService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | CallbackService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| partnerService | PartnerService |  |
| taskRepository | TaskRepository |  |
| LOG = LoggerFactory.getLogger(CallbackService.class) | Logger |  |
| taskService | TaskService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| callback | void |  |
| running | void |  |
| stop | void |  |
| getUrlHost | String |  |




