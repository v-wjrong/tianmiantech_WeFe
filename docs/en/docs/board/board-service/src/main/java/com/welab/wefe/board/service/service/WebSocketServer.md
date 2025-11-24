# Basic Information

|      |      |
|------|------|
| Name | WebSocketServer |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/WebSocketServer.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.base.LoginAccountInfo', 'com.welab.wefe.board.service.constant.ChatConstant', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.service.account.SsoAccountInfo', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.stereotype.Component', 'javax.websocket', 'javax.websocket.server.PathParam', 'javax.websocket.server.ServerEndpoint', 'java.io.IOException', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.AtomicInteger'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| WebSocketServer | class |  |



## Class WebSocketServer

|      |      |
|------|------|
| Access Modifier | @ServerEndpoint("/chatserver/{token}");@Component;public |
| Type | class |
| Name | WebSocketServer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| token = "" | String |  |
| memberChatService | MemberChatService |  |
| webSocketMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, WebSocketServer> |  |
| ONLINE_COUNT = new AtomicInteger(0) | AtomicInteger |  |
| log = LoggerFactory.getLogger(WebSocketServer.class) | Logger |  |
| session | Session |  |
| accountId | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| onClose | void |  |
| sendToOnline | boolean |  |
| onError | void |  |
| sendMessage | void |  |
| onOpen | void |  |
| onMessage | void |  |
| responseNonchatMessage | String |  |
| responseChatMessage | String |  |
| responseMessage | String |  |




