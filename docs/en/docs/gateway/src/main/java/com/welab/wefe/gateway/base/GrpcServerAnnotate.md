# Basic Information

|      |      |
|------|------|
| Name | GrpcServerAnnotate |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/base/GrpcServerAnnotate.java |
| Package Name | com.welab.wefe.gateway.base |
| Dependencies | ['com.welab.wefe.gateway.common.GrpcServerScopeEnum', 'io.grpc.BindableService', 'io.grpc.ServerInterceptor', 'java.util'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GrpcServerAnnotate | class |  |



## Class GrpcServerAnnotate

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | GrpcServerAnnotate |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| RPC_SERVER_MAP = new HashMap<>(16) | Map<String, GrpcServerAnnotate> |  |
| interceptMethods | List<String> |  |
| interceptors = new ArrayList<>() | List<Class<? extends ServerInterceptor>> |  |
| rpcBean | BindableService |  |
| classFullName | String |  |
| useScope | GrpcServerScopeEnum |  |

### Method List

| Name  | Type  | Description |
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




