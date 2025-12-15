---
date: 2025-12-13
description: 了解如何使用 Aspose.PSD for Java 通过处理未压缩的图像流来创建 PSD 图形对象并操作 PSD 图层。
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: 在 Java 中创建 PSD 图形对象 – 未压缩流
url: /zh/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 创建 PSD 图形对象 – Java 中的未压缩流

## 介绍
欢迎来到 Java 图像处理的世界！在本教程中，您将 **创建 PSD 图形对象** 并使用 Aspose.PSD for Java 处理未压缩的图像流对象。无论您是希望自动化工作流程的平面设计师，还是想将强大的图像处理能力集成到应用程序中的软件开发者，本指南都为您量身定制。我们将从前置条件一直讲解到结论，确保您对如何使用 Aspose.PSD 有扎实的了解。

## 快速答案
- **“创建 PSD 图形对象”是什么意思？** 它指的是为 PSD 文件实例化一个图形上下文，以便您可以绘制或编辑其内容。  
- **哪个库处理未压缩流？** Aspose.PSD for Java 完全支持原始（未压缩）图像数据。  
- **开发阶段需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。  
- **创建图形对象后可以操作 PSD 图层吗？** 可以——Graphics 实例允许您在任意图层上绘制。

## 前置条件
在我们进入代码之前，请确保您已经准备好所有必要的工具。以下是前置条件：

### Java Development Kit (JDK)
确保您的机器上已安装 JDK。您可以从 Oracle 官方网站下载，或使用 OpenJDK。

### Aspose.PSD for Java
您需要下载并安装 Aspose.PSD 库。该强大库可轻松操作 PSD 文件。您可以从[此链接](https://releases.aspose.com/psd/java/)获取最新版本。

### Integrated Development Environment (IDE)
建议使用 IDE 编写和测试 Java 代码。您可以使用 IntelliJ IDEA、Eclipse 或其他您喜欢的 IDE。

### Basic Understanding of Java
具备 Java 编程基础会让过程更加顺畅。请确保您了解类、方法和异常处理等基本概念。

一切就绪后，让我们卷起袖子，进入激动人心的编码环节吧！

## 导入包
为了开始工作，我们需要导入使用 Aspose.PSD 所必需的包。下面列出了处理 PSD 文件时通常需要的导入语句。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

现在，让我们把代码拆解为易于消化的步骤，确保您能够轻松跟随。我们将完成设置、加载 PSD 文件、操作它并保存输出。

## 步骤 1：定义文档目录
在编写代码之前，您需要定义 PSD 文件所在的位置。这相当于为项目搭建舞台。

```java
String dataDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为实际的路径，例如存放 `layers.psd` 的目录。这样可以轻松定位文件，避免麻烦。

## 步骤 2：创建字节数组输出流
您需要一个地方来存储修改后的图像，以便后续使用。`ByteArrayOutputStream` 能帮助您轻松捕获图像数据。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

此行代码初始化了一个名为 `ms` 的 `ByteArrayOutputStream` 对象。您将在后面使用该对象保存未压缩的图像。

## 步骤 3：加载 PSD 文件
现在是加载实际 PSD 文件的时候了。魔法即将开始！

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

此行代码将您的 PSD 文件加载到 `PsdImage` 对象中。请确保路径正确，否则会像未检查的测验一样弹出错误。

## 步骤 4：设置保存的 PsdOptions
您需要指定图像的保存方式——当然是未压缩的！

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

这里创建了一个 `PsdOptions` 对象，并将压缩方式设置为 `Raw`。该方式确保图像保持完整质量，且不进行任何压缩。

## 步骤 5：将图像保存到输出流
```java
psdImage.save(ms, saveOptions);
```

此行代码使用第 2 步创建的 `ByteArrayOutputStream`，并依据第 4 步定义的选项，将修改后的图像保存进去。`save` 方法会根据您的设置正确编码图像。

## 步骤 6：重置输出流
保存后，输出流已位于末尾。您需要将其重置，以便从头读取。

```java
ms.reset();
```

此 `reset` 方法为 `ByteArrayOutputStream` 做好重新从起始位置读取的准备。可以把它想象成在聆听喜爱歌曲前倒回磁带！

## 步骤 7：加载新创建的图像
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

这里我们将图像从 `ByteArrayOutputStream` 中读取回一个新的 `PsdImage` 对象。您可以在此检查之前工作的结果。

## 步骤 8：创建 Graphics 对象
为了进一步修改或渲染图像，您需要创建一个 graphics 对象。

```java
Graphics graphics = new Graphics(psdImage);
```

此行代码使用您的 `psdImage` 初始化了一个 `Graphics` 对象。现在您可以使用该对象绘制或操作图像，就像手中握着画笔一样！

## 使用 Graphics 对象操作 PSD 图层
现在您已经拥有 **Graphics** 实例，可以 **操作 PSD 图层**——例如绘制形状、添加文字或对特定图层应用滤镜。Graphics 上下文直接作用于底层像素数据，让您对每个图层的外观拥有细粒度的控制。

## 常见问题及解决方案
- **加载文件时出现 NullPointerException** – 再次检查 `dataDir` 路径并确保文件名正确。  
- **即使使用 Raw 仍得到压缩输出** – 确认在调用 `save` 方法之前已执行 `saveOptions.setCompressionMethod(CompressionMethod.Raw);`。  
- **Graphics 对象显示为空白** – 确保您在正确的 `PsdImage` 实例上绘制（使用已加载的实例，而不是新创建的，除非有意如此）。

## 常见问题
### What is Aspose.PSD?
Aspose.PSD 是一个 .NET 库，能够让开发者以编程方式创建、编辑和操作 Photoshop PSD 文件及相关图像格式。

### How can I download Aspose.PSD for Java?
您可以从[发布页面](https://releases.aspose.com/psd/java/)下载。

### Is there a free trial for Aspose.PSD?
是的，您可以从[此处](https://releases.aspose.com/)获取免费试用版。

### Can I get support for Aspose.PSD?
当然！您可以在[Aspose 支持论坛](https://forum.aspose.com/c/psd/34)寻求帮助。

### How can I obtain a temporary license for Aspose.PSD?
只需访问[临时许可证页面](https://purchase.aspose.com/temporary-license/)即可开始。

## 常见问答

**Q: Can I use the graphics object to edit only one specific layer?**  
A: 是的。加载 PSD 后，通过 `psdImage.getLayers().get_Item(index)` 选择所需图层，并将其传入 `Graphics` 构造函数即可。

**Q: Does the Raw compression method affect file size?**  
A: Raw 以未压缩方式存储像素数据，因此文件大小会大于压缩的 PSD，但图像质量保持不变。

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: 完全可以。编辑完成后，使用带有 `PngOptions` 的相应 `Image.save` 重载即可导出为 PNG 等格式。

**Q: What Java version is required?**  
A: Aspose.PSD for Java 支持 JDK 8 及更高版本。

**Q: How do I release resources after processing?**  
A: 调用 `psdImage.dispose()` 并关闭所有流，以释放本机资源。

---  

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}