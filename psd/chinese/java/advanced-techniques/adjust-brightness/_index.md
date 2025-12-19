---
date: 2025-12-19
description: 了解如何使用 Aspose.PSD for Java 调整图像的亮度。本 Java 图像处理教程提供了逐步指南。
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 调整图像的亮度
url: /zh/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 调整图像亮度

## 介绍

如果你需要 **学习如何在 Java 代码中直接调整图片的亮度**，这里就是你的正确入口。亮度调节是平面设计师、摄影师以及所有构建图像处理流水线的人员经常面对的任务。在本 **java 图像处理教程** 中，我们将完整演示工作流——加载 PSD/TIFF、应用亮度偏移并保存结果——使用 Aspose.PSD for Java 库。

## 快速回答
- **哪个库负责亮度调节？** Aspose.PSD for Java  
- **哪个方法修改亮度？** `RasterImage.adjustBrightness()`  
- **可以处理 PSD 和 TIFF 文件吗？** 可以，API 同时支持这两种格式。  
- **生产环境需要许可证吗？** 商业许可证是非评估使用的必需品。  
- **实现大概需要多长时间？** 基本调节通常在 10 分钟以内完成。

## 什么是图像亮度调节？

图像亮度调节会改变图像中每个像素的整体明度。提升亮度会使暗部变亮，降低亮度则会让整幅图变暗。此操作常用于纠正曝光不足的照片、为打印准备素材，或在应用程序中创建视觉效果。

## 为什么选择 Aspose.PSD for Java？

- **完整格式支持** – PSD、TIFF、JPEG、PNG 等。  
- **无外部本地依赖** – 纯 Java，实现轻松集成。  
- **高性能缓存** – 光栅数据可缓存，加速重复操作。  
- **丰富 API** – 包含颜色校正、图层、蒙版及其他高级编辑方法。

## 前置条件

在开始教程之前，请确保具备以下前置条件：

- Aspose.PSD for Java 库：从 [Aspose.PSD for Java 文档](https://reference.aspose.com/psd/java/) 下载并安装该库。

## 导入包

首先，将所需的包导入到你的 Java 项目中。本示例使用以下代码：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

现在，让我们把图像亮度调节的过程拆解为几个简单步骤：

## 使用 Aspose.PSD 调节亮度的步骤

### 步骤 1：加载图像

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

在此步骤中，我们加载目标图像并将其强制转换为 `RasterImage` 以便后续处理。

### 步骤 2：调节亮度

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

这里使用 `adjustBrightness` 方法修改图像的亮度。示例中将亮度降低了 50 个单位，你可以根据需求自行调整该数值。

### 步骤 3：设置 TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

为保存调节后的图像配置 `TiffOptions`。根据具体需求调整 `bitsPerSample` 和 `photometric` 属性。

### 步骤 4：保存结果图像

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

最后，使用指定的 `TiffOptions` 将修改后的图像保存到磁盘。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| **`ClassCastException` 在强制转换 Image 时出现** | 文件不是光栅图像（例如矢量 PSD）。 | 检查源文件格式，或在强制转换前使用 `image instanceof RasterImage` 进行判断。 |
| **亮度变化没有效果** | 调整前未对图像进行缓存。 | 如步骤 1 所示，调用 `rasterImage.cacheData()`。 |
| **保存的文件出现损坏** | `TiffOptions` 配置不正确。 | 确认 `bitsPerSample` 与源图像深度匹配（通常为每通道 8 位）。 |

## 常见问答

### Q1：我可以在除 PSD 之外的其他图像格式中调节亮度吗？

A1：可以，Aspose.PSD for Java 支持 JPEG、PNG、TIFF 等多种图像格式。

### Q2：在图像调节过程中如何处理错误？

A2：可以使用 try‑catch 块捕获并处理可能抛出的异常。

### Q3：亮度调节的范围有没有限制？

A3：调节范围取决于图像内容和格式，但 Aspose.PSD 提供了灵活的自定义空间。

### Q4：我可以在商业项目中使用 Aspose.PSD for Java 吗？

A4：可以，Aspose.PSD for Java 是商业库，可通过 [here](https://purchase.aspose.com/buy) 获取许可证。

### Q5：Aspose.PSD for Java 有免费试用吗？

A5：有，你可以从 [here](https://releases.aspose.com/) 获取免费试用版。

### Q6：`adjustBrightness` 方法会影响图层可见性吗？

A6：该方法作用于光栅化的合成图像，图层的可见性在光栅化时会被考虑。

### Q7：我可以将多个调节（如对比度、饱和度）链式调用吗？

A7：完全可以。在调节亮度后，你可以对同一 `RasterImage` 实例调用 `adjustContrast`、`adjustSaturation` 等方法。

---

**最后更新：** 2025-12-19  
**测试环境：** Aspose.PSD for Java 24.12（撰写时最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}