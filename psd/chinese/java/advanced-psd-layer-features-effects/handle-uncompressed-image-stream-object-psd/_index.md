---
date: 2026-02-17
description: 了解如何使用 Aspose.PSD for Java 将 PSD 导出为 PNG 并处理未压缩的图像流。
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: 将 PSD 导出为 PNG – 创建 PSD 图形对象 – Java 中的未压缩流
url: /zh/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in Java

## Introduction
欢迎来到 Java 图像处理的世界！在本教程中，您将 **创建 PSD 图形对象**，处理未压缩的图像流对象，并学习如何使用 Aspose.PSD for Java **将 PSD 导出为 PNG**。无论您是希望自动化工作流的平面设计师，还是想在应用程序中集成强大图像处理功能的软件开发者，本指南都为您量身定制。我们将从前置条件一直讲解到最终导出，确保您对整个过程有全面的了解。

## Quick Answers
- **“创建 PSD 图形对象”是什么意思？** 它指的是为 PSD 文件实例化一个图形上下文，以便您可以绘制或编辑其内容。  
- **哪个库处理未压缩流？** Aspose.PSD for Java 提供对原始（未压缩）图像数据的完整支持。  
- **编辑后可以将 PSD 导出为 PNG 吗？** 可以——只要拥有 `Graphics` 对象，就可以渲染 PSD 并保存为 PNG。  
- **开发阶段需要许可证吗？** 免费试用版可用于测试；生产环境需要商业许可证。  
- **导出是无损的吗？** 导出为 PNG 可保留图像质量，文件大小比 JPEG 大，但比未压缩的 PSD 小。  

## How to export PSD to PNG using Aspose.PSD for Java
当您需要 **将 PSD 导出为 PNG** 时，典型的工作流程如下：

1. 加载 PSD 文件（或创建一个）。  
2. 使用 `Graphics` 对象执行任何绘图或图层操作。  
3. 使用 `PngOptions` 保存生成的图像（同一个 `Graphics` 实例可以重复使用）。  

虽然本教程侧重于处理未压缩流，但您创建的同一个 `Graphics` 对象随后也可以用于将 PSD 渲染为 PNG 文件。

## Prerequisites
在我们进入代码之前，请确保您已准备好以下所有必需品，以顺利开启本次旅程。

### Java Development Kit (JDK)
确保您的机器上已安装 JDK。您可以从 Oracle 官网下载，或使用 OpenJDK。

### Aspose.PSD for Java
需要下载并安装 Aspose.PSD 库。该强大库可轻松操作 PSD 文件。最新版本可从 [此链接](https://releases.aspose.com/psd/java/) 获取。

### Integrated Development Environment (IDE)
建议使用 IDE 编写和测试 Java 代码。您可以选择 IntelliJ IDEA、Eclipse 或其他您喜欢的 IDE。

### Basic Understanding of Java
具备 Java 编程基础会让过程更加顺畅。请确保您了解类、方法和异常处理等基本概念。

准备就绪后，让我们卷起袖子，进入激动人心的编码环节吧！

## Import Packages
首先，需要导入使用 Aspose.PSD 所必需的包。下面列出了处理 PSD 文件时通常需要的 import 语句。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

接下来，我们将代码拆解为易于消化的步骤，帮助您轻松跟随。我们会完成设置、加载 PSD、操作它并保存输出的全过程。

## Step 1: Define Your Document Directory
在编写代码之前，您需要定义 PSD 文件所在的目录。这相当于为项目搭建舞台。

```java
String dataDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为实际的路径，例如存放 `layers.psd` 的文件夹位置。这样即可轻松定位文件。

## Step 2: Create a Byte Array Output Stream
您需要一个地方来存储修改后的图像数据。`ByteArrayOutputStream` 能帮助您轻松捕获图像字节。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

此行代码初始化了一个名为 `ms` 的 `ByteArrayOutputStream` 对象，后续将使用它保存未压缩的图像。

## Step 3: Load the PSD File
现在是加载实际 PSD 文件的时候了，魔法即将开始！

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

此行代码将您的 PSD 文件加载到 `PsdImage` 对象中。请确保路径正确，否则会抛出错误，就像一次意外的测验。

## Step 4: Set Up the PsdOptions for Saving
需要指定保存图像的方式——当然是未压缩的！

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

这里创建了一个 `PsdOptions` 对象，并将压缩方式设置为 `Raw`。该方式确保图像保持完整质量且不进行任何压缩。

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

此行代码使用第 4 步定义的选项，将修改后的图像保存到第 2 步创建的 `ByteArrayOutputStream` 中。`save` 方法会根据您的设置正确编码图像。

## Step 6: Reset the Output Stream
保存后，输出流指针已位于末尾，需要将其重置，以便从头读取。

```java
ms.reset();
```

`reset` 方法会把 `ByteArrayOutputStream` 的指针回到起始位置，类似于在听喜欢的歌曲前倒带磁带。

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

这里我们再次从 `ByteArrayOutputStream` 中加载图像，得到一个新的 `PsdImage` 对象，以便检查前一步的处理结果。

## Step 8: Create Graphics Object
若要进一步修改或渲染图像，需要创建一个 graphics 对象。

```java
Graphics graphics = new Graphics(psdImage);
```

此行代码使用 `psdImage` 实例初始化了一个 `Graphics` 对象。现在，您可以像握笔一样使用该对象绘制或操作图像。

## Manipulate PSD Layers with Graphics Object
拥有 **Graphics** 实例后，您可以 **操作 PSD 图层**——例如绘制形状、添加文字或对特定图层应用滤镜。图形上下文直接作用于底层像素数据，提供对每个图层外观的细粒度控制。

## Common Issues and Solutions
- **加载文件时出现 NullPointerException** – 请再次检查 `dataDir` 路径并确保文件名正确。  
- **即使使用 Raw 仍得到压缩输出** – 确认在调用 `save` 方法前已执行 `saveOptions.setCompressionMethod(CompressionMethod.Raw);`。  
- **Graphics 对象显示为空白** – 请确保您在正确的 `PsdImage` 实例上绘制（使用加载的实例，而不是新创建的，除非有意如此）。

## FAQ's
### What is Aspose.PSD?
Aspose.PSD 是一个 .NET 库，允许开发者以编程方式创建、编辑和操作 Photoshop PSD 文件及相关图像格式。

### How can I download Aspose.PSD for Java?
您可以从 [release page](https://releases.aspose.com/psd/java/) 下载。

### Is there a free trial for Aspose.PSD?
是的，您可以在 [here](https://releases.aspose.com/) 获取免费试用版。

### Can I get support for Aspose.PSD?
当然！您可以在 [Aspose support forum](https://forum.aspose.com/c/psd/34) 寻求帮助。

### How can I obtain a temporary license for Aspose.PSD?
只需访问 [temporary license page](https://purchase.aspose.com/temporary-license/) 即可获取。

## Frequently Asked Questions

**Q: Can I use the graphics object to edit only one specific layer?**  
A: 可以。加载 PSD 后，通过 `psdImage.getLayers().get_Item(index)` 选取目标图层，并将其传入 `Graphics` 构造函数。

**Q: Does the Raw compression method affect file size?**  
A: Raw 方式不进行压缩，因而文件大小会大于压缩后的 PSD，但图像质量保持不变。

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: 完全可以。编辑完成后，使用带有 `PngOptions` 的 `Image.save` 重载即可 **将 PSD 导出为 PNG**。

**Q: What Java version is required?**  
A: Aspose.PSD for Java 支持 JDK 8 及以上版本。

**Q: How do I release resources after processing?**  
A: 调用 `psdImage.dispose()` 并关闭所有流，以释放本地资源。

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}