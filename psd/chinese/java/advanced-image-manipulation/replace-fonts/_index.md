---
date: 2026-06-23
description: 了解如何使用 Aspose.PSD for Java 将 PSD 保存为 PNG、替换缺失的字体并导出图像——快速处理缺失字体的 PSD
  文件。
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: 替换字体
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何在 Java 中使用 Aspose 将 PSD 保存为 PNG 并替换缺失的字体
url: /zh/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 PSD 保存为 PNG – 在 Java 中替换缺失字体

## 介绍

如果您需要在 Photoshop (PSD) 文件中替换缺失或不需要的字体，同时 **save PSD as PNG**，Aspose PSD 字体替换可以让这一过程轻松完成。在 Java 应用程序中，您可以加载 PSD，告诉 Aspose 使用哪个回退字体，然后将修正后的图像导出为任意格式。本教程将带您完整了解工作流——从项目设置到导出更新后的 PNG——帮助您在不打开 Photoshop 的情况下可靠地 **handle missing fonts PSD** 场景。

## 快速答案
- **哪个库负责字体替换？** Aspose.PSD for Java  
- **实现大约需要多长时间？** 基本场景约 5‑10 分钟  
- **默认回退字体是什么？** 您可以设置任意 TrueType 字体，例如 “Arial”  
- **可以保存为 PNG 之外的格式吗？** 可以 – 支持 PSD、JPEG、BMP 等多种格式  
- **生产环境需要许可证吗？** 非试用使用时需要有效的 Aspose.PSD 许可证  

## 什么是 Aspose PSD 字体替换？

Aspose PSD 字体替换是指在库遇到 PSD 文件中缺失或不受支持的字体时，使用您指定的替代字体进行渲染的过程。这确保文本图层能够正确显示，无需在 Photoshop 中手动编辑，并且可以自动 **handle missing fonts PSD** 文件。

## 为什么选择 Aspose.PSD for Java？

Aspose.PSD for Java 提供了一套完整且高性能的解决方案，直接在 Java 代码中处理 Photoshop 文件，免除对 Photoshop 本身的依赖。它支持多种图层类型、效果和大文件尺寸，并提供简洁的 API 用于字体替换、图像转换和元数据处理。

- **功能完整的 PSD 处理** – Aspose.PSD 支持 **30+ 图层类型**、**20+ 效果**，并且能够在不将整个文档加载到内存的情况下处理高达 **2 GB** 的文件。  
- **跨平台** – 可在任何支持 Java 8+ 的操作系统上运行。  
- **无外部依赖** – 库内部自行处理字体替换，无需在应用中额外携带字体文件。  

## 如何使用 Aspose PSD 替换 PSD 中的缺失字体

要替换缺失字体，首先在加载选项中定义回退字体，然后加载 PSD 并渲染或保存图像。库会自动用您指定的字体替代缺失的字体，确保视觉输出符合预期，无需手动编辑。

## 前置条件

在开始之前，请确保您拥有：

- **Java Development Kit (JDK)** – 已安装 8 版或更高。  
- **Aspose.PSD for Java** – 从[发布页面](https://releases.aspose.com/psd/java/)下载最新 JAR。  
- **IDE** – IntelliJ IDEA、Eclipse 或您喜欢的任何编辑器。  

## 导入包

`PsdImage` 类表示内存中的 Photoshop 文档，提供对图层、文本和渲染功能的访问。`PsdLoadOptions` 控制文件读取方式，包括回退字体，而 `SaveOptions`（或特定格式的子类）定义图像写入方式。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步骤 1：设置文档目录

指定包含源 PSD 文件的文件夹。将占位符替换为您机器上的实际路径。

`File` 对象仅指向要处理的 PSD，无需额外配置。

```java
String dataDir = "Your Document Directory";
```

## 步骤 2：使用替代字体加载图像

创建 `PsdLoadOptions` 实例，设置默认替代字体（例如 **Arial**），然后加载 PSD。Aspose 会在遇到缺失字体时自动应用回退字体。

`PsdLoadOptions` 允许您定义加载行为，包括在导入阶段替代任何缺失字体的回退字体。

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## 步骤 3：将替换后的图像保存为 PNG

完成字体替换后，您可以将图像导出为任意受支持的格式。这里我们将其保存为 PNG，您也可以选择 JPEG、BMP，甚至重新保存为 PSD。

`PsdImage` 的 `save` 方法接受 `SaveOptions` 对象；使用 `PngOptions` 可确保输出为适合网页或后续处理的无损 PNG。

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## 如何在替换字体后将 PSD 保存为 PNG？

使用回退字体加载 PSD，然后调用 `psdImage.save("output.png", new PngOptions())`。此单行保存操作会生成完整渲染的 PNG，反映已替换的字体，使您可以在任何地方嵌入图像而无需担心缺失字体。请确保在保存前已应用替代字体，并可通过 `PngOptions` 对象调整 PNG 压缩设置以获得最佳文件大小。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| 替换后文本出现乱码 | 回退字体不包含所需字形 | 选择支持所需 Unicode 范围的字体（例如 “Arial Unicode MS”）。 |
| 大型 PSD 导致 `OutOfMemoryError` | 在堆内存不足的情况下加载高分辨率文件 | 增加 JVM 堆大小（`-Xmx2g`）或使用流式模式加载（如果可用）。 |
| 许可证异常 | 在生产环境使用试用版 | 在加载图像前应用有效的永久或临时许可证。 |

## 常见问答

**Q: 能否在 PSD 之外的其他图像格式中替换字体？**  
A: 可以。虽然主要场景是 PSD，但 Aspose.PSD 也支持 PNG、JPEG、BMP 和 TIFF，能够在任何包含文本图层的图像中进行字体替换。

**Q: 默认的替代字体是必须的吗？**  
A: 不是。您可以设置任意 TrueType 字体，或省略此设置让 Aspose 使用内部默认字体。

**Q: 使用 Aspose.PSD 是否有许可证要求？**  
A: 生产部署需要商业许可证。详情请参阅[购买页面](https://purchase.aspose.com/buy)。

**Q: 可以获取临时许可证用于测试吗？**  
A: 当然。Aspose 提供免费临时许可证供评估使用——请访问[临时许可证页面](https://purchase.aspose.com/temporary-license/)。

**Q: 在哪里可以获得更多支持或讨论 Aspose.PSD 相关问题？**  
A: 社区论坛是提问的好地方：[Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)。

**Q: 如何处理包含多种缺失字体的 PSD 文件？**  
A: 如示例只需设置一次默认替代字体——加载时会对 *所有* 缺失字体生效。

**Q: 是否可以在图像保存后再替换字体？**  
A: 字体替换必须在加载阶段完成。若需更改字体，请使用不同的替代字体重新加载 PSD 并再次保存。

## 结论

您已经完整了解了在 Java 中 **save psd as png** 的工作流——从导入相关类、配置回退字体、加载 PSD 到导出修正后的 PNG。将此模式集成到您的图像处理流水线中，可确保所有 PSD 资源的排版一致，并自动 **handle missing fonts PSD**。

---

**Last Updated:** 2026-06-23  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose

## 相关教程

- [Settings for Replacing Missing Fonts in Aspose.PSD for Java](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}