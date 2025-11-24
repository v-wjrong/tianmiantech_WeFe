# Basic Information

|      |      |
|------|------|
| Name | AbstractModelingComponent |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/component/modeling/AbstractModelingComponent.java |
| Package Name | com.welab.wefe.board.service.component.modeling |
| Dependencies | ['com.welab.wefe.board.service.component.base.AbstractComponent', 'com.welab.wefe.board.service.component.base.filter.OutputItemFilterFunction', 'com.welab.wefe.board.service.component.base.io', 'com.welab.wefe.board.service.database.entity.job.TaskResultMySqlModel', 'com.welab.wefe.board.service.model.FlowGraphNode', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.ComponentType', 'com.welab.wefe.common.wefe.enums.TaskResultType', 'org.springframework.beans.BeanUtils', 'java.util.ArrayList', 'java.util.Comparator', 'java.util.List', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractModelingComponent | class |  |



## Class AbstractModelingComponent

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractModelingComponent |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| TRAIN_DATA_SET_FILTER = (n, item) -> ComponentType.Segment == n.getComponentType() | OutputItemFilterFunction |  |
| TEST_DATA_SET_SUPPLIER = (graph, node) -> {        // Find validation set        FlowGraphNode validationNode = graph.findValidationDataSetFromParent(node, taskType());        if (validationNode != null) {            return new NodeOutputItem(validationNode, OutputItem.of(Names.Data.EVALUATION_DATA_SET, IODataType.DataSetInstance));        }        // Find data cutting        FlowGraphNode segmentNode = graph.findOneNodeFromParent(node, ComponentType.Segment);        if (segmentNode != null) {            return new NodeOutputItem(segmentNode, OutputItem.of(Names.Data.EVALUATION_DATA_SET, IODataType.DataSetInstance));        }        return null;    } | InputSupplier |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getResult | TaskResultMySqlModel |  |




