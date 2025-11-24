# 基础信息

|      |      |
|------|------|
| 名称 | GrpcServerAnnotate |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/base/GrpcServerAnnotate.java |
| 包名 | com.welab.wefe.gateway.base |
| 依赖项 | ['com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'io.grpc.BindableService', 'io.grpc.ServerInterceptor', 'java.util'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GrpcServerAnnotate | class |  |



## 类 GrpcServerAnnotate

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | GrpcServerAnnotate |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| RPC_SERVER_MAP = new HashMap<>(16) | Map<String, GrpcServerAnnotate> |  |
| interceptMethods | List<String> |  |
| interceptors = new ArrayList<>() | List<Class<? extends ServerInterceptor>> |  |
| rpcBean | BindableService |  |
| classFullName | String |  |
| useScope | GrpcServerScopeEnum |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setClassFullName | void |  |
| getInterceptors | List<Class<? extends ServerInterceptor>> |  |
| setInterceptors | void |  |
| getUseScope | GrpcServerScopeEnum |  |
| setUseScope | void |  |
| getInterceptMethods | List<String> |  |
| addAnnotate | void |  |
| setInterceptMethods | void |  |
| getClassFullName | String |  |
| getRpcBean | BindableService |  |
| setRpcBean | void |  |




