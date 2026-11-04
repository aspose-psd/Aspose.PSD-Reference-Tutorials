---
date: 2026-11-04
description: 了解如何使用 Aspose.PSD for Java 应用 invert adjustment layer、batch process PSD
  图像，并创建 negative image PSD 文件。
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: 如何使用 Aspose.PSD for Java 添加 invert adjustment layer、batch process
  PSD 图像，并创建 negative image PSD。请按照分步指南操作。
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: 如何使用 Aspose.PSD for Java 添加 invert adjustment layer
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: 如何在 Java 中使用 Aspose.PSD 添加 invert adjustment layer
url: /zh/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.PSD 添加反相调整图层

## 介绍

如果您正在寻找一个强大的 **image processing java library**，Aspose.PSD for Java 是市场上最通用的选项之一。在本教程中，您将看到 **how to use Aspose** 在 PSD 文件中插入 **Invert Adjustment Layer**，并将其与其他调整堆叠，甚至在数十个文件上运行此操作。无论您是构建批处理工具、服务器端图像服务，还是单图像编辑器，下面的步骤都能在几分钟内将源 PSD 转换为可完全编辑的负片图像。

## 快速答案
- **Invert Adjustment Layer 的作用是什么？** 它会翻转所选区域的每个 RGB 值，使图像变成摄影负片。  
- **哪个库提供此功能？** Aspose.PSD，一个领先的 **image processing java library**。  
- **我可以将其与其他调整堆叠吗？** 是的——您可以 **apply multiple adjustment layers**，例如 Brightness/Contrast、Hue/Saturation 等。  
- **开发是否需要许可证？** 有免费试用版；在生产环境中需要许可证。  
- **实现需要多长时间？** 对于基本用例，通常不到 10 分钟。

## 什么是 Invert Adjustment Layer？

Invert Adjustment Layer 是一种非破坏性编辑，可反转其影响的每个像素的颜色值。由于它位于图层堆栈之上，您可以切换其可见性或重新排序，而不会永久更改原始图像数据。这是创建 **negative image PSD** 文件或实现经典胶片负片外观的最快方法。

## 为什么将 Aspose.PSD 用作您的 image processing java library？

Aspose.PSD 支持 **200+ PSD features**，可以在不需要 Photoshop 的情况下读取和写入 Photoshop 文件，并使用不到 500 MB 的堆内存处理数百页文档。它可在任何 Java 运行时（Java 6+）上运行，使其非常适合在 Windows、Linux 或 macOS 服务器上进行 **batch process psd images**。

## 前提条件

在开始之前，请确保您拥有：

1. **Aspose.PSD for Java** – 从官方网站下载最新的 JAR [Aspose.PSD for Java 下载页面](https://releases.aspose.com/psd/java/)。  
2. **Java Development Kit** – 已在 `PATH` 中安装并配置 JDK 6.0 或更高版本。  

现在您已经准备好编写代码。

## 导入包

`PsdImage` 类表示内存中的整个 Photoshop 文档，而调整图层类位于 `com.aspose.psd.layers.adjustments` 包中。

`PsdImage` 类是 Aspose.PSD 的顶层对象，封装了 PSD 文件的结构和像素数据。导入命名空间后，您就可以加载、编辑和保存 PSD 文件。

## 步骤 1：设置文档目录

定义包含源 PSD 文件的文件夹以及输出将保存的位置。使用绝对路径可以避免工作目录更改时出现 `NullPointerException`。

## 步骤 2：加载 PSD 文件

将源文件加载到 `PsdImage` 对象中。该对象在内存中保存完整的图层层次结构，支持非破坏性编辑。

`PsdImage` 类提供了静态 `load` 方法，用于读取文件头、验证格式并构建可供操作的内存表示。

## 步骤 3：添加反相调整图层

调用内置方法在当前图层堆栈顶部插入 Invert Adjustment Layer。随后您可以添加更多图层（例如亮度、色相）以 **apply multiple adjustment layers** 于单一工作流。

`addInvertAdjustmentLayer()` 将 Invert Adjustment Layer 添加到 PSD 的图层集合中。

## 步骤 4：保存输出

将修改后的 PSD 持久化到磁盘。

`save()` 将 PSD 文件（包括所有图层和元数据）写入指定路径。

保存使用相同的 `save` 方法，将完整文档（包括所有调整图层、蒙版和元数据）写入指定格式。

### 刚才发生了什么？

PSD 文件已加载到 `PsdImage` 对象中，创建了 `InvertAdjustmentLayer` 并将其追加为最上层图层，随后文档被保存。此过程在保留原始图像数据的同时，添加了可切换或重新排序的非破坏性反相效果。

您已经成功使用 Aspose.PSD，这个 **image processing java library**，来操作 PSD 文件。

## 如何使用反相调整批量处理 PSD 图像？

在 `for` 循环中加载每个文件，执行相同的步骤，并对每次迭代调用 `save`。由于 Aspose.PSD 以流式方式处理文件，您可以在保持内存使用低于 300 MB 的情况下处理 **hundreds of PSDs**，只需复用同一个 `PsdImage` 实例。

## 如何将 PSD 转换为负片图像？

将 Invert Adjustment Layer 设为最上层项目并保存文档——此操作相当于 **convert PSD to negative**。随后您可以禁用或删除该图层，以在不重新加载源文件的情况下恢复原始外观。

## 常见问题与技巧

| 问题 | 原因 | 解决方案 |
|-------|-------|----------|
| **`Image.load` 上的 NullPointerException** | 文件路径不正确或文件缺失 | 验证 `dataDir` 和文件名；在测试时使用绝对路径 |
| **图层顺序不符合预期** | 在现有图层后添加图层会改变堆叠顺序 | 在其他调整之前插入反相图层，或通过 `psdImage.getLayers().move()` 重新排序 |
| **大型 PSD 的性能下降** | 将非常大的文件加载到内存中 | 增加 JVM 堆内存 (`-Xmx2g`) 或使用 `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` 分块处理文件 |

## 常见问题

**Q: Aspose.PSD 是否兼容所有 Java 版本？**  
A: 是的，它支持 Java 6.0 及更高版本，包括 Java 8、11 和 17。

**Q: 我可以在一次操作中应用多个调整图层吗？**  
A: 当然。添加反相图层后，您可以调用 `addBrightnessAdjustmentLayer()`、`addHueSaturationAdjustmentLayer()` 等方法来堆叠效果。

**Q: 我在哪里可以找到完整的 API 参考？**  
A: 完整的文档可在 [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/) 获取。

**Q: Aspose.PSD 有免费试用吗？**  
A: 有，您可以下载试用版 [Aspose.PSD trial download](https://releases.aspose.com/)。

**Q: 我如何获取用于测试的临时许可证？**  
A: 请求临时许可证 [temporary license request page](https://purchase.aspose.com/temporary-license/)。

**最后更新：** 2026-11-04  
**测试环境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## 相关教程

- [使用 Aspose.PSD for Java 向 PSD 文件添加层级调整图层](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [如何在 PSD 中添加调整图层 – 通道混合器 (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [如何编辑 PSD - 使用 Java 添加曲线调整图层](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}