# Basic Information

|      |      |
|------|------|
| Name | Tgz |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/file/compression/impl/Tgz.java |
| Package Name | com.welab.wefe.common.file.compression.impl |
| Dependencies | ['com.welab.wefe.common.file.compression.AbstractCompression', 'com.welab.wefe.common.file.compression.CompressionType', 'org.apache.commons.compress.archivers.tar.TarArchiveEntry', 'org.apache.commons.compress.archivers.tar.TarArchiveOutputStream', 'org.apache.commons.compress.compressors.gzip.GzipCompressorOutputStream', 'java.io.BufferedOutputStream', 'java.io.File', 'java.io.IOException', 'java.io.OutputStream', 'java.nio.file', 'java.nio.file.attribute.BasicFileAttributes'] |
| Brief Description | The Tgz class inherits from AbstractCompression and implements the doCompression method to package a directory into a tar.gz file, skipping symbolic links and logging failures. The main method tests the compression functionality and outputs the file path and size. |

# Description

The code defines a Tgz class, which inherits from the AbstractCompression abstract class and implements compression functionality in the tar.gz format. The main logic involves traversing all files in the source directory, then using TarArchiveOutputStream and GzipCompressorOutputStream to package and compress the files into the tar.gz format. During processing, symbolic link files are skipped, and error logs are recorded if access failures occur. Finally, the main method demonstrates the usage of the compression functionality, outputting the path and size of the compressed file.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Tgz | class | The Tgz class inherits from AbstractCompression and implements the doCompression method to package a directory into a tar.gz file, skipping symbolic links, logging failures, and supporting compression type retrieval. |



## Class Tgz

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | Tgz |
| Description | The Tgz class inherits from AbstractCompression and implements the doCompression method to package a directory into a tar.gz file, skipping symbolic links, logging failures, and supporting compression type retrieval. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractCompression {
        <<Abstract>>
        #abstract void doCompression(Path srcDir, String destFileName) throws IOException
        #abstract CompressionType getCompressionType()
        +File compression(String srcDirPath) File
    }

    class Tgz {
        -Logger LOG
        +void doCompression(Path srcDir, String destFileName) throws IOException
        +CompressionType getCompressionType()
        +static void main(String[] args) throws IOException
    }

    class CompressionType {
        <<Enumeration>>
        +Tgz
        +Zip
        +...
    }

    class TarArchiveOutputStream {
        +void putArchiveEntry(TarArchiveEntry entry)
        +void closeArchiveEntry()
        +void finish()
    }

    class SimpleFileVisitor~Path~ {
        <<Abstract>>
        +FileVisitResult visitFile(Path file, BasicFileAttributes attrs)
        +FileVisitResult visitFileFailed(Path file, IOException exc)
    }

    AbstractCompression <|-- Tgz
    Tgz --> TarArchiveOutputStream : uses
    Tgz --> SimpleFileVisitor~Path~ : uses
    Tgz --> CompressionType : returns

    note for Tgz "Implements TGZ format compression by combining Gzip and Tar streams\nSkips symbolic links and supports failure continuation"
```

Class diagram description: This diagram illustrates a TGZ compression implementation where the Tgz class inherits from the abstract class AbstractCompression. It achieves directory traversal compression by combining TarArchiveOutputStream and SimpleFileVisitor. The core process includes file access control, exception handling, and stream closure, with an enumeration type distinguishing compression formats. The diagram clearly demonstrates the design of the template method pattern combined with stream processing.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class Tgz extends AbstractCompression"]
    B["Override method: doCompression(Path srcDir, String destFileName)"]
    C["Create output stream chain: Files.newOutputStream → BufferedOutputStream → GzipCompressorOutputStream → TarArchiveOutputStream"]
    D["Traverse file tree: Files.walkFileTree"]
    E["Process single file: visitFile"]
    F["Skip symbolic links: attributes.isSymbolicLink"]
    G["Create tar entry: new TarArchiveEntry"]
    H["Write file content: tOut.putArchiveEntry → Files.copy → closeArchiveEntry"]
    I["Handle failed files: visitFileFailed"]
    J["Complete compression: tOut.finish"]
    K["Override method: getCompressionType → returns Tgz"]
    L["main method: Instantiate Tgz → call compression → output result"]

    A --> B
    A --> K
    A -.-> L
    B --> C
    B --> D
    D --> E
    E --> F
    E --> G
    G --> H
    D --> I
    B --> J
    L --> H
```

Flowchart description: This flowchart illustrates the core process of the Tgz compression utility, starting from initializing the output stream chain, recursively traversing the source directory to process each file (skipping symbolic links), packaging file data into tar format with gzip compression, and finally handling exceptions to complete compression. The main method demonstrates the actual invocation process including result output. Key aspects include the streaming architecture and file tree traversal mechanism.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getCompressionType | CompressionType | Method override, returns the compression type as Tgz. |
| doCompression | void | This method compresses the specified directory into a tar.gz file, skips symbolic links, traverses files and packages them one by one, logs exceptions and continues execution. |
| main | void | The Java main method uses the Tgz class to compress a specified directory and outputs the compressed file path and size (MB). |




