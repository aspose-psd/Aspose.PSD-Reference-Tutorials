---
title: 在 Aspose.PSD for .NET 中按比例调整图像大小
linktitle: 按比例调整图像大小
second_title: Aspose.PSD .NET API
description: 探索使用 Aspose.PSD for .NET 进行无缝图像调整。下载库，按照我们的教程，并增强您的图像处理能力。
type: docs
weight: 14
url: /zh/net/image-manipulation/resize-images-proportionally/
---
在图像处理领域，Aspose.PSD for .NET 是一款功能强大的工具包，它为开发人员提供了轻松按比例调整图像大小的功能。在本分步指南中，我们将引导您完成使用 Aspose.PSD for .NET 调整图像大小的过程，确保您的图像完美地保持其比例。

## 介绍

按比例调整图像大小是许多应用程序中的常见任务，而 Aspose.PSD for .NET 为开发人员简化了此过程。无论您是在开发 Web 应用程序、桌面软件还是移动应用程序，了解如何在保留图像纵横比的同时调整图像大小对于保持视觉吸引力和一致性至关重要。

## 先决条件

在深入研究使用 Aspose.PSD for .NET 进行调整大小的神奇功能之前，请确保您已满足以下先决条件：

1.  Aspose.PSD for .NET 库：确保已安装 Aspose.PSD for .NET 库。您可以从[Aspose.PSD for .NET 发布](https://releases.aspose.com/psd/net/)页。

2. 文档目录：创建一个目录来存储您的文档，并将提供的代码中的“您的文档目录”替换为该目录的实际路径。

现在您已经设置了先决条件，让我们进入分步指南。

## 导入命名空间

```csharp
using Aspose.PSD.ImageOptions;
```

导入必要的命名空间以访问所需的类和方法。

## 步骤 1：加载图像

```csharp
//文档目录的路径。
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

//将现有图像加载到 RasterImage 类的实例中
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	//其余步骤请点击此处
}
```

使用加载源图像`Image.Load`方法。

## 步骤 2：指定宽度和高度

```csharp
//指定宽度和高度
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

确定调整大小后图像的新宽度和高度。在此示例中，宽度和高度减半，但您可以根据需要调整这些值。

## 步骤 3：保存调整大小后的图像

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

使用保存调整大小的图像`Save`方法并指定选项。在本例中，我们将其保存为 PNG 文件。

## 结论

在 Aspose.PSD for .NET 中按比例调整图像大小是一个简单的过程，可为您的图像处理工作流程增添价值。本指南为您提供了将此功能无缝集成到您的应用程序中的知识。

## 常见问题解答

### 问题 1：我可以将图像调整为特定尺寸吗？

A1：是的，您可以在代码中根据您的要求自定义新的宽度和高度。

### Q2：Aspose.PSD for .NET 适合批量调整图像大小吗？

A2：当然可以！您可以将这些步骤合并到循环中，以批量处理多幅图像。

### Q3: Aspose.PSD for .NET 中还有其他图像处理功能吗？

A3：是的，Aspose.PSD for .NET 提供了广泛的功能，包括裁剪、旋转和对图像应用过滤器。

### 问题4：Aspose.PSD for .NET 有免费试用版吗？

 A4：是的，您可以通过免费试用探索 Aspose.PSD for .NET 的功能。访问[这里](https://releases.aspose.com/)开始吧。

### Q5：在哪里可以找到对 Aspose.PSD for .NET 的支持？

 A5：访问[Aspose.PSD for .NET 论坛](https://forum.aspose.com/c/psd/34)获得社区支持和讨论。