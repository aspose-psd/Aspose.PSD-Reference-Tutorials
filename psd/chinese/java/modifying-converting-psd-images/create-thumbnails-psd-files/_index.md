---
date: 2026-03-13
description: 学习如何使用 Aspose.PSD 在 Java 中创建 PSD 缩略图。按照我们的分步指南，快速从 PSD 文件生成缩略图。
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: 使用 Java 创建 PSD 缩略图 – 从 PSD 生成缩略图
url: /zh/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

phen, keep.

Make sure code block placeholders remain as is.

Now craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 创建 PSD 缩略图 Java – 从 PSD 生成缩略图

## 介绍
如果您需要 **create PSD thumbnail Java** 代码来提取 Photoshop 文件中的预览图像，您来对地方了。无论您是在构建数字资产管理器、网页画廊，还是自动化批处理流水线，从 PSD 文件生成缩略图都能显著提升性能和用户体验。在本教程中，我们将使用 Aspose.PSD for Java 完整演示整个过程，展示如何加载 PSD、定位其嵌入的缩略图资源，并将其保存为独立的图像文件。

## 快速答复
- **哪种库最适合 PSD 缩略图提取？** Aspose.PSD for Java。  
- **实现大约需要多长时间？** 基本设置大约需要 10‑15 分钟。  
- **需要安装 Photoshop 吗？** 不需要，Aspose.PSD 可独立工作。  
- **可以导出为哪些图像格式的缩略图？** 任意 Aspose.PSD 支持的格式（例如 BMP、PNG、JPEG）。  
- **生产环境需要许可证吗？** 是的，生产使用需要商业许可证。

## 什么是 “create PSD thumbnail Java”？
在 Java 中创建 PSD 缩略图指的是以编程方式读取 Photoshop 文档（PSD）内部存储的缩略图预览，并将其写出为单独的图像文件。这对于在不加载完整且通常体积庞大的 PSD 内容的情况下快速生成预览非常有用。

## 为什么在此任务中使用 Aspose.PSD？
- **无 Photoshop 依赖：** 可在任何安装 JDK 的平台上运行。  
- **完整的 PSD 支持：** 处理所有 PSD 版本和资源，包括缩略图。  
- **简洁的 API：** 只需几行代码即可提取并保存缩略图。  
- **性能优化：** 对大文件进行高效的内存管理。

## 前置条件
在深入缩略图创建的细节之前，让我们先了解您需要准备哪些内容。

### Java 开发环境
- **Java JDK：** 确保您的计算机已安装 Java Development Kit（JDK）。您可以在[此处](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)下载。  
- **IDE：** 使用 IntelliJ IDEA、Eclipse 或 NetBeans 等集成开发环境（IDE）可以让编码更轻松。

### Aspose.PSD 库
- 您需要在项目中引入 Aspose.PSD 库。您可以[在此处下载最新版本](https://releases.aspose.com/psd/java/)。

### Java 基础知识
- 熟悉 Java 基础将帮助您更有效地阅读示例代码。类、对象和循环等概念将在示例中频繁使用。

## 导入包
首先导入 Aspose.PSD 库中所需的类。这一步至关重要，因为它使您能够在代码中利用库的功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

排除前置条件后，让我们进入正题！从 PSD 文件创建缩略图只需几个简单步骤，下面我会为您逐一拆解。

## 如何创建 PSD 缩略图 Java – 步骤指南

### 步骤 1：设置环境
以下是启动项目并为生成缩略图做准备的步骤。

1. **创建一个 Java 项目**  
   - 打开您的 IDE 并新建一个 Java 项目。  
   - 将项目命名为类似 `"PsdThumbnailGenerator"`。

2. **引入 Aspose.PSD 库**  
   - 将 Aspose.PSD JAR 文件添加到项目的构建路径中。  
   - 如果使用 Maven，请在 `pom.xml` 中加入：

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### 步骤 2：加载 PSD 文件
接下来，需要加载我们想要生成缩略图的 PSD 文件。

1. **指定文档目录**  
   定义 PSD 文件所在的目录。

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **加载 PSD 文件**  
   使用 `PsdImage` 类加载您的 PSD 文件。

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **小贴士：** 将 PSD 文件放在专用文件夹（例如 `src/main/resources`）中，以避免路径问题。

### 步骤 3：遍历 PSD 资源
现在 PSD 图像已经加载，下一步是检查其资源。

1. **获取资源计数**  
   我们将遍历 PSD 文件中的所有资源。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **识别缩略图资源**  
   在循环内部，检查资源是否为缩略图。

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### 步骤 4：处理缩略图
一旦识别出缩略图资源，就需要相应地处理它。

1. **检索并检查缩略图格式**  
   如果资源确实是缩略图，检索它并检查其格式。

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### 步骤 5：创建并保存缩略图
这一步就是魔法所在！我们将根据缩略图数据创建新图像并保存。

1. **创建新图像**  
   我们将使用缩略图资源的宽度和高度创建一个新的位图图像。

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **在新图像中存储像素**  
   将缩略图数据转移到新创建的图像中。

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **保存缩略图图像**  
   最后，将缩略图图像保存到文档目录，并使用唯一名称命名。

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **常见陷阱：** 忘记关闭 `PsdImage` 对象会导致内存泄漏。如果使用 Java 7 及以上版本，请将图像处理代码放在 try‑with‑resources 块中。

## 结论
通过上述步骤，您现在拥有了一套可靠且可复用的 **create PSD thumbnail Java** 实现方法，能够从任何 Photoshop 文件中提取预览图像。此技术可集成到批处理器、Web 服务或桌面工具中，以加速图像目录的建立并提升 UI 响应速度。尝试在自己的 PSD 集合上运行，感受轻量级预览生成的速度吧！

## 常见问题

### 什么是 Aspose.PSD？
Aspose.PSD 是一个 Java 库，允许开发者以编程方式处理 Photoshop 文件，从而更轻松地操作和管理 PSD 文件。

### 我可以免费使用 Aspose.PSD 吗？
可以，Aspose 提供免费试用，您可以在购买许可证前先测试该库。

### 我可以将缩略图保存为何种格式？
本示例中我们将缩略图保存为 BMP 格式，但 Aspose.PSD 还支持多种其他格式。

### 使用 Aspose.PSD 是否需要安装 Photoshop？
不需要，Aspose.PSD 可独立于 Photoshop 工作。

### 在哪里可以找到关于 Aspose.PSD 的更多信息？
您可以查看 [Aspose.PSD 文档](https://reference.aspose.com/psd/java/)获取更多细节、教程和资源。

## 常见问答

**Q: 如何从受密码保护的 PSD 中提取缩略图？**  
A: 使用接受密码参数的 `Image.load` 重载方法加载 PSD 即可。

**Q: 我可以将缩略图生成 PNG 而不是 BMP 吗？**  
A: 完全可以。只需在 `save` 方法中更改文件扩展名，Aspose.PSD 会自动完成转换。

**Q: 是否有办法批量处理多个 PSD 文件？**  
A: 可以将代码包装在遍历 PSD 文件目录的循环中，对每个文件复用相同的提取逻辑。

**Q: 需要哪个 Java 版本？**  
A: Aspose.PSD 支持 Java 8 及以上版本。建议使用最新的 JDK，以获得更好的性能和安全性。

**Q: 该库能高效处理大型 PSD 文件吗？**  
A: 能。Aspose.PSD 使用惰性加载和优化的内存管理，能够在不耗尽堆内存的情况下处理大文件。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-03-13  
**测试环境：** Aspose.PSD 24.11 for Java (latest at time of writing)  
**作者：** Aspose