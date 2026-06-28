---
date: 2026-06-28
description: 了解如何使用 Aspose.PSD 在 Java 中合并图像，将两张图片合并到 PSD 画布，并在几分钟内生成分层文件。
keywords:
- combine images java
- java graphics draw image
- merge images into psd
linktitle: 合并图像
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  headline: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  type: TechArticle
- description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  name: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  steps:
  - name: Create PSD Options (prepare the file)
    text: '`PsdOptions` holds the configuration for the output PSD, such as compression
      level and color depth.'
  - name: Set the FileCreateSource (define where the PSD will be saved)
    text: '`FileCreateSource` tells Aspose where to write the generated file.'
  - name: Create Image Instance (initialize canvas size)
    text: The `Image` constructor creates a blank PSD canvas with the dimensions you
      specify.
  - name: Initialize Graphics and draw the first picture
    text: '`Graphics` provides drawing capabilities on the canvas. We clear the background
      to white and render the first source image on the left half.'
  - name: Draw the second picture (complete the combine)
    text: Now we place the second image on the right half of the same canvas, creating
      a second layer automatically.
  - name: Save the resulting PSD file
    text: Persist the combined canvas to disk. The resulting `combined.psd` contains
      two editable layers. Congratulations! You have successfully **combine images
      java** and generated a layered PSD file ready for further Photoshop editing.
  type: HowTo
- questions:
  - answer: Aspose.PSD natively reads and writes **15+ formats**, including PSD, PNG,
      JPEG, BMP, TIFF, GIF, and more, making it a versatile choice for image pipelines.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Each `drawImage` call creates a separate PSD layer, which you can
      later reposition, apply filters, or mask using Aspose.PSD’s extensive layer‑editing
      API.
    question: Can I perform additional edits after combining images?
  - answer: A valid license is required for production use. You can obtain one from
      the Aspose store; a free trial is available for evaluation.
    question: Do I need a commercial license for production?
  - answer: Simply repeat `graphics.drawImage(...)` with appropriate coordinates for
      each additional image. Each call adds a new layer.
    question: How do I add more than two pictures?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support, or consult the official documentation linked in the download page.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Java 合并图像 – 使用 Aspose.PSD 合并图片创建 PSD 文件
url: /zh/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 合并图像 Java – 使用 Aspose.PSD 合并图片创建 PSD 文件

## 介绍

如果您需要通过合并多张图片为单个 Photoshop 兼容文件来 **combine images java**，Aspose.PSD for Java 让整个过程变得轻而易举。在本教程中，我们将演示如何创建一个 600 × 600 像素的 PSD 画布，将两张源图片并排绘制，并将结果保存为分层 PSD 文件。完成后，您将了解为何此技术对自动化图形流水线有价值，以及如何将其扩展到任意数量的图像。

## 快速答案
- **什么库最适合将图像合并为 PSD？** Aspose.PSD for Java.
- **基本合并需要多长时间？** 大约 10‑15 分钟编写并运行代码。
- **开发是否需要许可证？** 免费试用可用于评估；生产部署需要商业许可证。
- **可以添加超过两张图片吗？** 当然——只需对每个额外图层重复 `drawImage` 调用。
- **支持哪些 Java 版本？** Java 8 及更高（最高到 Java 21）。

## 什么是 combine images java？

*Combine images java* 指使用 Java API 以编程方式将多张光栅图片合并为单个图像文件。Aspose.PSD 提供了一种高级、纯 Java 的方式来实现此功能，无需原生 Photoshop 依赖，使您能够自动化合成、保留图层，并输出可在 Photoshop 或其他支持 PSD 的工具中后期编辑的 Photoshop 兼容 PSD。

## 为什么使用 Aspose.PSD 合并图像？

Aspose.PSD 支持 **15+ 图像格式**（包括 PSD、PNG、JPEG、BMP、TIFF、GIF 等），并且能够在不将整个文件加载到内存的情况下处理 **多百页文档**，这归功于其流式架构。该库是 **100 % 受管 Java**，因此可在任何支持 JDK 的操作系统上运行，消除了原生 DLL 的麻烦。

## 前提条件

1. **Aspose.PSD Library** – 从 [here](https://releases.aspose.com/psd/java/) 下载。  
2. **Java Development Kit (JDK)** – 需要 Java 8 及以上；建议使用 Java 11 或更高版本以获得更佳性能。  
3. **Working Directory** – 您机器上的一个文件夹，包含源图片 (`example1.png`, `example2.png`) 并用于写入输出 PSD (`combined.psd`)。  
4. **License Purchase** – 在 [here](https://purchase.aspose.com/buy) 获取商业许可证，以用于生产环境。  
5. **Other Aspose Releases** – 在 [here](https://releases.aspose.com/) 探索其他产品和更新。

## 导入包

`import` 语句将必要的 Aspose.PSD 类引入作用域。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdOptions;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.PsdImageLayer;
import com.aspose.psd.imageoptions.FileCreateSource;
import com.aspose.psd.graphics.Graphics;
import com.aspose.psd.Color;
```

## 如何使用 Aspose.PSD combine images java？

加载一个空白画布，将每张图片绘制到画布上，然后将结果保存为 PSD 文件——这就是整个工作流的三个简洁步骤。API 会为每个 `drawImage` 调用自动创建一个独立的图层，使您以后在 Photoshop 中能够完全编辑。

### 步骤 1：创建 PSD 选项（准备文件）

`PsdOptions` 保存输出 PSD 的配置，例如压缩级别和颜色深度。

```java
PsdOptions psdOptions = new PsdOptions();
```

### 步骤 2：设置 FileCreateSource（定义 PSD 保存位置）

`FileCreateSource` 告诉 Aspose 将生成的文件写入何处。

```java
psdOptions.setSource(new FileCreateSource(dataDir + "combined.psd", false));
```

### 步骤 3：创建 Image 实例（初始化画布尺寸）

`Image` 构造函数会创建一个具有您指定尺寸的空白 PSD 画布。

```java
Image image = new Image(psdOptions, 600, 600);
```

### 步骤 4：初始化 Graphics 并绘制第一张图片

`Graphics` 提供在画布上的绘图功能。我们将背景清除为白色，并在左半部分渲染第一张源图片。

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(dataDir + "example1.png", new Rectangle(0, 0, 300, 600));
```

### 步骤 5：绘制第二张图片（完成合并）

现在我们将第二张图片放置在同一画布的右半部分，自动创建第二个图层。

```java
graphics.drawImage(dataDir + "example2.png", new Rectangle(300, 0, 300, 600));
```

### 步骤 6：保存生成的 PSD 文件

将合并后的画布持久化到磁盘。生成的 `combined.psd` 包含两个可编辑的图层。

```java
image.save();
```

恭喜！您已成功 **combine images java** 并生成了一个可供进一步 Photoshop 编辑的分层 PSD 文件。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| 加载源图片时 `File not found` | `dataDir` 路径不正确 | 确认 `dataDir` 指向包含 `example1.png` 和 `example2.png` 的文件夹。 |
| 输出 PSD 为空白 | `graphics.clear` 在绘制后被调用 | 在任何 `drawImage` 操作之前调用 `graphics.clear(Color.getWhite())` **before**。 |
| 运行时许可证异常 | 缺少或过期的 Aspose.PSD 许可证 | 在任何 API 调用之前使用 `License license = new License(); license.setLicense("Aspose.PSD.lic");` 应用有效许可证。 |

## 常见问答

**Q: Aspose.PSD 是否兼容所有图像格式？**  
A: Aspose.PSD 本地读取和写入 **15+ 格式**，包括 PSD、PNG、JPEG、BMP、TIFF、GIF 等，使其成为图像流水线的多功能选择。

**Q: 合并图像后我可以进行额外编辑吗？**  
A: 可以。每次 `drawImage` 调用都会创建一个独立的 PSD 图层，您随后可以使用 Aspose.PSD 丰富的图层编辑 API 重新定位、应用滤镜或遮罩。

**Q: 生产环境是否需要商业许可证？**  
A: 生产使用需要有效许可证。您可以从 Aspose 商店获取；免费试用可用于评估。

**Q: 如何添加超过两张图片？**  
A: 只需对每张额外图片使用适当坐标重复 `graphics.drawImage(...)` 调用。每次调用都会添加一个新图层。

**Q: 如果遇到问题，我可以在哪里获取帮助？**  
A: 访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34) 获取社区支持，或查阅下载页面中链接的官方文档。

---

**最后更新：** 2026-06-28  
**测试环境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [在 Aspose.PSD for Java 中通过设置路径创建图像](/psd/java/image-editing/create-image-by-setting-path/)
- [在 Aspose.PSD for Java 中使用流创建图像](/psd/java/image-editing/create-image-using-stream/)
- [在 Aspose.PSD for Java 中使用 Resize Type 枚举进行图像大小调整](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

```java
PsdOptions imageOptions = new PsdOptions();
```

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

```java
Image image = Image.create(imageOptions, 600, 600);
```

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

```java
image.save();
```