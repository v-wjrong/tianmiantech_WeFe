# Basic Information

|      |      |
|------|------|
| Name | ClientActuator |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/fusion/actuator/ClientActuator.java |
| Package Name | com.welab.wefe.board.service.fusion.actuator |
| Dependencies | ['java.util.List', 'java.util.Set', 'java.util.concurrent.locks.ReentrantLock', 'java.util.stream.Collectors', 'com.alibaba.fastjson.JSONObject', 'com.google.common.collect.Lists', 'com.welab.wefe.board.service.api.project.fusion.actuator.psi.DownloadBFApi', 'com.welab.wefe.board.service.api.project.fusion.actuator.psi.PsiCryptoApi', 'com.welab.wefe.board.service.api.project.fusion.actuator.psi.ReceiveResultApi', 'com.welab.wefe.board.service.api.project.fusion.actuator.psi.ServerCloseApi', 'com.welab.wefe.board.service.api.project.fusion.actuator.psi.ServerSynStatusApi', 'com.welab.wefe.board.service.dto.fusion.PsiMeta', 'com.welab.wefe.board.service.service.DataSetStorageService', 'com.welab.wefe.board.service.service.GatewayService', 'com.welab.wefe.board.service.service.fusion.FieldInfoService', 'com.welab.wefe.board.service.service.fusion.FusionTaskService', 'com.welab.wefe.board.service.util.primarykey.FieldInfo', 'com.welab.wefe.board.service.util.primarykey.PrimaryKeyUtils', 'com.welab.wefe.common.data.storage.common.Constant', 'com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.model.PageInputModel', 'com.welab.wefe.common.data.storage.model.PageOutputModel', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.Base64Util', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.fusion.core.actuator.psi.AbstractPsiClientActuator', 'com.welab.wefe.fusion.core.dto.PsiActuatorMeta', 'com.welab.wefe.fusion.core.enums.FusionTaskStatus', 'com.welab.wefe.fusion.core.enums.PSIActuatorStatus'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ClientActuator | class |  |



## Class ClientActuator

|      |      |
|------|------|
| Access Modifier | @SuppressWarnings("SynchronizeOnNonFinalField");public |
| Type | class |
| Name | ClientActuator |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dstMemberId | String |  |
| fieldInfoList | List<FieldInfo> |  |
| dataSetStorageService | DataSetStorageService |  |
| gatewayService = Launcher.getBean(GatewayService.class) | GatewayService |  |
| lock = new ReentrantLock(true) | ReentrantLock |  |
| columnList | Set<String> |  |
| headers | String[] |  |
| shardSize = 50000 | int |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getBucketByIndex | List<JObject> |  |
| isServerReady | boolean |  |
| dump | void |  |
| close | void |  |
| notifyServerClose | void |  |
| init | void |  |
| bucketSize | int |  |
| downloadActuatorMeta | PsiActuatorMeta |  |
| dataTransform | byte[][] |  |
| sendFusionDataToServer | void |  |
| hashValue | String |  |




