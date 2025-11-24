# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilters |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/utils/bf/BloomFilters.java |
| 包名 | com.welab.wefe.data.fusion.service.utils.bf |
| 依赖项 | ['java.io.DataInputStream', 'java.io.DataOutputStream', 'java.io.IOException', 'java.io.InputStream', 'java.io.OutputStream', 'java.io.Serializable', 'java.nio.charset.Charset', 'java.security.MessageDigest', 'java.security.NoSuchAlgorithmException', 'java.util.Collection', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.google.common.base.Preconditions'] |
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
| bitsPerElement | double |  |
| serialVersionUID = -2326638072608273135L | long |  |
| LOG = LoggerFactory.getLogger(BloomFilters.class) | Logger |  |
| numberOfAddedElements | long |  |
| bitset | BitArray |  |
| expectedNumberOfFilterElements | long |  |
| bitSetSize | long |  |
| k | int |  |
| HASHNAME = "MD5" | String |  |
| DIGESTFUNCTION | MessageDigest |  |
| CHARSET = Charset.forName("UTF-8") | Charset |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| equals | boolean |  |
| hashCode | int |  |
| createHash | long |  |
| add | void |  |
| readFrom | BloomFilters |  |
| getK | int |  |
| getFalsePositiveProbability | double |  |
| getFalsePositiveProbability | double |  |
| createHash | long |  |
| containsAll | boolean |  |
| getBitSet | BitArray |  |
| addAll | void |  |
| size | long |  |
| createHash | long |  |
| count | long |  |
| contains | boolean |  |
| expectedFalsePositiveProbability | double |  |
| getExpectedNumberOfElements | long |  |
| getExpectedBitsPerElement | double |  |
| getBitsPerElement | double |  |
| writeTo | void |  |




