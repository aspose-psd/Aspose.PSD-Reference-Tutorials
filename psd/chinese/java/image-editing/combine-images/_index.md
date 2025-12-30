---
date: 2025-12-30
description: 了解如何使用 Aspose.PSD 在 Java 中通过合并两张图像来创建 PSD 文件。按照我们的分步指南，快速将图像合并为 PSD 文件。
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: 如何在 Java 中创建 PSD 文件 – 使用 Aspose.PSD 合并图像
url: /zh/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 创建 PSD 文件 Java – 使用 Aspose.PSD 合并图像

## 介绍

如果您需要通过合并多张图片 **create a PSD file in Java**，Aspose.PSD 能让这项工作变得简单。在本教程中，我们将演示如何将两张图像合并到一个 PSD 画布中，说明这种方法的优势，并提供可直接运行的代码。完成后，您将能够 **combine two images Java** 风格地生成专业的分层文件。

## 快速答案
- **What library is best for merging images into PSD?** Aspose.PSD for Java.
- **How long does the implementation take?** About 10‑15 minutes for a basic combine.
- **Do I need a license?** A free trial works for testing; a commercial license is required for production.
- **Can I add more than two images?** Yes – repeat the `drawImage` calls for each additional layer.
- **Which Java version is supported?** Java 8 and newer.

## 前提条件

在开始之前，请确保您具备以下条件：

1. **Aspose.PSD Library** – download it from [here](https://releases.aspose.com/psd/java/)。  
2. **Java Development Kit (JDK)** – Java 8+ is recommended.  
3. **Document Directory** – a folder on your machine where the source images and the resulting PSD will be stored.

## 导入包

首先在项目中导入所需的 Aspose.PSD 类：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## 步骤指南

### 步骤 1：创建 PSD 选项（准备文件）

我们首先创建一个 `PsdOptions` 实例，用于保存输出设置。

```java
PsdOptions imageOptions = new PsdOptions();
```

### 步骤 2：设置 FileCreateSource（定义 PSD 保存位置）

为选项分配一个 `FileCreateSource`，指向期望的结果文件。

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### 步骤 3：创建 Image 实例（初始化画布大小）

使用该选项创建一个 `Image` 对象，并指定 600 × 600 像素的画布。

```java
Image image = Image.create(imageOptions, 600, 600);
```

### 步骤 4：初始化 Graphics 并绘制第一张图片

`Graphics` 对象允许我们在画布上绘制。我们先将背景清为白色，然后在左半部分绘制第一张源图像。

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### 步骤 5：绘制第二张图片（完成合并）

接下来将第二张图像放置在同一画布的右半部分。

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### 步骤 6：保存生成的 PSD 文件

最后，将合并后的画布持久化到磁盘。

```java
image.save();
```

恭喜！您已成功 **merge images into PSD** 并在 Java 中创建了 PSD 文件。

## 为什么使用 Aspose.PSD 合并图像？

- **Layer‑aware** – each `drawImage` call adds a separate layer you can edit later.  
- **Format flexibility** – supports PSD, PNG, JPEG, BMP, and more.  
- **No native dependencies** – pure Java, works on any OS that runs the JDK.  

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| `File not found` error when loading source images | Incorrect `dataDir` path | Verify `dataDir` points to the folder containing `example1.psd` and `example2.psd`. |
| Output PSD is blank | `graphics.clear` called after drawing | Ensure `graphics.clear(Color.getWhite())` is executed **before** any `drawImage` calls. |
| License exception at runtime | Missing or expired Aspose.PSD license | Apply a valid license using `License license = new License(); license.setLicense("Aspose.PSD.lic");` before any API call. |

## 常见问答

### Q1：Aspose.PSD 是否兼容所有图像格式？

A1: Aspose.PSD 主要关注 PSD 文件格式。不过，它也支持多种其他格式的输入和输出。

### Q2：我可以对合并后的图像进行额外修改吗？

A2: 当然可以！在合并图像后，您可以使用 Aspose.PSD 丰富的功能进一步操作生成的 PSD。

### Q3：使用 Aspose.PSD 是否有许可要求？

A3: 是的，商业使用需要有效的许可证。您可以从 [here](https://purchase.aspose.com/buy) 获取。

### Q4：Aspose.PSD 是否提供免费试用？

A4: 是的，您可以在 [here](https://releases.aspose.com/) 进行免费试用。

### Q5：在哪里可以找到 Aspose.PSD 相关问题的支持？

A5: 请访问 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 获取社区支持和讨论。

**最后更新：** 2025-12-30  
**测试环境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}