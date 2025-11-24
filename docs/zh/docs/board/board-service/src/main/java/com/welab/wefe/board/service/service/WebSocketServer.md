# 基础信息

|      |      |
|------|------|
| 名称 | WebSocketServer |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/WebSocketServer.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.board.service.base.LoginAccountInfo', 'com.welab.wefe.board.service.constant.ChatConstant', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.service.account.SsoAccountInfo', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.stereotype.Component', 'javax.websocket', 'javax.websocket.server.PathParam', 'javax.websocket.server.ServerEndpoint', 'java.io.IOException', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.AtomicInteger'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| WebSocketServer | class |  |



## 类 WebSocketServer

|      |      |
|------|------|
| 访问范围 | @ServerEndpoint("/chatserver/{token}");@Component;public |
| 类型 | class |
| 名称 | WebSocketServer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| token = "" | String |  |
| memberChatService | MemberChatService |  |
| webSocketMap = new ConcurrentHashMap<>() | ConcurrentHashMap<String, WebSocketServer> |  |
| ONLINE_COUNT = new AtomicInteger(0) | AtomicInteger |  |
| log = LoggerFactory.getLogger(WebSocketServer.class) | Logger |  |
| session | Session |  |
| accountId | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




