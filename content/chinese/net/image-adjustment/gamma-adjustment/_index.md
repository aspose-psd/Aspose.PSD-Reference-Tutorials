---
title: 在 Aspose.PSD for .NET 中实现伽玛调整
linktitle: 实施伽玛调整
second_title: Aspose.PSD .NET API
description: 通过我们关于实施伽玛调整的分步指南来探索 Aspose.PSD for .NET 的强大功能。轻松微调图像亮度和对比度。
type: docs
weight: 12
url: /zh/net/image-adjustment/gamma-adjustment/
---
## 介绍

欢迎阅读这份关于在 Aspose.PSD for .NET 中实现 Gamma 调整的综合指南！伽玛调整是一项重要的图像处理技术，可让您微调图像的亮度和对比度。在本教程中，我们将引导您使用强大的 .NET Aspose.PSD 库完成整个过程。

## 先决条件

在深入实施之前，请确保满足以下先决条件：

-  Aspose.PSD for .NET 库：确保您已安装 Aspose.PSD for .NET 库。你可以下载它[这里](https://releases.aspose.com/psd/net/).

- .NET Framework：本教程假设您对 .NET 开发有基本的了解并且已安装 .NET Framework。

- 集成开发环境 (IDE)：选择用于 .NET 开发的首选 IDE，例如 Visual Studio。

## 导入命名空间

在您的 .NET 项目中，首先导入使用 Aspose.PSD 所需的命名空间：

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 第 1 步：设置您的项目

在您选择的 IDE 中创建一个新的 .NET 项目。确保添加对 Aspose.PSD 库的引用。

## 第 2 步：定义文档目录

```csharp
string dataDir = "Your Document Directory";
```

## 第 3 步：加载图像

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    //附加步骤将在此 using 块内执行。
}
```

## 第 4 步：转换为 RasterImage 并缓存数据

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## 第5步：调整伽玛值

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## 第 6 步：创建 TiffOptions 并保存

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## 结论

恭喜！您已使用 Aspose.PSD for .NET 成功实现了伽玛调整。这个强大的库提供了强大的图像处理功能，使其成为 .NET 开发人员的宝贵工具。

## 常见问题解答

### Q1：哪里可以找到Aspose.PSD文档？

 A1：可以参考文档[这里](https://reference.aspose.com/psd/net/).

### Q2：如何下载 Aspose.PSD for .NET？

 A2：您可以下载该库。[这里](https://releases.aspose.com/psd/net/).

### Q3：有免费试用吗？

 A3: 是的，您可以获得免费试用。[这里](https://releases.aspose.com/).

### Q4：我在哪里可以获得 Aspose.PSD 的支持？

 A4：您可以访问支持论坛。[这里](https://forum.aspose.com/c/psd/34).

### Q5: 我需要临时许可证吗？

 A5：如果需要，您可以获得临时许可证。[这里](https://purchase.aspose.com/temporary-license/).