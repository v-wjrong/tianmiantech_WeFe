# 基础信息

|      |      |
|------|------|
| 名称 | GrpcConstant |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/common/GrpcConstant.java |
| 包名 | com.welab.wefe.gateway.common |
| 依赖项 | ['io.grpc.Metadata'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GrpcConstant | class |  |



## 类 GrpcConstant

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | GrpcConstant |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| SYSTEM_TIMESTAMP_HEADER_KEY = Metadata.Key.of("system_timestamp_header_key", Metadata.ASCII_STRING_MARSHALLER) | Metadata.Key<String> |  |
| INVALID_ARGUMENT_EXP_MSG = "INVALID_ARGUMENT" | String |  |
| SIGN_KEY_UUID = "uuid" | String |  |
| SIGN_KEY_SIGN = "sign" | String |  |
| MAX_SYSTEM_TIMESTAMP_DIFF = 300 | int |  |
| SIGN_HEADER_KEY = Metadata.Key.of("sign_header_key", Metadata.ASCII_STRING_MARSHALLER) | Metadata.Key<String> |  |
| SIGN_KEY_MEMBER_ID = "memberId" | String |  |
| SIGN_KEY_DATA = "data" | String |  |
| SYSTEM_TIMESTAMP_PERMISSION_EXP_MSG = "FAILED_PRECONDITION" | String |  |
| SIGN_KEY_TIMESTAMP = "timestamp" | String |  |
| REQ_DATA_HASH_SIGN_HEADER_KEY = Metadata.Key.of("req_data_hash_sign_header_key", Metadata.ASCII_STRING_MARSHALLER) | Metadata.Key<String> |  |
| INTERCEPTOR_VERIFIED_REQ_INVALID_HEADER_KEY = Metadata.Key.of("interceptor_verify_req_invalid_header_key", Metadata.ASCII_STRING_MARSHALLER) | Metadata.Key<String> |  |
| SIGN_PERMISSION_EXP_MSG = "UNAUTHENTICATED" | String |  |
| CONNECTION_DISABLE_EXP_MSG = "UNAVAILABLE" | String |  |
| IP_PERMISSION_EXP_MSG = "PERMISSION_DENIED" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|




