# Basic Information

|      |      |
|------|------|
| Name | AbstractTextWriter |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/io/text/writer/AbstractTextWriter.java |
| Package Name | com.welab.wefe.common.io.text.writer |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.common.io.text.writer.delegate.FileNameFunction', 'com.welab.wefe.common.io.text.writer.delegate.RecordToStringFunction', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.Closeable', 'java.io.IOException', 'java.util.concurrent.atomic.LongAdder'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractTextWriter | class |  |



## Class AbstractTextWriter

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractTextWriter |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| encoding = "utf-8" | String |  |
| currentFilePath | String |  |
| recordToStringFunction = (record, sequence) -> JSON.toJSONString(record) | RecordToStringFunction<S> |  |
| lastActionTime = System.currentTimeMillis() | long |  |
| totalLength = new LongAdder() | LongAdder |  |
| fileNameFunction | FileNameFunction<S> |  |
| maxFileLength = Integer.MAX_VALUE | long |  |
| dataFailCounter = new LongAdder() | LongAdder |  |
| recordSeparator = System.lineSeparator() | String |  |
| dataTotalCounter = new LongAdder() | LongAdder |  |
| logger = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getRecordSeparator | String |  |
| getCurrentFilePath | String |  |
| setMaxFileLength | void |  |
| getTotalLength | long |  |
| getFailCount | long |  |
| getTotalCount | long |  |
| write | void |  |
| setEncoding | void |  |
| getEncoding | String |  |
| setRecordSeparator | void |  |
| receive | void |  |
| reset | void |  |
| getLastActionTime | long |  |
| setFileNameFunction | void |  |
| setRecordToStringFunction | void |  |




