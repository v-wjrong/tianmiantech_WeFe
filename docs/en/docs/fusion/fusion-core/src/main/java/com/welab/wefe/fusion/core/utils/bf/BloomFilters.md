# Basic Information

|      |      |
|------|------|
| Name | BloomFilters |
| Language | .java |
| Code Path | WeFe/fusion/fusion-core/src/main/java/com/welab/wefe/fusion/core/utils/bf/BloomFilters.java |
| Package Name | com.welab.wefe.fusion.core.utils.bf |
| Dependencies | ['com.google.common.base.Preconditions', 'java.io', 'java.nio.charset.Charset', 'java.security.MessageDigest', 'java.security.NoSuchAlgorithmException', 'java.util.BitSet', 'java.util.Collection'] |
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

### Method List

| Name  | Type  | Description |
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




