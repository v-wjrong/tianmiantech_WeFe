# Basic Information

|      |      |
|------|------|
| Name | modelexport |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/modelexport |
| Package Name | docs.board.board-service.src.main.java.com.welab.wefe.board.service.service.modelexport |
| Brief Description | Multiple Java classes implement multi-language code generation for XGBoost and logistic regression models, including Java, Python, C#, R, etc., supporting binary and multi-class classification, and providing node processing, method signature generation, and result calculation functions. |

# Description

## Overview  
The core responsibility of this module is to enable multilingual code generation for machine learning models (XGBoost and logistic regression) and PMML format conversion, analogous to a compiler frontend that transforms abstract models into concrete language implementations. The interface specifications consist of two categories: BaseXgboostLanguage and BaseLogisticRegressionLanguage serve as base classes defining template methods, while subclasses like XgboostPythonLanguage override methods to implement language-specific logic. The LanguageSelector class (e.g., XgboostLanguageSelector) provides language adapter selection functionality.  

Key data structures include the Node class (describing node attributes of tree structures) and LANGUAGE_MAP (storing mappings for 14 languages and their implementation classes). External dependencies involve the Spring framework (e.g., ModelExportService), PMML 4.3 standards, and mathematical libraries (e.g., Sigmoid function). For instance, XgboostPmmlLanguage recursively processes nodes to generate XML, while LogisticRegressionRubyLanguage produces method templates in Ruby syntax.  

## Core Business Scenarios  
The module supports two typical workflows: model export (e.g., XgboostModelExportService preprocesses tree data and invokes language generators) and cross-language scoring (e.g., LogisticRegressionJavaScriptLanguage generates JS functions). The interaction pattern is standardized: input model parameters and language type → select adapter → generate code/PMML → return string output.  

Functional completeness is demonstrated by support for 14 languages (e.g., C#/Haskell/PowerShell) and PMML, covering binary/multiclass scenarios. Examples include XgboostGoLanguage handling multiclass Softmax and LogisticRegressionPmmlLanguage serializing regression coefficients. API types encompass service classes (ModelExportService) and generator classes (e.g., XgboostCLanguage), with integration cases including horizontal federated learning model exports and online prediction service code generation.


### Package Internal Structure View

```mermaid
graph TD
    modelexport --> XgboostJavaLanguage.java
    modelexport --> LogisticRegressionJavaScriptLanguage.java
    modelexport --> Node.java
    modelexport --> LogisticRegressionLanguageSelector.java
    modelexport --> XgboostPmmlLanguage.java
    modelexport --> XgboostPythonLanguage.java
    modelexport --> BaseXgboostLanguage.java
    modelexport --> XgboostCSharpLanguage.java
    modelexport --> XgboostHaskellLanguage.java
    modelexport --> XgboostRLanguage.java
    modelexport --> LogisticRegressionPythonLanguage.java
    modelexport --> ModelExportService.java
    modelexport --> LogisticRegressionModelExportService.java
    modelexport --> XgboostRubyLanguage.java
    modelexport --> BaseLogisticRegressionLanguage.java
    modelexport --> LogisticRegressionRubyLanguage.java
    modelexport --> LogisticRegressionCSharpLanguage.java
    modelexport --> LogisticRegressionRLanguage.java
    modelexport --> XgboostVisualBasicLanguage.java
    modelexport --> XgboostPowerShellLanguage.java
    modelexport --> LogisticRegressionCLanguage.java
    modelexport --> LogisticRegressionVisualBasicLanguage.java
    modelexport --> LogisticRegressionGoLanguage.java
    modelexport --> XgboostLanguageSelector.java
    modelexport --> XgboostDartLanguage.java
    modelexport --> XgboostPhpLanguage.java
    modelexport --> LogisticRegressionJavaLanguage.java
    modelexport --> LogisticRegressionPowerShellLanguage.java
    modelexport --> XgboostJavaScriptLanguage.java
    modelexport --> LogisticRegressionHaskellLanguage.java
    modelexport --> LogisticRegressionPmmlLanguage.java
    modelexport --> XgboostModelExportService.java
    modelexport --> XgboostGoLanguage.java
    modelexport --> LogisticRegressionPhpLanguage.java
    modelexport --> XgboostCLanguage.java
    modelexport --> LogisticRegressionDartLanguage.java
```

This flowchart displays the complete file structure under the modelexport directory, comprising 34 file nodes. These are primarily categorized into language implementation files for two machine learning model exports (Xgboost and LogisticRegression), along with base classes, selector files, and service class files. All files are directly subordinate to the modelexport directory with no deeper subdirectory hierarchy.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [XgboostJavaLanguage.java](XgboostJavaLanguage.md) | file | The `XgboostJavaLanguage` class inherits from `BaseXgboostLanguage` and is used to implement XGBoost functionality in the Java language. |
| [LogisticRegressionJavaScriptLanguage.java](LogisticRegressionJavaScriptLanguage.md) | file | The `LogisticRegressionJavaScriptLanguage` class extends `BaseLogisticRegressionLanguage` and overrides the `generatePreMethodSignNameCode` method to generate a JavaScript scoring function template. |
| [Node.java](Node.md) | file | The Node class represents a tree node, containing attributes such as site name, ID, parent and child node IDs, weight, left and right child nodes, parent node, hierarchy level, code, etc., and provides getter and setter methods. |
| [LogisticRegressionLanguageSelector.java](LogisticRegressionLanguageSelector.md) | file | The `LogisticRegressionLanguageSelector` class stores logistic regression implementations for different languages through a static mapping, returning corresponding instances based on the input language. |
| [XgboostPmmlLanguage.java](XgboostPmmlLanguage.md) | file | The XgboostPmmlLanguage class inherits from BaseXgboostLanguage and implements the functionality to convert XGBoost models into PMML format. This includes constructing header information, data dictionaries, mining models, and segmentation structures, supporting both classification and regression tasks, and ultimately outputting the PMML string. |
| [XgboostPythonLanguage.java](XgboostPythonLanguage.md) | file | The XgboostPythonLanguage class inherits from BaseXgboostLanguage and implements Python code generation logic, including node condition judgment, classification result calculation, and return logic, supporting both binary and multi-class classification tasks. |
| [BaseXgboostLanguage.java](BaseXgboostLanguage.md) | file | The `BaseXgboostLanguage` class is used to generate Java code for XGBoost models, supporting both binary classification and multi-class classification tasks. It includes functionalities such as constant definitions, tree node code generation, method signature construction, and result logic processing. The core method `buildWholeCode` integrates the preprocessing, method signature, and main code generation processes. |
| [XgboostCSharpLanguage.java](XgboostCSharpLanguage.md) | file | The `XgboostCSharpLanguage` class inherits from `BaseXgboostLanguage` and implements C# code generation logic, including the construction of scoring methods for binary and multiclass classification, as well as result calculation and return logic. |
| [XgboostHaskellLanguage.java](XgboostHaskellLanguage.md) | file | The `XgboostHaskellLanguage` class inherits from `BaseXgboostLanguage` and implements Haskell code generation logic, including classification method signatures, node code generation, and result computation logic. |
| [XgboostRLanguage.java](XgboostRLanguage.md) | file | The `XgboostRLanguage` class inherits from `BaseXgboostLanguage` and implements R language XGBoost model code generation, including binary and multi-class logic, node code generation, and formatting methods. |
| [LogisticRegressionPythonLanguage.java](LogisticRegressionPythonLanguage.md) | file | The `LogisticRegressionPythonLanguage` class inherits from `BaseLogisticRegressionLanguage`, overrides the methods for generating Python scoring method signatures and line-ending symbols, and returns no line-ending characters. |
| [ModelExportService.java](ModelExportService.md) | file | The ModelExportService handles model export, supports horizontal federated learning, invokes different model export services based on task ID, node ID, and language parameters, and logs errors while throwing exceptions when anomalies occur. |
| [LogisticRegressionModelExportService.java](LogisticRegressionModelExportService.md) | file | The `LogisticRegressionModelExportService` class provides model export functionality, generating corresponding code based on parameters and language. The `export` method processes model parameters, extracts header information, intercepts, and weights, and invokes the language interpreter to generate code. The `getXgboostLanguage` method selects the appropriate language interpreter. |
| [XgboostRubyLanguage.java](XgboostRubyLanguage.md) | file | The `XgboostRubyLanguage` class inherits from `XgboostPythonLanguage` and overrides multiple methods to generate Ruby code, including constructing classification method signatures, node condition judgments, binary and multi-class result logic, and return code. |
| [BaseLogisticRegressionLanguage.java](BaseLogisticRegressionLanguage.md) | file | The BaseLogisticRegressionLanguage class is used to generate logistic regression model code, including functionalities such as method placeholders, indentation units, generating method signatures, and body code. |
| [LogisticRegressionRubyLanguage.java](LogisticRegressionRubyLanguage.md) | file | The `LogisticRegressionRubyLanguage` class inherits from `BaseLogisticRegressionLanguage`, overriding the generation of Ruby method signature code with no line endings or return symbols. |
| [LogisticRegressionCSharpLanguage.java](LogisticRegressionCSharpLanguage.md) | file | C# Logistic Regression Class Generation Pre-Method Signature Code, Including Namespace, Static Class, and Scoring Method Framework. |
| [LogisticRegressionRLanguage.java](LogisticRegressionRLanguage.md) | file | The `LogisticRegressionRLanguage` class inherits from `BaseLogisticRegressionLanguage` and overrides the method for generating R language scoring function templates, with indented function body placeholders and no line-ending symbols. |
| [XgboostVisualBasicLanguage.java](XgboostVisualBasicLanguage.md) | file | The XgboostVisualBasicLanguage class inherits from XgboostPythonLanguage and overrides methods to generate VB code, including classification method signatures, node condition judgments, result logic calculations, and variable definitions. |
| [XgboostPowerShellLanguage.java](XgboostPowerShellLanguage.md) | file | The XgboostPowerShellLanguage class inherits from BaseXgboostLanguage and implements the code generation logic for XGBoost models in PowerShell, including core functionalities such as classification scoring, result computation, and return operations. |
| [LogisticRegressionCLanguage.java](LogisticRegressionCLanguage.md) | file | The `LogisticRegressionCLanguage` class inherits from `BaseLogisticRegressionLanguage` and overrides the `generatePreMethodSignNameCode` method to generate a C language scoring function template. |
| [LogisticRegressionVisualBasicLanguage.java](LogisticRegressionVisualBasicLanguage.md) | file | The `LogisticRegressionVisualBasicLanguage` class inherits from `BaseLogisticRegressionLanguage` and overrides the method for generating VB code, including method signatures, return statements, and variable comparison formats. |
| [LogisticRegressionGoLanguage.java](LogisticRegressionGoLanguage.md) | file | You are a professional translation assistant. Please accurately translate the following content into the target language.  Please strictly adhere to the following guidelines:  1. Maintain consistency with the original text in terms of semantics, context, and style.  2. Preserve the original hierarchical structure and numbering system in full.  3. Strictly retain all formatting elements from the original text, such as code block identifiers (```text/```, ```mermaid/```), etc.  4. Translate only the natural language content, without any format adjustments, content additions, or explanatory processing.  5. Output only the translated result of the original text, without any additional prompt messages.  Content to be translated:  Go language logistic regression class generation pre-method signature code, returning a method string containing placeholders.  Target language code: en |
| [XgboostLanguageSelector.java](XgboostLanguageSelector.md) | file | The XgboostLanguageSelector class stores Xgboost implementations for different languages through a static mapping and returns corresponding instances based on the input language. It supports 14 languages including C, C#, Dart, etc. |
| [XgboostDartLanguage.java](XgboostDartLanguage.md) | file | XgboostDartLanguage inherits from XgboostCLanguage and overrides three methods: generating Dart scoring method signatures, binary classification return code, and multiclass classification return code. |
| [XgboostPhpLanguage.java](XgboostPhpLanguage.md) | file | The XgboostPhpLanguage class inherits from BaseXgboostLanguage and implements PHP code generation logic, including core functionalities such as binary classification and multiclass model scoring function construction, variable naming, and indentation control. |
| [LogisticRegressionJavaLanguage.java](LogisticRegressionJavaLanguage.md) | file | A Java-implemented logistic regression language class, inheriting from the base logistic regression language class. |
| [LogisticRegressionPowerShellLanguage.java](LogisticRegressionPowerShellLanguage.md) | file | The `LogisticRegressionPowerShellLanguage` class inherits from `BaseLogisticRegressionLanguage` and overrides methods for generating PowerShell function signatures, variable name comparisons, and line-ending symbols. The function is named `Score`, with an array parameter `InputVector`, and variable comparisons use index-based access. |
| [XgboostJavaScriptLanguage.java](XgboostJavaScriptLanguage.md) | file | The `XgboostJavaScriptLanguage` class inherits from `BaseXgboostLanguage` and implements JavaScript code generation, including functionalities such as constructing classification method signatures, return code, and variable definitions. |
| [LogisticRegressionHaskellLanguage.java](LogisticRegressionHaskellLanguage.md) | file | Haskell logistic regression class, generating module definitions, function signatures, and placeholders without line-ending symbols or return characters, supporting indexed variable access. |
| [LogisticRegressionPmmlLanguage.java](LogisticRegressionPmmlLanguage.md) | file | The `LogisticRegressionPmmlLanguage` class inherits from `BaseLogisticRegressionLanguage` and generates logistic regression model code in PMML format, including header information, data dictionary, regression model, mining schema, and regression table. |
| [XgboostModelExportService.java](XgboostModelExportService.md) | file | XgboostModelExportService exports XGBoost models, processes tree-structured data, and generates target language code. It includes feature name mapping, tree preprocessing, node layering, and language selector functionalities. |
| [XgboostGoLanguage.java](XgboostGoLanguage.md) | file | The `XgboostGoLanguage` class inherits from `BaseXgboostLanguage` and implements XGBoost model code generation for the Go language, including binary and multi-class classification logic, mathematical computations, variable definitions, and formatted output. |
| [LogisticRegressionPhpLanguage.java](LogisticRegressionPhpLanguage.md) | file | PHP logistic regression class, generating scoring function framework and input variable index code. |
| [XgboostCLanguage.java](XgboostCLanguage.md) | file | The XgboostCLanguage class inherits from BaseXgboostLanguage and implements C language code generation, including classification method signatures, result logic, and return codes, supporting both binary and multiclass classification. |
| [LogisticRegressionDartLanguage.java](LogisticRegressionDartLanguage.md) | file | Dart language logistic regression class, rewriting the method signature code generation method to return a method template string containing placeholders.  Target language code: en |


