# 基础信息

|      |      |
|------|------|
| 名称 | Validator |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/Validator.java |
| 包名 | com.welab.wefe.common |
| 依赖项 | ['java.util.regex.Pattern'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| Validator | class |  |



## 类 Validator

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | Validator |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| MATCH_UNSIGNED_INTEGER_PATTERN = Pattern.compile("^\\d+$") | Pattern |  |
| MATCH_BOOLEAN_PATTERN = Pattern.compile("^true$|^false$|^0$|^1$", Pattern.CASE_INSENSITIVE) | Pattern |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| isLong | boolean |  |
| isInteger | boolean |  |
| isDouble | boolean |  |
| isBoolean | boolean |  |
| isUnsignedInteger | boolean |  |
| isDateTime | boolean |  |




