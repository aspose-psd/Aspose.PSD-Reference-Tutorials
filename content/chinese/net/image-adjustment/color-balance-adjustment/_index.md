---
title: 在 Aspose.PSD for .NET 中应用色彩平衡调整
linktitle: 应用色彩平衡调整
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 的色彩平衡调整功能轻松增强 PSD 图像颜色。按照我们的分步指南获得令人惊叹的结果。
type: docs
weight: 14
url: /zh/net/image-adjustment/color-balance-adjustment/
---
## 介绍

欢迎阅读这份关于在 Aspose.PSD for .NET 中应用色彩平衡调整的综合指南！ Aspose.PSD 是一个功能强大的 .NET 库，允许开发人员高效地处理 PSD 文件。在本教程中，我们将重点介绍色彩平衡调整功能，使您能够轻松增强 PSD 图像的色彩平衡。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.PSD for .NET Library：从以下位置下载并安装该库：[Aspose.PSD 网站](https://releases.aspose.com/psd/net/).
- 开发环境：确保您的计算机上设置了有效的 .NET 开发环境。
- PSD 文件：准备好要应用色彩平衡调整的 PSD 文件。

## 导入命名空间

在您的 .NET 项目中，包含使用 Aspose.PSD 功能所需的命名空间。将以下行添加到您的代码中：

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

现在，让我们将色彩平衡调整过程分解为多个步骤：

## 第 1 步：加载 PSD 文件

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    //色彩平衡调整的代码将在以下步骤中添加。
}
```

## 第 2 步：访问并调整色彩平衡

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## 第三步：保存调整后的图像

```csharp
im.Save(outputPath);
```

现在，您已经使用 Aspose.PSD for .NET 成功将色彩平衡调整应用到您的 PSD 文件！

## 结论

恭喜！您已经了解了如何使用 Aspose.PSD for .NET 增强 PSD 图像的色彩平衡。尝试不同的平衡值以达到所需的视觉效果。

## 常见问题解答

### Q1：我可以对多个图层应用色彩平衡调整吗？

A1：是的，您可以迭代 PSD 文件中的所有图层并根据需要调整色彩平衡。

### Q2：Aspose.PSD for .NET适合批量处理PSD文件吗？

A2：当然！ Aspose.PSD为PSD文件提供高效的批处理功能。

### Q3：如何获得 Aspose.PSD for .NET 的临时许可证？

 A3：参观[Aspose.PSD临时许可证](https://purchase.aspose.com/temporary-license/)以获得临时许可证。

### Q4：在哪里可以找到更多示例和文档？

 A4：探索[Aspose.PSD 文档](https://reference.aspose.com/psd/net/)获取详细示例和指南。

### 问题 5：Aspose.PSD for .NET 有哪些支持选项？

 A5：访问[Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)以获得社区支持和讨论。
