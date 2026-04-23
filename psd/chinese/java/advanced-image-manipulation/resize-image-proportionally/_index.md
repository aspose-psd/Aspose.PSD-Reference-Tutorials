---
date: 2026-02-09
description: 学习如何使用 Aspose.PSD 在 Java 中将 PSD 转换为 PNG 并按比例调整图像大小。本分步教程涵盖图像缓存、调整大小以及保存为
  PNG。
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 将 PSD 转换为 PNG 并按比例调整大小
url: /zh/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 将 PSD 转换为 PNG 并按比例调整大小

## 引言

如果您需要在保持原始宽高比的情况下 **将 PSD 转换为 PNG**，您来对地方了。在本 **Aspose.PSD Java** 教程中，我们将演示一个完整的 **java image processing tutorial**，展示如何 **按比例调整图像大小**，为图像缓存以获得最佳性能，最后将结果保存为 PNG。完成后，您就可以将此工作流集成到任何基于 Java 的图像处理管道中。

## 快速解答
- **Aspose.PSD 能将 PSD 转换为 PNG 吗？** 是的 – 只需加载 PSD 并使用 `PngOptions` 保存即可。  
- **该库支持按比例调整大小吗？** 当然；使用 `resizeWidthProportionally` 和 `resizeHeightProportionally`。  
- **我需要先缓存图像吗？** 缓存（`image.cacheData()`）可提升大 PSD 文件的性能。  
- **需要哪个 Java 版本？** 完全支持 Java 8 或更高版本。  
- **生产环境是否需要许可证？** 是的，商业许可证可去除评估水印。

## 什么是“将 PSD 转换为 PNG”，以及它为何如此重要？

将 Photoshop 文档（PSD）转换为可移植网络图形（PNG）文件，可让您以轻量、适合网页的格式共享分层设计。PNG 保留透明度并提供无损质量，因而非常适合 UI 资源、缩略图或任何对图像保真度有要求的场景。

## 为什么要在 Java 中按比例调整图像大小？

在 **如何按比例调整图像大小** 而不扭曲宽高比，可确保图形在不同屏幕上看起来自然。`Aspose.PSD` API 提供专门的 **resize image proportionally** 方法，自动计算匹配的高度或宽度，帮助您避免手动计算错误。

## 这对开发者有何意义？

- **降低 PSD 文件大小** – 在转换前缩小大型 PSD，可降低内存使用并加快后续处理。  
- **一致的 UI 渲染** – 按比例调整大小可确保图标和图形在不同设备上保持视觉平衡。  
- **无需 Photoshop 依赖** – 您可以在服务器或 CI 流水线中执行这些操作，而无需安装 Photoshop。

## 前提条件

在开始编写代码之前，请确保您已具备以下条件：

1. **Java 开发工具包 (JDK)** – 已安装 Java 8 或更高版本。  
2. **Aspose.PSD for Java** – 从官方站点[此处](https://releases.aspose.com/psd/java/)下载最新 JAR。  
3. 一个示例 PSD 文件 (`sample.psd`)，放置在项目可引用的目录中。

## 导入包

在您的 Java 类中添加必要的导入。这些类让您能够访问图像加载、缓存、调整大小以及 PNG 输出选项。

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步骤 1：加载 PSD 图像

首先，加载源 PSD 文件。如果文件较大，缓存图像数据可在执行后续操作时减少内存波动。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## 步骤 2：按比例调整图像大小（Java）

现在决定新的尺寸。在本示例中，我们将图像缩小为原始尺寸的 **一半**，同时保持宽高比。您可以根据需要调整目标宽度或高度。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro tip:** 使用 `resizeWidthProportionally` *或* `resizeHeightProportionally` — 库会自动计算另一维度以保持图像比例。

## 步骤 3：将调整大小后的图像保存为 PNG 格式

最后，将调整大小后的图像导出为 PNG 格式。此步骤完成 **convert PSD to PNG** 工作流。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

代码运行后，您会得到一个 PNG 文件，其大小是原始 PSD 的一半，视觉质量保持不变且没有失真。

## 常见问题及解决方案

| 问题 | 原因 | 解决方法 |
|-------|-------|-----|
| **内存溢出错误** | 大型 PSD 文件未缓存 | 调整大小前调用 `image.cacheData()` |
| **PNG 输出空白** | 文件路径错误 | 检查 `dataDir` 目录及其写入权限 |
| **宽高比不正确** | 手动设置宽度和高度 | 使用 Aspose.PSD 提供的比例调整方法 |

## 减小 PSD 文件大小的技巧

- **在加载文件前裁剪不必要的图层**。  
- **按比例调整大小**，如上所示，以提前缩小尺寸。  
- **使用合适的位深度保存为 PNG**，避免多余数据。

## 常见问题解答

**Q: Aspose.PSD 是否兼容所有图像格式？**  
A: Aspose.PSD 支持 PSD、PNG、JPEG、BMP、GIF 等多种格式。完整列表请参阅[文档](https://reference.aspose.com/psd/java/)。

**Q: 我可以在商业项目中使用 Aspose.PSD 吗？**  
A: 可以。请在[Aspose 商店](https://purchase.aspose.com/buy)购买商业许可证。

**Q: 是否提供用于测试的临时许可证？**  
A: 当然 – 可在[此处](https://purchase.aspose.com/temporary-license/)申请临时许可证用于评估。

**Q: 我可以在哪里找到社区支持？**  
A: [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)是提问和分享解决方案的好地方。

**Q: 如何获取完整的 API 参考？**  
A: 详细的 API 文档可在[这里](https://reference.aspose.com/psd/java/)获取。

## 结论

现在您已经了解如何 **将 PSD 转换为 PNG**、**按比例调整图像大小**，以及使用 Aspose.PSD for Java 高效地进行缓存处理。将这些步骤整合到自己的应用程序中，即可实现快速、高质量的图像处理，而无需依赖本地 Photoshop 安装。此 **aspose psd java** 方法是任何 **java image processing tutorial** 的可靠组成部分，帮助您在保持视觉保真度的同时控制 PSD 文件大小。

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
