# Basic Information

|      |      |
|------|------|
| Name | BloomFilters |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/utils/bf/BloomFilters.java |
| Package Name | com.welab.wefe.data.fusion.service.utils.bf |
| Dependencies | ['java.io.DataInputStream', 'java.io.DataOutputStream', 'java.io.IOException', 'java.io.InputStream', 'java.io.OutputStream', 'java.io.Serializable', 'java.nio.charset.Charset', 'java.security.MessageDigest', 'java.security.NoSuchAlgorithmException', 'java.util.Collection', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.google.common.base.Preconditions'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilters | class |  |



## Class BloomFilters

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BloomFilters |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
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

### Method List

| Name  | Type  | Description |
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




