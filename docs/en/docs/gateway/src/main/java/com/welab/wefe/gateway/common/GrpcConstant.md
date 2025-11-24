# Basic Information

|      |      |
|------|------|
| Name | GrpcConstant |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/common/GrpcConstant.java |
| Package Name | com.welab.wefe.gateway.common |
| Dependencies | ['io.grpc.Metadata'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| GrpcConstant | class |  |



## Class GrpcConstant

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | GrpcConstant |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
|-------|-------|------|




