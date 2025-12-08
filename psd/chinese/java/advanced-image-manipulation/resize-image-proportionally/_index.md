---
date: 2025-12-08
description: 学习如何使用 Aspose.PSD 在 Java 中将 PSD 转换为 PNG 并按比例调整图像大小。本分步教程涵盖图像缓存、调整大小以及保存为
  PNG。
language: zh
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 将 PSD 转换为 PNG 并按比例调整大小
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 将 PSD 转换为 PNG 并按比例调整大小

## 介绍

如果您需要 **将 PSD 转换为 PNG** 并保持原始宽高比，您来对地方了。在本教程中，我们将完整演示一个 **Aspose.PSD 教程**，展示如何在 Java 中 **按比例调整图像**，对图像进行缓存以获得最佳性能，最后将结果保存为 PNG。完成后，您即可将此工作流集成到任何基于 Java 的图像处理管道中。

## 快速答案
- **Aspose.PSD 能将 PSD 转换为 PNG 吗？** 能——只需加载 PSD 并使用 `PngOptions` 保存即可。
- **库是否支持按比例调整大小？** 当然；使用 `resizeWidthProportionally` 和 `resizeHeightProportionally`。
- **是否需要先缓存图像？** 缓存（`image.cacheData()`）可提升大 PSD 文件的性能。
- **需要哪个 Java 版本？** 完全支持 Java 8 及以上版本。
- **生产环境是否需要许可证？** 需要，商业许可证可去除评估水印。

## 什么是 “convert PSD to PNG”，它为何重要？

将 Photoshop 文档（PSD）转换为可移植网络图形（PNG）文件，可让您以轻量、适合 Web 的格式共享分层设计。PNG 保留透明度并提供无损质量，适用于 UI 资源、缩略图或任何对图像保真度有要求的场景。

## 为什么在 Java 中按比例调整图像？

**按比例调整图像** 而不扭曲宽高比，可确保图形在不同屏幕上自然显示。`Aspose.PSD` API 提供专用的比例缩放方法，自动计算匹配的高度或宽度，免去手动计算的错误。

## 前置条件

在开始编写代码之前，请确保您已具备：

1. **Java Development Kit (JDK)** – 已安装 Java 8 或更高版本。  
2. **Aspose.PSD for Java** – 从官方站点[此处](https://releases.aspose.com/psd/java/)下载最新 JAR。  
3. 一个示例 PSD 文件（`sample.psd`），放置在项目可以引用的目录中。

## 导入包

在 Java 类中添加必要的导入。这些类提供图像加载、缓存、比例缩放以及 PNG 输出选项的功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步骤 1：加载 PSD 图像

首先，加载源 PSD 文件。如果文件较大，缓存图像数据可在后续操作时减少内存波动。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## 步骤 2：在 Java 中按比例调整图像

接下来确定新的尺寸。在本例中，我们将图像缩小为原始尺寸的 **一半**，同时保持宽高比。您可以根据需要调整目标宽度或高度。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **小技巧：** 使用 `resizeWidthProportionally` *或* `resizeHeightProportionally`——库会自动计算另一维度，以保持图像比例。

## 步骤 3：将调整大小后的图像保存为 PNG

最后，将调整大小后的图像导出为 PNG 格式。这一步完成了 **convert PSD to PNG** 工作流。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

代码运行后，您将在指定位置得到一个尺寸为原始 PSD 一半的 PNG 文件，视觉质量保持不变且无失真。

## 常见问题与解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| **OutOfMemoryError** | 大 PSD 未缓存 | 在缩放前调用 `image.cacheData()` |
| **Blank PNG output** | 文件路径错误 | 检查 `dataDir` 并确认写入权限 |
| **Aspect ratio looks off** | 手动同时设置宽高 | 使用 Aspose.PSD 提供的比例方法 |

## 常见问答

**Q: Aspose.PSD 是否兼容所有图像格式？**  
A: Aspose.PSD 支持 PSD、PNG、JPEG、BMP、GIF 等多种格式。完整列表请参阅[文档](https://reference.aspose.com/psd/java/)。

**Q: 我可以在商业项目中使用 Aspose.PSD 吗？**  
A: 可以。请在[Aspose 商店](https://purchase.aspose.com/buy)购买商业许可证。

**Q: 是否提供临时许可证用于测试？**  
A: 当然——可在[此处](https://purchase.aspose.com/temporary-license/)申请临时许可证进行评估。

**Q: 哪里可以找到社区支持？**  
A: [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)是提问和分享解决方案的好地方。

**Q: 如何访问完整的 API 参考？**  
A: 详细的 API 文档可在[这里](https://reference.aspose.com/psd/java/)查看。

## 结论

现在，您已经掌握了如何 **将 PSD 转换为 PNG**、按比例调整图像大小，并使用 Aspose.PSD for Java 高效地进行缓存。将这些步骤整合到自己的应用程序中，即可实现快速、高质量的图像处理，而无需依赖本地 Photoshop 安装。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2025-12-08  
**测试环境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose