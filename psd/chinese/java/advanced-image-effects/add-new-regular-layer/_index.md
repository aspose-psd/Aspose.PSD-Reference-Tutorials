---
date: 2026-02-01
description: 了解如何使用 Aspose.PSD for Java 将 PSD 导出为 PNG 并创建新的 PSD 图层。本分步教程涵盖 PSD 图像处理以及将
  PSD 转换为 PNG。
linktitle: Add a New Regular Layer to PSD
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 将 PSD 导出为 PNG 并添加新普通图层
url: /zh/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 PSD 导出为 PNG 并使用 Aspose.PSD for Java 添加新普通图层

## 介绍

在本 **aspose psd tutorial** 中，您将学习如何 **export PSD to PNG**，同时在同一文件中 **创建一个新普通图层**。无论是生成网页缩略图、为设计流水线准备资源，还是仅仅尝试 **psd image manipulation**，Aspose.PSD for Java 都能为您提供完整的编程控制。我们将逐步演示从加载源文件到保存更新后的 PSD 以及 PNG 副本的全过程，让您立即开始操作 PSD 图层。

## 如何使用 Aspose.PSD 将 PSD 导出为 PNG

将 PSD 导出为 PNG 是一个两步过程：首先添加或修改所需的图层，然后使用 `PngOptions` 实例调用 `save`。这种方式可以在一次流畅的操作中 **convert PSD to PNG** 或 **export PSD as PNG**。

## 什么是普通图层，为什么要添加新的 PSD 图层？

**普通图层** 是一种基本的光栅图层，可容纳像素数据、透明度和位置信息。添加新的 PSD 图层可以在不改变现有艺术作品的前提下注入图形、水印或占位符。这在需要 **add layer to PSD** 进行自动化批处理时尤为有用。

## 快速答疑
- **Can I export PSD to PNG with one call?** 是的，添加图层后即可使用 `PngOptions` 调用 `save`。
- **Do I need a license for development?** 临时许可证可用于测试；生产环境需要正式许可证。
- **Which Java version is supported?** Aspose.PSD 支持 Java 8 及更高版本。
- **Is layer positioning pixel‑based?** 是的，您可以以像素为单位设置 left、top、right、bottom 坐标。
- **Will the PNG retain layer transparency?** PNG 将包含所有可见图层的合并结果。

## 前置条件

在开始之前，请确保您拥有：

- **Java 开发环境** – 已安装 JDK 8+ 以及构建工具（Maven/Gradle）。
- **Aspose.PSD for Java** – 从官方站点[此处](https://releases.aspose.com/psd/java/)下载最新 JAR。
- **示例 PSD 文件** – 示例中使用 `OneLayer.psd`。

## 导入包

在 Java 类中添加所需的导入。这些类提供了 **psd image manipulation** 和图层处理的核心功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 步骤 1：加载 PSD 文件

首先加载要修改的现有 PSD。这会得到一个可供操作的 `PsdImage` 对象。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 步骤 2：准备像素数据和矩形区域

我们将创建两个像素缓冲区 (`int[]`) 并定义新图层绘制的矩形区域。这是 **creating a new PSD layer** 的基础。

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## 步骤 3：初始化图层数据

为像素缓冲区填充默认的 ARGB 值。数值 `-10000000` 对应半透明的深色阴影。

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## 步骤 4：添加普通图层（操作 PSD 图层）

现在我们 **add regular layers** 到 PSD 图像并设置它们的边界。这演示了如何以编程方式 **manipulate PSD layers** 并有效 **add layer to PSD**。

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## 步骤 5：导出 PSD 为 PNG 并保存更新后的 PSD

图层就位后，保存修改后的文档。首先将结果导出为 PNG（**export psd to png** 步骤），随后将带有新图层的 PSD 持久化。

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **专业提示：** 如果您只需要 PNG，可以跳过 PSD 的 `save` 调用，直接使用 `PngOptions` 调用 `save`。

## 常见问题与排查

| 症状 | 可能原因 | 解决办法 |
|------|----------|----------|
| PNG 显示为空白 | 图层不可见或完全透明 | 确保设置了非透明像素值或调用 `layer.setVisible(true)`。 |
| `ArrayIndexOutOfBoundsException` | 矩形尺寸与像素数组长度不匹配 | 验证 `rect.width * rect.height == dataArray.length`。 |
| 运行时出现 LicenseException | 未加载有效许可证 | 在调用任何 API 方法前加载临时或正式许可证。 |

## 常见问答

**Q: Aspose.PSD 是否兼容 Java 8？**  
A: 是的，Aspose.PSD 支持 Java 8 及更高版本。

**Q: 我可以对添加的图层进行变换（旋转、缩放）吗？**  
A: 完全可以！`Layer` 类提供 `rotate`、`scale`、`translate` 等方法，实现完整的变换控制。

**Q: 哪里可以找到更多 Aspose.PSD 文档？**  
A: 详细的 API 文档请访问[此处](https://reference.aspose.com/psd/java/)。

**Q: 如何获取 Aspose.PSD 的临时许可证？**  
A: 请前往临时许可证页面[此处](https://purchase.aspose.com/temporary-license/)。  

**Q: 是否有 Aspose.PSD 的社区论坛？**  
A: 有，您可以在 Aspose 论坛[此处](https://forum.aspose.com/c/psd/34)参与讨论。

## 结论

您现在已经掌握了如何使用 Aspose.PSD for Java **export PSD to PNG** 并 **add new regular layers**。此工作流展示了核心的 **psd image manipulation** 能力：加载文件、创建图层、填充像素数据以及导出最终合成。欢迎尝试不同的矩形尺寸、像素颜色或图层效果，以满足项目的特定需求。

---

**Last Updated:** 2026-02-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}