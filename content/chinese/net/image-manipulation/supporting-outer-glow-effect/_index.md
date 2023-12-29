---
title: 在 Aspose.PSD for .NET 中支持外发光效果
linktitle: 支持外发光效果
second_title: Aspose.PSD .NET API
description: 探索 Aspose.PSD for .NET 中外发光效果的强大功能。通过此分步教程提升您的图像设计。
type: docs
weight: 16
url: /zh/net/image-manipulation/supporting-outer-glow-effect/
---
## 介绍

欢迎来到我们关于在 Aspose.PSD for .NET 中支持外发光效果的分步指南。 Aspose.PSD 是一个功能强大的库，可以在 .NET 应用程序中无缝操作 PSD 文件。在本教程中，我们将探索外发光效果的实现，并提供将其集成到项目中的详细演练。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.PSD for .NET 库：从以下位置下载库：[Aspose.PSD .NET 文档](https://reference.aspose.com/psd/net/).

- 开发环境：设置您首选的 .NET 开发环境。

- 文档和输出目录：在提供的代码中定义文档和输出目录。

## 导入命名空间

在本节中，我们将导入必要的命名空间来启动我们的外发光效果实现。按着这些次序：

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

现在，让我们将提供的示例分解为多个步骤来实现外发光效果。

## 第1步：设置文档和输出路径

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## 第 2 步：加载 PSD 图像

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    //下面将添加实施步骤。
}
```

## 第三步：添加外发光效果

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## 步骤 4：配置外发光参数

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## 第 5 步：保存图像

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## 第 6 步：清理

```csharp
File.Delete(outputPng);
```

## 第7步：显示成功消息

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## 结论

恭喜！您已使用 Aspose.PSD for .NET 成功实现了外发光效果。这一强大的功能增强了图像的视觉吸引力，为您的设计提供了独特的触感。

## 常见问题解答

### Q1：Aspose.PSD 与所有.NET 框架兼容吗？

A1：是的，Aspose.PSD支持广泛的.NET框架，确保与各种开发环境的兼容性。

### Q2：在哪里可以找到 Aspose.PSD 的附加文档？

 A2：请参阅[Aspose.PSD .NET 文档](https://reference.aspose.com/psd/net/)获取全面的信息和示例。

### Q3：如何获得Aspose.PSD的临时许可证？

 A3：参观[Aspose.PSD临时许可证](https://purchase.aspose.com/temporary-license/)用于临时许可选项。

### Q4：Aspose.PSD 用户可以获得哪些支持？

 A4：加入[Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)以获得社区支持和讨论。

### Q5：我可以购买 Aspose.PSD for .NET 吗？

 A5：是的，探索许可选项并进行购买[这里](https://purchase.aspose.com/buy).