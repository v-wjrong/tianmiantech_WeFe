# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilters |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-core/src/main/java/com/welab/wefe/fusion/core/utils/bf/BloomFilters.java |
| 包名 | com.welab.wefe.fusion.core.utils.bf |
| 依赖项 | ['com.google.common.base.Preconditions', 'java.io', 'java.nio.charset.Charset', 'java.security.MessageDigest', 'java.security.NoSuchAlgorithmException', 'java.util.BitSet', 'java.util.Collection'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilters | class |  |



## 类 BloomFilters

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BloomFilters |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| bitSetSize | int |  |
| expectedNumberOfFilterElements | int |  |
| serialVersionUID = -2326638072608273135L | long |  |
| bitsPerElement | double |  |
| bitset | BitSet |  |
| HASHNAME = "MD5" | String |  |
| k | int |  |
| CHARSET = Charset.forName("UTF-8") | Charset |  |
| DIGESTFUNCTION | MessageDigest |  |
| numberOfAddedElements | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clear | void |  |
| getK | int |  |
| add | void |  |
| getBit | boolean |  |
| createHash | long |  |
| createHash | long |  |
| setBit | void |  |
| getFalsePositiveProbability | double |  |
| createHash | long |  |
| getFalsePositiveProbability | double |  |
| addAll | void |  |
| contains | boolean |  |
| getBitSet | BitSet |  |
| size | int |  |
| getExpectedNumberOfElements | int |  |
| getExpectedBitsPerElement | double |  |
| getBitsPerElement | double |  |
| writeTo | void |  |
| readFrom | BloomFilters |  |
| expectedFalsePositiveProbability | double |  |
| equals | boolean |  |
| hashCode | int |  |
| containsAll | boolean |  |
| count | int |  |




