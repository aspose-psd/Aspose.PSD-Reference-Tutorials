---
date: 2026-02-12
description: 学习如何使用 Aspose.PSD for Java 在 Java 中调整图像大小。提供包含 Resize Type 枚举的分步指南，以及将
  PSD 转换为 JPEG 的技巧。
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
title: Java 图像大小调整 - 在 Aspose.PSD for Java 中使用 Resize Type 枚举
url: /zh/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 调整图像大小（Java）：在 Aspose.PSD for Java 中使用 Resize Type 枚举

## 介绍

在 Java 应用程序中，调整图像大小是常见需求，使用 Aspose.PSD 可以轻松完成 **resize image java** 操作。在本教程中，您将学习如何使用强大的 Resize Type 枚举来 **resize image java**，并了解在调整大小后如何 **convert psd to jpeg**。无论您是构建桌面工具还是服务器端服务，这些步骤都能帮助您可靠地处理图像尺寸并实现高质量的图像调整。

## 快速答案
- **什么库处理 resize image java？** Aspose.PSD for Java。  
- **哪种 resize type 提供最佳质量？** `ResizeType.LanczosResample`。  
- **我可以在调整大小后将 PSD 转换为 JPEG 吗？** 是的——只需使用 `JpegOptions` 保存。  
- **生产环境是否需要许可证？** 生产使用需要有效的 Aspose.PSD 许可证。  
- **此方法适用于大批量处理吗？** 绝对适用；API 已针对性能进行优化。

## 什么是 Resize Image Java？

“resize image java” 指的是使用 Java 代码以编程方式更改图像的像素尺寸。Aspose.PSD 提供了简洁的 API，抽象了底层像素操作，让您专注于业务逻辑，而无需关注图像处理细节。

## 为什么使用 Resize Type 枚举？

Resize Type 枚举让您对重采样算法进行细粒度控制，从而在速度和质量之间取得平衡。对于大多数应用，`LanczosResample` 提供了很好的折中，能够在不显著影响性能的情况下产生清晰的结果。选择合适的 resize type 是实现高质量图像调整的关键。

## 前提条件

1. **Java 开发环境** – 已安装并配置 JDK 8+。  
2. **Aspose.PSD 库** – 从[网站](https://releases.aspose.com/psd/java/)下载并安装 Aspose.PSD 库。  
3. **示例 PSD 文件** – 准备好用于实验的示例 PSD 文件。您可以使用本教程中的 [sample.psd](Your Document Directory/sample.psd) 文件。

## 导入包

要开始，请在 Java 项目中导入必要的包：

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步骤 1：加载图像

首先，将现有图像加载到 `RasterImage` 类的实例中。使用以下代码片段：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## 步骤 2：调整图像大小

现在，使用 Resize Type 枚举对已加载的图像进行大小调整。在本例中，我们使用 Lanczos Resample 方法，它在 **how to resize image** 时能够提供高质量的效果：

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 步骤 3：保存调整后的图像

调整大小后，使用指定的尺寸和选定的 resize type 保存图像。在这里，我们还通过将结果保存为 JPEG 文件演示 **convert psd to jpeg**：

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

至此，您已经完成了完整的 **resize image java** 工作流，生成了高质量的图像调整结果以及可直接使用的 JPEG 输出。

## 常见问题及解决方案

- **图像在调整后出现模糊** – 尝试使用不同的 `ResizeType`，如 `Bicubic` 或 `NearestNeighbour`，以查看哪种在特定图像上产生最佳视觉效果。  
- **在大型 PSD 文件上出现 OutOfMemoryError** – 将图像分成更小的块处理或增大 JVM 堆大小（`-Xmx` 参数）。  

## 常见问答

### Q1：Aspose.PSD for Java 是否适用于小型和大型项目？

A1：绝对适用！Aspose.PSD for Java 旨在满足各种规模项目的需求，提供可扩展性和高效性。

### Q2：我可以使用除 Lanczos Resample 之外的其他 resize type 吗？

A2：可以，Aspose.PSD for Java 提供多种 resize type，例如 Nearest Neighbour、Bicubic 等。请查阅文档获取完整列表。

### Q3：在哪里可以找到 Aspose.PSD for Java 的更多支持？

A3：如有任何疑问或需要帮助，请访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34/)。

### Q4：Aspose.PSD for Java 是否提供免费试用？

A4：是的，您可以在 [此处](https://releases.aspose.com/) 获取免费试用版本。

### Q5：如何获取 Aspose.PSD for Java 的临时许可证？

A5：获取临时许可证，请访问 [此链接](https://purchase.aspose.com/temporary-license/)。

## 常见问题

**问：如何在不调整大小的情况下将 PSD 文件编程转换为 JPEG？**  
答：使用 `Image.load` 加载 PSD，然后调用 `image.save("output.jpg", new JpegOptions());`。

**问：在调整大小时是否可以保持原始 DPI？**  
答：可以，在保存之前为 `Image` 对象设置 `Resolution` 属性。

**问：我可以链式调用多个 resize 操作吗？**  
答：虽然可以多次调用 `resize`，但更高效的做法是一次性计算最终尺寸并进行一次 resize。

## 附加问答

**问：Resize Type 枚举会影响处理速度吗？**  
答：会，`NearestNeighbour` 等简单算法速度更快但可能导致质量下降，而 `LanczosResample` 在适度的性能开销下提供更高质量。

**问：我可以在多线程环境中调整图像大小吗？**  
答：Aspose.PSD API 对只读操作是线程安全的。若进行并发调整，请为每个线程创建独立的 `Image` 实例。

**问：在调整大小时如何处理带有 alpha 通道的图像？**  
答：库默认保留 alpha 透明度。如需将图像展平，请在保存前设置背景颜色。

**最后更新：** 2026-02-12  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}