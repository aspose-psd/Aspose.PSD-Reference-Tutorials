---
date: 2026-04-12
description: 在本分步指南中，学习如何使用 Java 和 Aspose.PSD 库将 PSD 转换为 RAW 并在不压缩的情况下导出 PSD。
keywords:
- convert psd to raw
- export psd without compression
- Aspose.PSD Java
linktitle: 使用 Java 在 PSD 中处理未压缩图像文件
second_title: Aspose.PSD Java API
title: 如何使用 Java 将 PSD 转换为 RAW（未压缩图像文件）
url: /zh/java/advanced-psd-layer-features-effects/work-uncompressed-image-files-psd/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 将 PSD 转换为 RAW（未压缩图像文件）

## 介绍
在 Java 中处理 Photoshop 文档（PSD）时，了解如何**convert PSD to RAW**以及在不压缩的情况下导出 PSD 对于保持图像保真度至关重要。在本教程中，我们将探讨 Aspose.PSD 如何简化处理未压缩图像文件的过程，从加载 PSD 到将其保存为 RAW 风格的未压缩文件。无论您是构建图形密集型应用程序还是需要无损图像导出，这里都有您需要的全部信息。准备好深入了解了吗？让我们开始吧！

## 快速答案
- **“convert PSD to RAW” 是什么意思？** 它在不进行任何压缩的情况下保存 PSD 数据，保持像素数据的原始形态。  
- **哪个库处理此操作？** Aspose.PSD for Java 提供了一个直接的 API 用于未压缩保存。  
- **我需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。  
- **需要哪个 Java 版本？** JDK 8 或更高。  
- **保存后我还能编辑文件吗？** 可以——您可以重新加载未压缩的 PSD 并继续绘制或分层。

## 什么是“convert PSD to RAW”？
将 PSD 转换为 RAW 意味着**without any compression**导出 Photoshop 文档。生成的文件保留完整的像素数据，适用于图像质量不能妥协的场景——例如归档存储、科学成像或高端印刷流水线。

## 为什么要在不压缩的情况下导出 PSD？
- **Maximum quality:** 由于压缩伪影，细节不会丢失。  
- **Predictable file size:** 原始文件的大小直接反映图像尺寸和位深度。  
- **Simplified downstream processing:** 其他工具可以直接读取像素数据，无需先解压。

## 前置条件
在我们卷起袖子开始编码之前，需要检查几项前置条件。别担心，这些都相当简单！

### Java 开发工具包 (JDK)
- 确保系统上已安装 JDK 8 或更高版本。如果没有，请前往[Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)下载最新版本。

### 集成开发环境 (IDE)
- 使用 IntelliJ IDEA、Eclipse 或 NetBeans 等优秀 IDE 能让您事半功倍。如果尚未设置，请先准备好一个。

### Aspose.PSD for Java 库
- 下载 Aspose.PSD for Java 库。您可以在[here](https://releases.aspose.com/psd/java/)获取最新发布。

### Java 基础知识
- 您应具备 Java 编程和面向对象范式的基本理解，以便顺利跟随教程。

### PSD 文件
- 准备一个用于测试的示例 PSD 文件。您可以在 Photoshop 中创建，或在线下载免费样本。

现在一切就绪，让我们深入代码吧！

## 导入包
首先，需要导入代码所需的必要包。下面是您需要的导入列表：

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

这些导入将把必要的类和方法引入项目，使我们能够无缝操作 PSD 文件。让我们把过程拆分为可管理的步骤。

## 步骤 1：设置文件目录
首先，需要指定 PSD 文件所在位置以及输出文件的保存位置。在示例代码中，我们将创建一个变量来保存目录路径。

```java
String dataDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为实际存放 PSD 文件（`layers.psd`）的路径。这样可以确保程序知道去哪里查找文件。

## 步骤 2：加载 PSD 文件
现在，让我们使用 `Image.load()` 方法加载 PSD 文件，并将其强制转换为 `PsdImage` 类型。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

此行调用 `Image` 类的 `load` 方法，将您的 PSD 文件加载到内存中。通过强制转换为 `PsdImage`，我们告诉 Java 将此图像视为具有 PSD 特定功能的文件。

## 步骤 3：配置保存选项
接下来，需要设置文件的保存选项，特别是指定输出为**uncompressed**（即 convert PSD to RAW）。

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

`PsdOptions` 类允许我们为 PSD 文件的保存指定各种选项。将 `setCompressionMethod` 设置为 `CompressionMethod.Raw` 可确保保存的文件未压缩并保持高质量。

## 步骤 4：保存未压缩的 PSD 文件
现在是保存新配置的 PSD 图像的时候了。

```java
psdImage.save(dataDir + "uncompressed_out.psd", saveOptions);
```

此行在我们的 `PsdImage` 实例（`psdImage`）上执行保存功能。它将文件保存为 `uncompressed_out.psd`，位于指定目录，并应用前面定义的选项。

## 步骤 5：重新打开新创建的图像
保存后，让我们重新加载输出图像，以验证一切如预期工作。

```java
PsdImage img = (PsdImage) Image.load(dataDir + "uncompressed_out.psd");
```

再次调用 `load`，我们可以创建一个对应已保存文件的 `PsdImage` 新实例。如果您想在保存后继续操作或显示图像，此步骤至关重要。

## 步骤 6：绘制或操作图像
最后，您可能希望在新打开的图像上进行绘制或其他操作。

```java
Graphics graphics = new Graphics(img);
```

这里我们初始化了一个 `Graphics` 对象，允许我们对 `img` 执行各种图形操作。您可以绘制形状、添加文字，甚至根据需要修改图层！

## 常见用例
- **Archival storage:** 在不产生任何损失的情况下保留原始艺术作品。  
- **Scientific imaging:** 导出原始像素数据以供分析。  
- **Print production:** 在将文件发送至打印机之前确保最高保真度。

## 常见问题

**Q: 什么是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一个 Java 库，允许开发者以编程方式处理 Photoshop PSD 文件。

**Q: 我可以使用 Aspose.PSD 操作 PSD 文件中的图层吗？**  
A: 可以！Aspose.PSD 允许访问和操作图层，轻松完成复杂操作。

**Q: Aspose.PSD 免费使用吗？**  
A: 提供免费试用，但若要广泛使用并访问高级功能，则需要购买许可证。

**Q: 如果遇到问题，我该如何联系支持？**  
A: 您可以通过[Aspose support forum](https://forum.aspose.com/c/psd/34)获取帮助。

**Q: Aspose.PSD 支持除 PSD 之外的格式保存吗？**  
A: 支持，Aspose.PSD 可根据需求保存为 PNG、JPEG 等多种格式。

**Q: 我可以在其他平台上导出无压缩的 PSD 吗？**  
A: 相同方法适用于 .NET 和 C++ 版本的 Aspose.PSD，只需调整语言特定的语法即可。

## 结论
恭喜！您已经学习了如何使用 Java 和 Aspose.PSD 库**convert PSD to RAW**并在不压缩的情况下导出 PSD。这个强大的 API 让您能够轻松管理 PSD 文件——加载、操作并以未压缩状态保存。现在可以尝试使用 graphics 对象，添加图层、绘制形状，或将此工作流集成到更大的图像处理流水线中。

别忘了查看[documentation](https://reference.aspose.com/psd/java/)以获取更高级的功能和选项。如果想直接上手，可以在[here](https://releases.aspose.com/psd/java/)下载库或开始免费试用。如有任何疑问，欢迎访问[support forum](https://forum.aspose.com/c/psd/34)向社区寻求帮助。

---

**Last Updated:** 2026-04-12  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}