# Basic Information

|      |      |
|------|------|
| Name | common-proto |
| Language | .java |
| Code Path | WeFe/common/java/common-proto |
| Package Name | docs.common.java.common-proto |
| Brief Description | This is a Google Protocol Buffers (protobuf) definition file describing a protocol for intermediate data structures. It primarily includes three message types: IntermediateDataItem (key-value pair data item), BatchSerializationData (batch serialized data), and IntermediateData (intermediate data container). IntermediateData supports two storage methods: 1) a collection of multiple key-value pair data items; 2) binary data after complete serialization. The file defines the data structures and related operational methods for data exchange between different systems. |

# Description

The content defines a Protobuf protocol for intermediate data transmission, comprising three primary structures: IntermediateDataItem represents a key-value data item, BatchSerializationData denotes a serialized binary data block, and IntermediateData serves as a container supporting two storage modes (a collection of multiple data items or a single data block). The protocol distinguishes storage types via the dataFlag field and provides comprehensive serialization/deserialization support.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | This is a Google Protocol Buffers (protobuf) definition file describing a protocol for intermediate data structures. It primarily includes three message types: IntermediateDataItem (key-value pair data item), BatchSerializationData (batch serialized data), and IntermediateData (intermediate data container). IntermediateData supports two storage methods: 1) a collection of multiple key-value pair data items; 2) binary data after complete serialization. The file defines the data structures and related operational methods for data exchange between different systems. |


