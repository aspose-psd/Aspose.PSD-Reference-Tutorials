---
date: 2026-04-03
description: 了解如何使用 Aspose.PSD for Java 通过合并图层来减小 PSD 文件大小。本分步指南展示了如何快速合并 PSD 文件。
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: 通过扁平化图层减小 PSD 文件大小 – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: 通过扁平化图层减小 PSD 文件大小 – Aspose.PSD Java
url: /zh/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 通过扁平化图层减小 PSD 文件大小 – Aspose.PSD Java

## 介绍

如果你曾经打开过 Photoshop 文档并想知道如何**减小 PSD 文件大小**，扁平化图层是最有效的技巧之一。使用 Aspose.PSD for Java，你可以以编程方式扁平化整个 PSD，或仅合并你选择的图层，从而在不牺牲视觉质量的前提下细致地控制文件体积。在本教程中，我们将演示两种方法——扁平化整个图像和合并特定图层——帮助你快速缩小 PSD 文件并保持工作流顺畅。

## 快速答疑
- **扁平化有什么作用？** 它将可见图层合并为单个背景图层，去除图层信息，通常可以减小文件大小。  
- **我可以只扁平化选定的图层吗？** 可以，你可以合并特定图层，而保持其他图层不变。  
- **我需要许可证吗？** 免费试用可用于开发；生产环境需要商业许可证。  
- **需要哪个 Java 版本？** JDK 8 或更高版本。  
- **扁平化会影响图像质量吗？** 不会，视觉外观保持不变，仅图层结构会改变。

## 什么是“减小 PSD 文件大小”？

减小 PSD 文件大小是指删除不必要的数据——例如多余的图层、隐藏的通道或过多的元数据——使文件更轻便，加载、共享或处理速度更快。扁平化图层是一种常用技术，因为它在保留最终合成图像的同时丢弃了独立的图层对象。

## 为什么使用 Aspose.PSD for Java 扁平化图层？

- **自动化：** 无需手动打开 Photoshop；可直接集成到你的 Java 应用程序中。  
- **精确控制：** 可以选择扁平化整个文档或仅可见图层（`flattenImage`），或合并选定图层（`mergeLayers`）。  
- **性能提升：** 更小的文件加载更快，在后续处理过程中占用更少的内存。  
- **跨平台：** 在任何支持 Java 的操作系统上均可运行。

## 前置条件

1. **Java Development Kit (JDK)：** 已安装 JDK 8 或更高版本。  
2. **Aspose.PSD for Java：** 从[此处](https://releases.aspose.com/psd/java/)下载库。  
3. **IDE：** IntelliJ IDEA、Eclipse 或任何兼容 Java 的 IDE。  
4. **基本的 Java 知识：** 有帮助，但并非执行步骤的必需条件。  
5. **示例 PSD：** 包含多个图层的文件（我们将使用 `ThreeRegularLayersSemiTransparent.psd`）。

现在所有准备工作已就绪，让我们深入代码。

## 导入包

首先，导入必要的 Aspose.PSD 类：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

这些导入使我们能够加载 PSD 文件、操作其图层并保存结果。

## 步骤 1：扁平化整个 PSD 图像

扁平化整个图像是**减小 PSD 文件大小**的最快方法，因为它会删除所有单独的图层数据。

### 1.1 加载 PSD 文件

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 扁平化图像

```java
im.flattenImage();
```

### 1.3 保存扁平化后的图像

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

你的新文件现在只包含一个背景图层，通常会导致 PSD 文件体积更小。

## 步骤 2：合并特定图层（如何选择性扁平化 PSD）

有时你只想**扁平化可见图层**，或在保留其他图层可编辑的情况下合并部分图层。

### 2.1 再次加载 PSD 文件

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 确认并选择图层

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 合并图层

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 用合并后的图层替换现有图层

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 保存更新后的 PSD 文件

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

现在 PSD 只包含合并后的图层，实现了在保留所需图层的同时减小文件体积。

## 常见问题与技巧

- **扁平化前备份：** 一旦图层被扁平化，操作无法撤销。请保留原始 PSD 的副本。  
- **可见性重要：** `flattenImage()` 只合并*可见*图层。隐藏任何不想包含的图层。  
- **内存使用：** 大型 PSD 可能占用大量内存；请考虑在内存充足的机器上进行处理。  
- **混合模式：** 合并时会保留每个图层的混合模式，因此视觉结果与 Photoshop 中看到的相同。

## 常见问题

**问：我可以撤销 Aspose.PSD 中的图层扁平化吗？**  
答：不能，扁平化是不可逆的。请始终保留原始文件的备份。

**问：是否可以只扁平化可见图层？**  
答：可以。`flattenImage()` 会遵循图层的可见性，在调用该方法前请隐藏任何不想扁平化的图层。

**问：扁平化图层会减小文件大小吗？**  
答：通常会。删除图层数据和元数据往往会使 PSD 更小，尽管具体减小幅度取决于内容。

**问：我可以合并具有不同混合模式的图层吗？**  
答：当然可以。Aspose.PSD 在合并图层时会保留其混合模式所产生的视觉效果。

**问：如果尝试合并非相邻的图层会怎样？**  
答：Aspose.PSD 允许合并任意图层，无论它们在堆栈中的顺序如何；结果会体现合并后的外观。

---

**最后更新：** 2026-04-03  
**测试环境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}