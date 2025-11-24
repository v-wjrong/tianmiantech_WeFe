# 基础信息

|      |      |
|------|------|
| 名称 | AbstractTextWriter |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/io/text/writer/AbstractTextWriter.java |
| 包名 | com.welab.wefe.common.io.text.writer |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.common.io.text.writer.delegate.FileNameFunction', 'com.welab.wefe.common.io.text.writer.delegate.RecordToStringFunction', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.Closeable', 'java.io.IOException', 'java.util.concurrent.atomic.LongAdder'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractTextWriter | class |  |



## 类 AbstractTextWriter

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractTextWriter |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




