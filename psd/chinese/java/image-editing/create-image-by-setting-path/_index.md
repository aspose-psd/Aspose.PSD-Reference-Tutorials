---
date: 2026-07-03
description: 了解如何使用 Aspose.PSD for Java 通过设置路径创建 PSD 图像（Java）。请按照我们的分步指南，实现无缝的图像生成。
keywords:
- create psd image java
- create image by path
- Aspose.PSD Java
linktitle: 通过设置路径创建图像
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to create psd image java by setting path using Aspose.PSD
    for Java. Follow our step-by-step guide for seamless image generation.
  headline: Create PSD Image Java by Setting Path with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it works flawlessly with Eclipse, IntelliJ IDEA, NetBeans, and any
      IDE that supports Maven or Gradle.
    question: Is Aspose.PSD compatible with different Java IDEs?
  - answer: Absolutely—purchase a commercial license to remove evaluation limits and
      obtain full support.
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      assistance or open a support ticket through your license portal.
    question: Where can I get help if I run into trouble?
  - answer: Yes, you can access the free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can obtain a temporary license for testing purposes [here](https://purchase.aspose.com/temporary-license/).
    question: Do I need a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD 通过设置路径创建 PSD 图像（Java）
url: /zh/java/image-editing/create-image-by-setting-path/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 通过设置路径使用 Aspose.PSD 创建 PSD 图像 Java

## 介绍

在本教程中，您将学习如何通过显式设置文件系统路径使用 Aspose.PSD for Java **创建 psd image java**。无论是构建批处理流水线还是即时生成图形，控制输出位置都能为您提供完全的灵活性。我们将逐步演示每个配置步骤，解释每个设置为何重要，并以可直接运行的示例结束。有关其他 Aspose 产品，请访问[此处](https://releases.aspose.com/)。

## 快速答案
- **“create psd image java” 是什么意思？** 它指的是使用 Java 代码以编程方式生成兼容 Photoshop 的 PSD 文件。  
- **哪个库负责此功能？** Aspose.PSD for Java 提供了完整的 API 用于创建、编辑和保存 PSD 文件。  
- **我需要许可证才能尝试吗？** 提供 30 天免费试用；生产环境需要商业许可证。  
- **我可以设置自定义输出文件夹吗？** 可以——只需通过 `PsdOptions.Source` 提供目录路径。  
- **API 是否兼容 Java 8 及更高版本？** 当然，支持 Java 8 到 Java 21。

## 什么是 create psd image java？
*Create psd image java* 是使用 Java 代码从头构建兼容 Photoshop 的 PSD 文件的过程。Aspose.PSD 的 `Image` 类表示画布，而 `PsdOptions` 让您控制压缩、颜色模式和输出位置。此功能使开发者能够在无需安装 Photoshop 的情况下，以编程方式生成分层图形。

## 为什么使用 Aspose.PSD 通过路径创建 PSD 图像？
Aspose.PSD 支持 **100 多项 Photoshop 功能**，可处理高达 **2 GB** 的文件而无需将整个文档加载到内存中，并可在 **所有主流操作系统** 上运行。通过显式路径控制，您可以避免使用临时位置，轻松将 PSD 生成无缝集成到自动化工作流中，无论是小图标还是多层高分辨率艺术作品。

## 先决条件

在开始之前，请确认您已具备：

- 基本的 Java 开发经验。  
- 已安装 Aspose.PSD for Java 库。您可以在[此处](https://releases.aspose.com/psd/java/)下载。  

您可以在[购买页面](https://purchase.aspose.com/buy)购买许可证。

## 导入包

`com.aspose.psd` 命名空间包含您需要的所有类。请在源文件顶部导入它们：

`Image` 是表示用于创建或编辑 PSD 文件的光栅画布的核心类。  
`CompressionMethod` 枚举了 PSD 文件支持的压缩算法。  
`PsdOptions` 保存压缩和源路径等配置。  
`FileCreateSource` 指定输出文件路径以及是否为临时文件。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;

```

## 如何设置文档目录路径？

设置新 PSD 文件将写入的文件夹可让您完全控制文件组织，并防止库使用默认的临时位置。请使用绝对路径以确保确定性，或使用相对路径（相对于项目工作目录）。在继续之前，请确保目录已存在或通过代码创建它。

```java
String dataDir = "Your Document Directory";
```

## 步骤 1：设置文档目录路径

设置文档目录的路径，以便在其中创建图像。

```java
String dataDir = "Your Document Directory";
```

```java
String desName = dataDir + "CreatingAnImageBySettingPath_out.psd";
```

## 如何定义输出文件名？

将目录路径与描述性文件名组合形成完整的输出路径。此步骤确保 `Image` 对象明确知道写入位置，避免出现模糊的文件位置。请包含 `.psd` 扩展名，并考虑在批处理操作中使用时间戳或唯一标识符。

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setCompressionMethod(CompressionMethod.RLE);
```

## 步骤 2：定义输出文件名

定义输出文件名，包括文档目录。

```java
String desName = dataDir + "CreatingAnImageBySettingPath_out.psd";
```

```java
psdOptions.setSource(new FileCreateSource(desName, false));
```

## 如何配置 PSD 文件的压缩？

选择一种在文件大小和处理速度之间取得平衡的压缩方法。RLE（行程长度编码）提供快速压缩且尺寸适中，而 ZIP 在提供更高压缩率的同时会消耗更多 CPU 时间。在创建图像之前，请在 `PsdOptions` 实例上设置所需的方法。

```java
Image image = Image.create(psdOptions, 500, 500);
```

## 步骤 3：配置 PsdOptions

创建 PsdOptions 实例并配置其属性，例如压缩方法。

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setCompressionMethod(CompressionMethod.RLE);
```

```java
image.save();
```

## 如何为临时或永久文件设置 Source 属性？

`Source` 属性告诉 Aspose.PSD 输出文件是临时工作区还是最终产品。将 `isTemporary` 标志设为 `false`，即可确保文件永久写入您指定的位置，并可立即供其他进程使用。

CODE_BLOCK_PLACEHOLDER_7_END

## 步骤 4：设置 Source 属性

为 PsdOptions 实例定义 source 属性，指定输出文件及其是否为临时文件。

```java
psdOptions.setSource(new FileCreateSource(desName, false));
```

CODE_BLOCK_PLACEHOLDER_8_END

## 如何使用特定尺寸创建 PSD 图像？

`Image.create` 使用您提供的尺寸生成新的空白画布，并应用在 `PsdOptions` 中配置的选项。此方法返回一个 `Image` 对象，您可以进一步操作、添加图层，或在画布准备好后直接保存到磁盘。

CODE_BLOCK_PLACEHOLDER_9_END

## 步骤 5：创建图像

创建 Image 实例并通过传入 PsdOptions 对象和图像尺寸调用 Create 方法。

```java
Image image = Image.create(psdOptions, 500, 500);
```

CODE_BLOCK_PLACEHOLDER_10_END

## 如何将生成的 PSD 文件保存到磁盘？

在 `Image` 实例上调用 `save` 方法，将图像数据写入先前定义的路径。该方法遵循压缩设置并确保文件正确关闭，使其可立即使用或分发。

CODE_BLOCK_PLACEHOLDER_11_END

## 步骤 6：保存图像

保存创建的图像。

```java
image.save();
```

## 常见问题及解决方案

- **路径未找到错误：** 验证目录是否存在以及应用程序是否具有写入权限。使用 `new File(path).mkdirs()` 创建缺失的文件夹。  
- **不支持的压缩异常：** 确保使用的压缩方法受目标 PSD 版本支持（例如，PSD‑v3 使用 ZIP）。  
- **大图像内存溢出：** 将 `psdOptions.isMemoryOptimized = true` 设置为流式处理数据，而不是一次性加载整个图像到 RAM。

## 常见问答

**问：Aspose.PSD 是否兼容不同的 Java IDE？**  
答：是的，它可在 Eclipse、IntelliJ IDEA、NetBeans 以及任何支持 Maven 或 Gradle 的 IDE 中无缝工作。

**问：我可以在商业项目中使用 Aspose.PSD 吗？**  
答：当然——购买商业许可证即可解除评估限制并获得完整支持。

**问：如果遇到问题，我该在哪里获取帮助？**  
答：访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34) 获取社区帮助，或通过许可证门户提交支持工单。

**问：是否提供免费试用？**  
答：是的，您可以在[此处](https://releases.aspose.com/)获取免费试用。

**问：我需要临时许可证进行测试吗？**  
答：您可以在[此处](https://purchase.aspose.com/temporary-license/)获取用于测试的临时许可证。

## 结论

我们已覆盖通过 Aspose.PSD 设置自定义输出路径来 **create psd image java** 的所有步骤。通过控制目录、文件名、压缩和 source 选项，您可以完全掌握生成的 PSD 文件——无论是用于自动化批处理作业，还是在企业应用中动态生成图形。

---

**最后更新：** 2026-07-03  
**测试于：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [在 Aspose.PSD for Java 中使用流创建图像](/psd/java/image-editing/create-image-using-stream/)
- [使用 Aspose.PSD 简单缩放 – Java 图像处理库](/psd/java/basic-image-operations/simple-resizing/)
- [使用 Aspose.PSD 验证图像透明度 Java](/psd/java/basic-image-operations/verify-image-transparency/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}