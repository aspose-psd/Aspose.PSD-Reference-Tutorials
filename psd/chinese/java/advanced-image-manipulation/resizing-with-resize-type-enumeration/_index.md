---
title: 使用 Aspose.PSD for Java 中的 Resize 类型枚举调整大小
linktitle: 使用 Resize 类型枚举调整大小
second_title: Aspose.PSD Java API
description: 掌握使用 Aspose.PSD 在 Java 中调整图像大小的方法。使用 Resize Type Enumeration 的分步指南。
weight: 18
url: /zh/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 中的 Resize 类型枚举调整大小

## 介绍

在不断发展的 Java 开发领域中，高效的图像处理是开发人员经常遇到的一个关键问题。Aspose.PSD for Java 是一款功能强大的解决方案，它通过 Resize Type Enumeration 的额外优势，为调整图像大小提供了无缝的体验。在本教程中，我们将深入研究使用 Aspose.PSD for Java 调整图像大小的复杂性，分解每个步骤以确保全面理解。

## 先决条件

在开始本教程之前，请确保您已满足以下先决条件：

1. Java 开发环境：确保您的机器上已设置 Java 开发环境。

2. Aspose.PSD 库：从[网站](https://releases.aspose.com/psd/java/).

3. 示例 PSD 文件：准备一个示例 PSD 文件以供实验。您可以使用[本教程的 sample.psd](您的文档目录/sample.psd) 文件。

## 导入包

首先，将必要的包导入到你的 Java 项目中：

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步骤 1：加载图像

首先将现有图像加载到`RasterImage`类。使用以下代码片段：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//将现有图像加载到 RasterImage 类的实例中
Image image = Image.load(sourceFile);
```

## 第 2 步：调整图像大小

现在，使用 Resize Type Enumeration 调整加载的图像的大小。在此示例中，我们使用 Lanczos Resample 方法：

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 步骤 3：保存调整大小后的图像

调整大小后，使用指定的尺寸和所选的调整大小类型保存图像。在这里，我们将其保存为 JPEG 文件：

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

就这样！您已成功使用 Aspose.PSD for Java 中的 Resize Type Enumeration 调整了图像大小。

总之，Aspose.PSD for Java 提供了一个强大的图像处理平台，而 Resize 类型枚举为这个过程增加了一层灵活性。无论您是在处理小型项目还是大型应用程序，掌握这些步骤都可以让您无缝处理图像大小调整。

## 常见问题解答

### 问题1：Aspose.PSD for Java 是否适合小型和大型项目？

A1：当然！Aspose.PSD for Java 旨在满足各种规模的项目，提供可扩展性和效率。

### 问题 2：我可以使用除了 Lanczos Resample 之外的其他调整大小类型吗？

A2：是的，Aspose.PSD for Java 提供各种调整大小类型，例如最近邻、双三次等等。查看文档以获取完整列表。

### 问题 3：在哪里可以找到对 Aspose.PSD for Java 的额外支持？

 A3：如有任何疑问或需要帮助，请访问[Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34).

### 问题4：Aspose.PSD for Java 有免费试用版吗？

 A4：是的，您可以访问免费试用版[这里](https://releases.aspose.com/).

### Q5: 如何获取 Aspose.PSD for Java 的临时许可证？

 A5：要获取临时许可证，请访问[此链接](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
