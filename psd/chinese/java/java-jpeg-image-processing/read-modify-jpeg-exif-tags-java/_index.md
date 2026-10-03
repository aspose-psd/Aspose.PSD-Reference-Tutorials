---
date: 2026-10-03
description: 在本分步指南中学习如何使用 Aspose.PSD for Java 在 Java 中读取图像元数据并修改 JPEG EXIF 标签，帮助开发者高效处理图像元数据。
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: 在 Java 中读取和修改 JPEG EXIF 标签
og_description: 了解如何使用 Aspose.PSD for Java 在 Java 中读取图像元数据并修改 JPEG EXIF 标签。本指南提供分步代码示例，演示如何提取和更新
  EXIF 信息。
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: 如何在 Java 中读取图像元数据并修改 JPEG EXIF 标签
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: 如何在 Java 中读取图像元数据并修改 JPEG EXIF 标签
url: /zh/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 读取和修改 Java 中的 JPEG EXIF 标签

## 介绍
如果您需要 **java read image metadata** 从 JPEG 文件中读取并以编程方式更改它，您来对地方了。在本教程中，我们将演示如何使用 Aspose.PSD for Java 提取和更新 EXIF 标签。完成后，您将能够获取相机详情、方向和自定义字段，然后将它们写回文件——无需图形编辑器。

## 快速答案
- **哪个库在 Java 中处理 JPEG EXIF？** Aspose.PSD for Java。  
- **读取 EXIF 需要多少行代码？** 加载图像后大约三行代码。  
- **可以修改 EXIF 标签吗？** 是的，您可以更改任何标准或自定义标签并保存结果。  
- **支持的图像格式？** 超过 150 种格式，包括 PSD、JPEG、PNG、TIFF 和 BMP。  
- **最低 Java 版本？** Java 7 或更高。

## 为什么使用 Aspose.PSD for Java？
Aspose.PSD 支持 **150+ 图像格式**，并且能够在不将整个文档加载到内存中的情况下处理高达 **2 GB** 的文件，为大型照片集合提供快速、低内存的元数据操作。它还提供了简洁的 API 用于读取和写入 EXIF、IPTC 和 XMP 数据，使数千张图像的批处理既高效又可靠。

## 前置条件
1. **Java Development Kit (JDK)** – 确保您使用 JDK 11 或更高版本。您可以从 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下载。  
2. **Aspose.PSD for Java library** – 从 [Aspose releases page](https://releases.aspose.com/psd/java/) 获取最新的 JAR 包。  
3. **IDE** – IntelliJ IDEA、Eclipse 或您喜欢的任何编辑器。  
4. **Basic Java knowledge** – 您应熟悉创建项目并添加外部 JAR。

## 什么是 Java read image metadata？
Java read image metadata 指的是使用 Java 代码以编程方式访问图像文件中嵌入的信息（如 EXIF、IPTC 和 XMP）。这些元数据可能包括相机设置、时间戳、GPS 坐标、版权声明和用户评论，使应用程序能够基于描述性数据组织、搜索和操作图像。

## 导入包
首先，将 Aspose.PSD JAR 添加到项目的类路径并导入所需的类。

`com.aspose.psd` 包提供了用于加载图像和访问其资源的核心 API。

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 如何在 Java 中读取 JPEG 文件的图像元数据？
使用 `PsdImage.load("image.jpg")` 加载 JPEG，定位包含 EXIF 数据的缩略图资源，然后调用 `ExifData.read()` 获取填充好的 `ExifData` 对象。这一步骤即可让您完整访问所有标准 EXIF 字段以及任何自定义标签。

## 步骤 1：加载 PSD 图像
PsdImage 是 Aspose.PSD 中表示 PSD 文件的类，提供访问其资源和元数据的方法。  
在此步骤中，我们将加载要读取 EXIF 数据的 PSD 图像。确保图像位于正确的目录中。

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## 步骤 2：遍历图像资源
ThumbnailResource 表示存储在 PSD 文件中的缩略图图像，通常包含嵌入的 EXIF 数据。  
图像加载完成后，下一步是遍历其资源以查找缩略图资源，该资源通常包含 EXIF 数据。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## 步骤 3：提取 EXIF 数据
JpegExifData 是用于保存从 JPEG 图像中提取的 EXIF 信息的类，允许您读取和修改各个标签。  
现在我们拥有了缩略图资源，可以从中提取 EXIF 数据。EXIF 数据包括相机所有者姓名、光圈值、方向等有价值的信息。

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## 步骤 4：修改 EXIF 数据
读取 EXIF 数据后，您可能想修改其中的某些字段。下面展示了如何进行修改：

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## 步骤 5：保存更改
最后，在修改 EXIF 数据后，将更改保存为新的 PSD 文件。

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## 常见问题及解决方案
- **Missing thumbnail resource** – 某些 JPEG 将 EXIF 直接存储在主图像头部。如果缺少缩略图资源，请改用 `image.getExifData()`。  
- **Large files cause OutOfMemoryError** – 确保使用足够的堆内存启动 JVM（例如 `-Xmx2g`），或使用 `PsdImage.load(inputStream, loadOptions)` 以流模式处理图像。  
- **Unsupported tag types** – Aspose.PSD 支持所有标准 EXIF 标签；自定义标签可能需要手动进行字节级处理。

## 常见问题

**Q: 什么是 EXIF 数据？**  
A: EXIF（Exchangeable Image File Format）元数据存储相机设置、时间戳、GPS 坐标以及嵌入在 JPEG 等图像文件中的其他信息。

**Q: 我可以免费使用 Aspose.PSD for Java 吗？**  
A: 您可以从 [Aspose releases page](https://releases.aspose.com/) 获取免费试用版。

**Q: Aspose.PSD for Java 是否兼容所有 Java 版本？**  
A: Aspose.PSD for Java 支持 Java SE 7 及以上版本。

**Q: 在哪里可以找到更多关于 Aspose.PSD for Java 的文档？**  
A: 请查看 [documentation](https://reference.aspose.com/psd/java/) 获取详细信息。

**Q: 如何获取 Aspose.PSD for Java 的支持？**  
A: 您可以在 [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/) 获得帮助。

## 结论
通过遵循这些步骤，您可以 **java read image metadata** 任意 JPEG，调整所需的 EXIF 字段，并将更新后的数据写回文件——只需几行简洁的 Java 代码。Aspose.PSD 丰富的 API 使元数据处理可靠且高效，您可以将其集成到批处理管道、照片管理工具或任何需要处理图像信息的应用中。

---

**最后更新：** 2026-10-03  
**测试环境：** Aspose.PSD for Java 24.5  
**作者：** Aspose

## 相关教程

- [使用 Aspose (asp) 在 Java 中读取特定 EXIF 标签信息](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [使用 Aspose.PSD for Java 在 PSD 文件中创建 XMP 元数据](/psd/java/image-editing/create-xmp-metadata/)
- [使用 Aspose.PSD for Java 调整图像大小 – 绘制形状与基本图像操作](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}