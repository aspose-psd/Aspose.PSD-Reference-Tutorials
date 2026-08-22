---
date: 2026-07-22
description: 了解如何使用 Aspose.PSD 在 Java 中将 PSD 保存为 PNG、保留 PNG 透明度并旋转 PSD 图层。提供分步指南、免代码说明和故障排除技巧。
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: 使用 Aspose.PSD 在 Java 中将 PSD 保存为 PNG 并旋转图层
og_description: 使用 Aspose.PSD for Java 将 PSD 保存为 PNG。保留透明度、旋转图层，并仅用几行代码导出 PNG——非常适合自动化工作流。
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: 使用 Aspose.PSD 在 Java 中将 PSD 保存为 PNG 并旋转图层
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: 使用 Aspose.PSD 在 Java 中将 PSD 保存为 PNG 并旋转图层
url: /zh/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## 相关教程

- [在 Aspose.PSD for Java 中将 PSD 保存为 PNG 并应用渲染投影阴影](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [如何使用 Aspose.PSD for Java 压缩 PNG 文件](/psd/java/optimizing-png-files/compress-png-files/)
- [如何在 Java 中使用 Aspose.PSD 旋转图像](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# 使用 Aspose.PSD 在 Java 中将 PSD 保存为 PNG 并旋转图层

## 介绍
如果您需要 **将 PSD 保存为 PNG** 并同时旋转图层，本指南适合您。无论您是在构建批处理工具、需要即时图像处理的 Web 服务，还是仅仅在自动化设计工作流，使用编程方式完成这些操作都能节省时间并消除对 Adobe Photoshop 的依赖。在本教程中，我们将演示 **如何旋转 PSD 图层** 并使用 Aspose.PSD for Java 将结果导出为 PNG。让我们动手，让您的设计工作流顺畅运行！

## 快速答案
- **我可以使用哪个库？** Aspose.PSD for Java  
- **我能一次性同时旋转并将 PSD 保存为 PNG 吗？** 是的 – 先旋转 PSD，然后保存为 PNG  
- **我需要许可证吗？** 免费试用可用于测试；生产环境需要付费许可证  
- **支持哪个 Java 版本？** Java 8 及更高版本  
- **PNG 输出是否透明？** 是的，当您设置 `PngColorType.TruecolorWithAlpha` 时  

## 什么是“将 PSD 转换为 PNG”？
将 Photoshop 文档（PSD）转换为 PNG 图像会将视觉内容——包括图层、蒙版和 Alpha 通道——提取到一种广泛支持的光栅格式中，同时保留透明度。这使得 PNG 成为网页图形、缩略图以及后续图像处理的理想选择。生成的 PNG 可直接用于网页、移动应用，或由其他图像库进一步处理。

## 为什么使用 Aspose.PSD for Java 将 PSD 保存为 PNG 并旋转 PSD 图层？
Aspose.PSD 让您 **将 PSD 保存为 PNG** 并在无需安装 Photoshop 的情况下旋转图层。它支持 **50 多种输入和输出格式**，在使用不到 200 MB 内存的情况下处理数百页的 PSD 文件，并可在 Windows、Linux 和 macOS 上运行。API 只需几行代码，即可实现高保真结果，并内置对图层效果、蒙版和 Alpha 通道的处理。

## 前置条件
在开始编写代码之前，请确保您具备以下条件：

- **Java 开发工具包 (JDK)** – 从 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) 下载。  
- **集成开发环境 (IDE)** – IntelliJ IDEA、Eclipse 或 NetBeans 都可以。  
- **Aspose.PSD for Java 库** – 从 [release page](https://releases.aspose.com/psd/java/) 获取最新的 JAR。  
- **基本的 Java 知识** – 熟悉类、对象和异常处理。

## 步骤指南

### 步骤 1：设置 Java 项目
在 IDE 中创建一个新的 Java 项目，并将 Aspose.PSD JAR 添加到项目的构建路径。

### 步骤 2：导入所需类
`PsdImage` 是表示 Photoshop 文档的核心类。`PngOptions` 控制 PNG 的特定设置，`RotateFlipType` 定义旋转和翻转操作。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

这些导入让您能够访问图像加载、旋转以及 PNG‑特定选项。

### 步骤 3：定义文件路径
指定源 PSD 所在位置以及输出文件的写入路径。测试时使用绝对路径可避免 “文件未找到” 错误。

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **专业提示：** 将路径存放在配置文件中，可在大型项目中更易维护。

### 步骤 4：加载 PSD 文件
`PsdImage` 将整个 Photoshop 文档（包括所有图层、蒙版和效果）加载到可操作的对象中。

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

现在 `im` 代表完整的 PSD，已准备好进行转换。

### 步骤 5：旋转图像（如何旋转 PSD）
`RotateFlipType` 列举了所有支持的旋转和翻转方式。在本例中我们将图像旋转 270° 并在两个轴上翻转，这会在交换宽高的同时镜像图像。

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

随意尝试其他值，例如 `Rotate90FlipNone` 或 `Rotate180FlipX`。

### 步骤 6：将旋转后的图像保存为 PNG（将 PSD 保存为 PNG）
配置 `PngOptions` 以保持透明度（`PngColorType.TruecolorWithAlpha`），然后调用 `save`。PNG 将保留图层透明度，确保在 Web 或移动应用中无缝使用。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

生成的 PNG 保留了 Alpha 通道，适合合成或进一步处理。

### 步骤 7：保存修改后的 PSD（可选）
如果您还需要一个已应用旋转的新 PSD，可以将修改后的 `PsdImage` 再次保存到磁盘。

```java
im.save(psdPath);
```

这样您既拥有 PNG 预览，又拥有更新后的 PSD 文件。

## 常见问题及解决方案
- **文件未找到：** 验证 `dataDir` 以路径分隔符（`/` 或 `\`）结尾。  
- **大型 PSD 导致 OutOfMemoryError：** 增加 JVM 堆大小（`-Xmx2g`）。  
- **透明度丢失：** 确保已设置 `PngColorType.TruecolorWithAlpha`；否则 PNG 将没有 alpha 通道。  
- **翻转 PSD 图像未如预期工作：** 再次检查所选的 `RotateFlipType` 常量；某些常量在一步中同时进行旋转和翻转。

## 常见问答

**Q: 我可以旋转 PSD 文件中的特定图层吗？**  
A: 可以，在遍历 `im.getLayers()` 后调用 `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`。

**Q: Aspose.PSD for Java 有性能限制吗？**  
A: 该库对大多数文件都能高效处理，但极大的 PSD（>500 MB）可能需要额外的内存或流式选项。

**Q: Aspose.PSD 免费使用吗？**  
A: Aspose 提供免费试用，但生产环境需要付费许可证。请参阅 [temporary license](https://purchase.aspose.com/temporary-license/) 进行测试。

**Q: 在哪里可以找到详细文档？**  
A: 完整文档可在 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) 查看。

**Q: 使用 Aspose.PSD 时遇到问题怎么办？**  
A: 可通过 [Aspose Support Forum](https://forum.aspose.com/c/psd/34) 获取帮助。

**Q: 将 PSD 转换为 PNG 是否保留图层效果？**  
A: 是的，只要使用 `PngColorType.TruecolorWithAlpha` 保存，大多数视觉效果都会栅格化到 PNG 中。

**Q: 能批量处理多个 PSD 文件吗？**  
A: 完全可以。将代码放入循环中，遍历目录下的 PSD 文件即可。

**Q: 可以设置 PNG 的压缩级别吗？**  
A: `PngOptions` 提供 `setCompressionLevel(int)` 方法，可微调输出大小。

**Q: 是否需要关闭图像对象？**  
A: `PsdImage` 实现了 `Closeable` 接口；使用 try‑with‑resources 或在 `finally` 块中调用 `im.close()`。

**Q: 旋转后的 PNG 会与原始尺寸相同吗？**  
A: 旋转 90° 或 270° 会交换宽高，PNG 会自动反映新的方向。

## 结论
通过使用 Aspose.PSD for Java，您可以 **将 PSD 保存为 PNG**、**保留 PNG 透明度**，并 **旋转 PSD 图层**，仅需几行代码。这种方式消除了对 Photoshop 的依赖，加快了自动化工作流，并让您完全掌控图像输出。请在自己的项目中尝试，感受节省的时间与效率！

---

**最后更新：** 2026-07-22  
**测试环境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}