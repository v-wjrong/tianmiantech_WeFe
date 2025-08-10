# Basic Information

|      |      |
|------|------|
| Name | ImageUtil |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/ImageUtil.java |
| Package Name | com.welab.wefe.common.util |
| Dependencies | ['net.coobird.thumbnailator.Thumbnails', 'javax.imageio.ImageIO', 'java.awt.image.BufferedImage', 'java.io.ByteArrayInputStream', 'java.io.ByteArrayOutputStream', 'java.io.IOException', 'java.math.BigDecimal'] |
| Brief Description | The ImageUtil class provides image compression functionality, which recursively compresses Base64 images to specified dimensions and quality, supporting both PNG and JPG formats, and returns the compressed Base64 string. |

# Description

The ImageUtil class provides image compression functionality, using the `compressPicForScale` method to compress a Base64-format image to a specified size. This method first converts the image to PNG format, retrieves the original width and height, and then invokes the recursive compression method `commpressPicCycle`. The recursive method gradually adjusts the image dimensions and quality based on the precision parameter, iteratively compressing until the target file size (in KB) is achieved or the original dimensions fall below the target value. It returns `null` in case of exceptions and the compressed Base64 string upon success.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ImageUtil | class | The ImageUtil class provides image compression functionality, recursively compressing Base64 images to specified dimensions and quality levels, supporting both PNG and JPG formats, and returning the compressed Base64 string. |



## Class ImageUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ImageUtil |
| Description | The ImageUtil class provides image compression functionality, recursively compressing Base64 images to specified dimensions and quality levels, supporting both PNG and JPG formats, and returning the compressed Base64 string. |


### UML Class Diagram

```mermaid
classDiagram
    class ImageUtil {
        +compressPicForScale(String base64Image, long desFileSize, double accuracy) String
        -commpressPicCycle(byte[] bytes, long desFileSize, double accuracy) byte[]
    }

    class Base64Util {
        +base64ToByteArray(String base64) byte[]
        +encode(byte[] bytes) String
    }

    class Thumbnails {
        +of(BufferedImage image) Builder
        +of(InputStream is) Builder
    }

    class Thumbnails.Builder {
        +size(int width, int height) Builder
        +imageType(int imageType) Builder
        +outputFormat(String format) Builder
        +outputQuality(double quality) Builder
        +toOutputStream(OutputStream os) void
    }

    class BufferedImage {
        +getWidth() int
        +getHeight() int
    }

    class ImageIO {
        +read(InputStream input) BufferedImage
    }

    ImageUtil --> Base64Util : Uses
    ImageUtil --> Thumbnails : Uses
    ImageUtil --> BufferedImage : Uses
    ImageUtil --> ImageIO : Uses
    Thumbnails --> Thumbnails.Builder : Creates
```

Class Diagram Description:
This diagram illustrates the core structure and dependencies of the ImageUtil utility class. ImageUtil provides image compression functionality, primarily relying on Base64Util for Base64 encoding/decoding, utilizing the Thumbnails library for image resizing and quality compression, obtaining image dimensions through BufferedImage, and invoking ImageIO to read image data. Thumbnails.Builder implements the builder pattern to support chained configuration of compression parameters. The design implements recursive compression logic until the target file size is achieved.


### Internal Method Call Graph

```mermaid
graph TD
    A["compressPicForScale Entry"]
    B["Base64Util.base64ToByteArray"]
    C["ByteArrayInputStream Initialization"]
    D["ImageIO.read to Get BufferedImage"]
    E["Get Image Dimensions: image.getWidth/getHeight"]
    F["Thumbnails.Builder Configuration: imageType/outputFormat"]
    G["ByteArrayOutputStream Initialization"]
    H["builder.toOutputStream Write"]
    I["commpressPicCycle Recursive Compression"]
    J["Base64Util.encode to Base64"]
    K["Exception Handling: e.printStackTrace"]
    L["Return null or Compressed Result"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    J --> L
    A -.-> K
    K --> L

    M["commpressPicCycle Entry"]
    N["Check File Size Compliance"]
    O["ImageIO.read to Get BufferedImage"]
    P["Calculate New Dimensions: BigDecimal Multiplication"]
    Q["Thumbnails.of Configure Compression Parameters"]
    R["Recursively Call commpressPicCycle"]
    S["Return Compressed Byte Array"]

    M --> N
    N --Compliant--> S
    N --Non-compliant--> O
    O --> P
    P --> Q
    Q --> R
    R --> M
```

Flowchart Description: This flowchart illustrates the complete image compression process in the ImageUtil class. The main method compressPicForScale first converts a base64 image into a byte stream, obtains the original dimensions, performs PNG format conversion via Thumbnails, and then enters the recursive compression loop commpressPicCycle. The recursive method continuously adjusts image dimensions and quality parameters until the file size meets requirements or the maximum compression attempts are reached, ultimately returning the compressed base64 string. The entire process includes exception handling and multiple format conversion stages.

### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| commpressPicCycle | byte[] | This method recursively compresses the image to the target size. If the current dimensions meet the requirements, it returns the original data; otherwise, it adjusts the width and height according to the precision ratio and recompresses, looping until the conditions are satisfied. |
| compressPicForScale | String | This method compresses a Base64 image to the target size by first converting it to PNG format, then iteratively compressing it to the specified precision, and finally returning the compressed Base64 string. |




