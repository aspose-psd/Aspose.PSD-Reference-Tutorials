---
title: 使用 Aspose.PSD for Java 调整图像的 Gamma
linktitle: 调整图像的伽玛值
second_title: Aspose.PSD Java API
description: 学习使用 Aspose.PSD for Java 轻松调整图像伽玛。请遵循我们的分步指南以获得最佳结果。
type: docs
weight: 23
url: /zh/java/advanced-techniques/adjust-gamma/
---
## 介绍

在图像处理领域，调整图像的伽玛是增强其视觉吸引力的关键步骤。 Aspose.PSD for Java 为 Java 开发人员提供了一个强大的解决方案，可以轻松地操纵图像伽玛。在本教程中，我们将探索如何使用 Aspose.PSD 调整伽玛，分解每个步骤以确保无缝实施。

## 先决条件

在深入学习本教程之前，请确保您已设置以下先决条件：

1. Java 开发环境：确保您的系统上安装了 Java 开发环境。
2.  Aspose.PSD 库：下载 Aspose.PSD 库并将其集成到您的 Java 项目中。您可以在以下位置找到必要的资源[文档](https://reference.aspose.com/psd/java/).
3. 示例图像：准备用于应用伽马调整的示例 PSD 图像。

## 导入包

要开始该过程，请在 Java 项目中导入所需的包。这为无缝利用 Aspose.PSD 功能奠定了基础。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 第 1 步：加载图像

首先将示例 PSD 图像加载到`RasterImage`班级。这是后续gamma调整的基础。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//将现有图像加载到 RasterImage 类的实例中
Image image = Image.load(sourceFile);

//将 Image 对象转换为 RasterImage
RasterImage rasterImage = (RasterImage)image;

//检查 RasterImage 是否已缓存以获得更好的性能
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## 第 2 步：调整伽玛值

现在，使用以下命令调整加载图像的伽玛值：`adjustGamma`方法。根据您的要求微调伽玛值。

```java
//调整伽玛值
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 第 3 步：创建 TiffOptions

创建一个实例`TiffOptions`对于结果图像。设置各种属性，例如每个样本的位数和光度选项，以根据您的规格定制输出。

```java
//为生成的图像创建 TiffOptions 实例
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 第 4 步：保存结果图像

使用之前定义的将处理后的图像保存为 TIFF 格式`TiffOptions`.

```java
//将生成的图像保存为 TIFF 格式
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 结论

恭喜！您已使用 Aspose.PSD for Java 成功调整了图像的伽玛值。此过程使开发人员能够轻松提高图像质量，从而打造具有视觉吸引力的用户体验。

## 常见问题解答

### Q1：哪里可以找到Aspose.PSD文档？

 A1：您可以访问文档：[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: 如何下载 Aspose.PSD for Java？

 A2：从以下位置下载库[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3：哪里可以购买Aspose.PSD？

 A3：参观[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy)购买Aspose.PSD。

### Q4：有免费试用吗？

 A4：是的，您可以在以下位置探索免费试用：[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5：我在哪里可以寻求Aspose.PSD的支持？

 A5：如需支持，请访问 Aspose.PSD 论坛：[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).