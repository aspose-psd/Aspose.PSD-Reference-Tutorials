---
date: 2026-08-01
description: 了解如何使用 Aspose.PSD for Java 将 PSD 导出为 PNG 并处理未压缩图像流。
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: 在 PSD 中处理未压缩图像流对象 - Java
og_description: 使用 Aspose.PSD for Java 将 PSD 导出为 PNG。了解如何处理未压缩图像流、创建图形对象并保存高质量 PNG。
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: 将 PSD 导出为 PNG – Java 未压缩 PSD 流指南
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: 将 PSD 导出为 PNG – 创建 PSD 图形对象 – Java 中的未压缩流
url: /zh/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 PSD 为 PNG – 创建 PSD 图形对象 – Java 中的未压缩流

## 介绍
在本分步指南中，您将使用 Aspose.PSD for Java 在处理未压缩图像流时 **export PSD to PNG**。无论是自动化设计流水线还是构建自定义编辑器，能够在不失真的情况下渲染 Photoshop 文件都是必不可少的。我们将从所需的环境设置开始，逐步演示创建 `Graphics` 对象的过程，最后完成无损 PNG 导出。完成后，您将了解 Aspose.PSD 为什么能够高效处理原始流，以及如何将其集成到任何 Java 项目中。

## 快速答案
- **“create PSD graphics object” 是什么意思？** 这意味着实例化一个 `Graphics` 上下文，以便以编程方式在 PSD 图像上绘制或修改。  
- **哪个库处理未压缩流？** Aspose.PSD for Java 完全支持原始（未压缩）图像数据。  
- **编辑后我可以将 PSD 导出为 PNG 吗？** 可以——一旦拥有 `Graphics` 对象，就可以渲染 PSD 并在一次调用中将其保存为 PNG。  
- **开发阶段需要许可证吗？** 免费试用可用于测试；生产部署需要商业许可证。  
- **导出是无损的吗？** 导出为 PNG 会保留原始像素数据，提供无损质量，同时文件大小比原始 PSD 更小。

## 什么是导出 PSD 为 PNG？
将 PSD 导出为 PNG 会将分层的 Photoshop 文档转换为单层、无损的光栅图像，任何网页浏览器或图像查看器都能显示。该过程保留透明度、色彩深度和图层效果，同时舍弃 Photoshop 专有的元数据，并保持原始色彩配置文件以实现准确的颜色再现。

## 为什么在图像处理时使用 Aspose.PSD for Java？
Aspose.PSD 支持 **50+** 输入和输出格式——包括 PSD、PNG、JPEG、BMP 和 TIFF，并且能够在不将整个文档加载到内存中的情况下处理 **200+** 图层。其 `Raw` 压缩选项以未压缩方式存储像素数据，确保下游编辑或归档时像素完美保真。

## 先决条件
在开始编写代码之前，请确认您具备以下条件：

- **Java 开发工具包 (JDK)** – 安装 JDK 8 或更高版本。  
- **Aspose.PSD for Java** – 从官方发布页面下载最新的 JAR：[Aspose.PSD Java download](https://releases.aspose.com/psd/java/)。您也可以通过 [this link](https://releases.aspose.com/psd/java/) 或 [release page](https://releases.aspose.com/psd/java/) 访问。其他 Aspose 产品请点击 [here](https://releases.aspose.com/)。  
- **IDE** – IntelliJ IDEA、Eclipse 或任何兼容 Java 的编辑器。  
- **基本的 Java 知识** – 熟悉类、方法和异常处理。

有了上述准备，您即可开始编码。

## 导入包
`Graphics` 类是 Aspose.PSD 的绘图表面，允许您直接渲染或编辑像素数据。`PsdImage` 类表示内存中的 PSD 文件，而 `PsdOptions` 控制图像的保存方式。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

现在，让我们将代码拆解为易于理解的步骤，您可以轻松跟随。我们将设置环境、加载 PSD 文件、进行操作，最后保存输出。

## 步骤 1：定义文档目录
在进行任何文件操作之前，您需要告诉程序在哪里查找 PSD 资源。此目录路径将在整个教程中使用。

```java
String dataDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为包含 `layers.psd` 的绝对路径。将路径设为可配置可以使代码在不同项目中复用。

## 步骤 2：创建字节数组输出流
`ByteArrayOutputStream` 是一种在内存中以字节数组形式保存数据的 Java 流。它充当修改后图像的内存缓冲区，使您能够在将数据写入磁盘或通过网络发送之前捕获原始字节。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

变量 `ms` 将在 `save` 操作后保存未压缩的图像数据。

## 步骤 3：加载 PSD 文件
`PsdImage` 类将 PSD 文件加载到内存中以便进行操作。加载过程会将磁盘上的 PSD 转换为 `PsdImage` 对象，供后续处理。此步骤中，Aspose.PSD 会读取文件头、图层和资源。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

如果路径不正确，Aspose.PSD 会抛出 `FileNotFoundException`，生产代码中应捕获该异常。

## 步骤 4：设置保存的 PsdOptions
`PsdOptions` 指定 PSD 文件的保存参数。将压缩方式设为 `Raw` 表示像素数据将不进行压缩，完全保留内存中的像素状态。

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

`CompressionMethod.Raw` 选项在后续需要进一步编辑时尤为理想，因为它保留了每个像素的原始信息。

## 步骤 5：将图像保存到输出流
现在，将（可能已修改的）PSD 持久化到先前创建的 `ByteArrayOutputStream` 中。`save` 方法会遵循您配置的 `PsdOptions`。

```java
psdImage.save(ms, saveOptions);
```

此时，`ms` 包含了未压缩 PSD 的完整二进制表示。

## 步骤 6：重置输出流
写入后，流的内部指针位于末尾。重置它可以将指针回滚到开头，以便后续读取。

```java
ms.reset();
```

可以把它想象成在播放前把磁带头移回起始位置。

## 步骤 7：加载新创建的图像
现在，您可以直接从字节数组创建一个全新的 `PsdImage` 实例。此步骤验证保存的数据能够在不损坏的情况下重新加载。

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

如果图像成功加载，说明未压缩流已正确写入。

## 步骤 8：创建 Graphics 对象
`Graphics` 类是 Aspose.PSD 的绘图画布。它提供在 `PsdImage` 的像素矩阵上绘制形状、文字和应用滤镜的方法。

```java
Graphics graphics = new Graphics(psdImage);
```

有了这个 `Graphics` 实例，您可以绘制新内容、擦除部分区域或合成额外图层。

## 如何使用 Aspose.PSD for Java 将 PSD 导出为 PNG？
使用 `new PsdImage(dataDir + "layers.psd")` 加载 PSD，创建 `Graphics` 对象，完成所需绘制后，调用 `psdImage.save("output.png", new PngOptions())`。此序列在一次渲染后即可将编辑后的 PSD 写入无损 PNG，利用 Aspose.PSD 内置的转换引擎。

## 使用 Graphics 对象操作 PSD 图层
拥有 `Graphics` 实例后，您可以对每个图层进行像素级控制。可以绘制几何形状、渲染文字或应用自定义滤镜。由于图形上下文作用于图层的光栅化视图，保存图像时更改会立即生效。

## 常见问题及解决方案
- **加载文件时出现 NullPointerException** – 仔细检查 `dataDir` 路径，并确保文件名完全匹配，包括大小写。  
- **即使使用 Raw 仍然得到压缩输出** – 确认在调用 `save` 之前已执行 `saveOptions.setCompressionMethod(CompressionMethod.Raw);`。  
- **Graphics 对象显示为空白** – 确认您正在对正确的 `PsdImage` 实例绘制（即已加载的实例，而不是新建的空图像）。  
- **大文件导致 OutOfMemoryError** – 使用 `PsdImage.load(dataDir, LoadOptions)` 并通过 `loadOptions.setLoadMode(LoadMode.Memory)` 以流式方式处理大型文件，避免一次性将整个文档加载到 RAM 中。

## 常见问答

### 什么是 Aspose.PSD？
Aspose.PSD 是一个 Java 库，允许开发者在不依赖 Adobe Photoshop 的情况下以编程方式创建、编辑和转换 Photoshop PSD 文件。它支持读取和写入 PSD，处理图层、蒙版、通道和各种图像资源，并提供光栅和矢量操作的 API，适用于服务器端图像处理和自动化任务。

### 如何下载 Aspose.PSD for Java？
您可以从官方发布页面下载： [Aspose.PSD Java download](https://releases.aspose.com/psd/java/)。

### Aspose.PSD 有免费试用吗？
有，官方下载页面提供功能完整的免费试用版，可用于开发和评估。

### 我可以获得 Aspose.PSD 的支持吗？
当然！Aspose 支持论坛提供产品团队和社区的解答： [Aspose support forum](https://forum.aspose.com/c/psd/34)。

### 如何获取 Aspose.PSD 的临时许可证？
您可以直接在 Aspose 的授权门户申请临时许可证，生成有效期为 30 天的限时密钥。此密钥可让您在不购买商业许可证的情况下评估全部功能。试用期结束后，请使用永久许可证替换临时密钥，以继续在生产环境中使用库。访问临时许可证页面获取密钥： [temporary license page](https://purchase.aspose.com/temporary-license/)。

## 常见问题

**Q: 我可以使用 graphics 对象仅编辑特定的单个图层吗？**  
A: 可以。加载 PSD 后，通过 `psdImage.getLayers().get_Item(index)` 获取目标图层，并将该图层传递给 `Graphics` 构造函数。

**Q: Raw 压缩方式会影响文件大小吗？**  
A: Raw 以未压缩方式存储像素数据，因此生成的文件会比压缩 PSD 大，但它保证了 100 % 的像素保真度。

**Q: 是否可以将编辑后的 PSD 导出为其他格式（例如 PNG）？**  
A: 完全可以。编辑完成后，调用 `psdImage.save("output.png", new PngOptions())`——这就是使用 **export PSD to PNG** 的标准无损导出方式。

**Q: 需要哪个 Java 版本？**  
A: Aspose.PSD for Java 支持 JDK 8 及以上版本，包括所有 LTS 版本至 JDK 21。

**Q: 处理完毕后如何释放资源？**  
A: 调用 `psdImage.dispose()` 并关闭所有流（例如 `ms.close()`），以释放本机内存并防止泄漏。

---

**Last Updated:** 2026-08-01  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [使用 Aspose.PSD for Java 将图像保存到流](/psd/java/advanced-techniques/save-images-to-stream/)
- [使用 Java 导出 PSD 图层组为图像](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [在 Aspose.PSD for Java 中使用流创建图像](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}