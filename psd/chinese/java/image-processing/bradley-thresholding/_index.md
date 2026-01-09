---
date: 2026-01-09
description: 了解如何使用 Aspose.PSD for Java 中的 Bradley 阈值法将 PSD 转换为 PNG。本指南展示了如何选择最佳阈值并高效地对
  PSD 图像进行二值化。
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: 使用Bradley阈值法将PSD转换为PNG（Aspose.PSD Java）
url: /zh/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Bradley 阈值化将 PSD 转换为 PNG（Aspose.PSD Java）

欢迎阅读本综合指南，介绍在 Aspose.PSD for Java 中使用 Bradley 阈值化 **convert PSD to PNG**。在接下来的几分钟里，您将了解为何此技术非常适合从 Photoshop 文档创建高对比度、二值化的 PNG 文件，并获得动手的分步演练。

## 快速答案
- **我可以使用 Aspose.PSD 将 PSD 转换为 PNG 吗？** 是的 – 加载 PSD，应用 `binarizeBradley`，然后保存为 PNG。  
- **“choose optimal threshold” 是什么意思？** 它是一个灵敏度值（0‑1），决定像素的暗/亮如何分类。  
- **生产环境使用是否需要许可证？** 需要商业许可证；免费试用可用于评估。  
- **支持哪些图像格式的保存？** PNG、JPEG、BMP，以及通过 `ImageOptions` 类支持的许多其他格式。  
- **代码是否兼容 Java 8 及更高版本？** 完全兼容 – Aspose.PSD Java API 支持 Java 8+。

## Bradley 阈值化是什么？

Bradley 阈值化是一种自适应二值化算法，它为每个像素计算局部平均值，并将像素强度与该平均值乘以用户定义的阈值进行比较。结果是保持重要细节的干净的黑白图像。

## 为什么使用 Bradley 阈值化将 PSD 转换为 PNG？

- **保留锐利边缘** – 适用于 OCR、条形码检测或任何需要前景与背景清晰分离的工作流。  
- **减小文件大小** – PNG 是无损的，但二值化后通常更小。  
- **跨平台兼容性** – PNG 在所有平台均可使用，而 PSD 仅限 Photoshop。

## 先决条件

在开始之前，请确保您已具备以下条件：

1. **Java 开发环境** – 已安装 JDK 8 或更高版本。  
2. **Aspose.PSD 库** – 从 [here](https://releases.aspose.com/psd/java/) 下载最新的 JAR。  
3. **示例 PSD 图像** – 任意您想转换的 PSD 文件；也可以使用 Aspose 示例中提供的样本。

## 导入包

首先在 Java 项目中导入所需的类：

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## 如何使用 Bradley 阈值化将 PSD 转换为 PNG

以下是完整的工作流，分为清晰的编号步骤。每一步包含简短说明以及您需要复制粘贴的完整代码。

### 步骤 1：加载 PSD 图像

首先，指向源文件并使用 Aspose.PSD 加载它。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### 步骤 2：选择最佳阈值

阈值（范围 0 – 1）控制二值化的强度。典型的起始值为 **0.15**，但您可以根据图像进行调整。

```java
// Define threshold value
double threshold = 0.15;
```

### 步骤 3：二值化 PSD 图像

现在应用 Bradley 算法。此步骤根据您选择的阈值 **binarize PSD image**。

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### 步骤 4：将输出保存为 PNG

最后，将处理后的图像以 PNG 格式写入磁盘。

```java
// Save the output image
image.save(destName, new PngOptions());
```

对需要处理的任意数量的 PSD 文件重复这些步骤，并根据需要调整阈值以获得最佳视觉效果。

## 常见问题与技巧

- **阈值过低/过高：** 如果输出看起来噪点过多或过于淡白，请逐步调整 `threshold` 值（例如 0.10 – 0.20）。  
- **内存消耗：** 大型 PSD 文件可能占用大量内存。考虑一次处理一个文件或增大 JVM 堆大小（`-Xmx`）。  
- **保存前预览：** 使用 `image.save("preview.bmp", new BmpOptions());` 在最终导出 PNG 前检查二值化结果。

## 常见问答

**Q: `binarizeBradley` 与其他阈值化方法有什么区别？**  
A: `binarizeBradley` 为每个像素计算局部均值，与全局阈值化相比，对光照不均的图像更具鲁棒性。

**Q: 我可以将 Bradley 阈值化应用于 JPEG 或 BMP 文件吗？**  
A: 可以。使用 `Image.load(...)` 加载任何受支持的格式，然后在保存前调用 `binarizeBradley`。

**Q: 是否有办法在保存前预览二值化图像？**  
A: 当然。使用 Aspose.PSD 的任意图像保存选项（例如 BMP）写入临时预览文件。

**Q: 我可以在哪里找到更多支持和资源？**  
A: 访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34) 获取社区帮助，并查阅完整的 [文档](https://reference.aspose.com/psd/java/) 了解高级场景。

## 结论

您现在已经学习了如何通过 **选择最佳阈值** 并使用 Bradley 阈值化 **二值化 PSD 图像**，高效地 **convert PSD to PNG**。此方法非常适合需要从复杂 Photoshop 文件生成干净、高对比度 PNG 输出的工作流。

---

**最后更新：** 2026-01-09  
**测试环境：** Aspose.PSD Java 23.12（撰写时的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}