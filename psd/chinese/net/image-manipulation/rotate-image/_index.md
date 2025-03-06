---
title: 在 Aspose.PSD for .NET 中旋转图像
linktitle: 旋转图像
second_title: Aspose.PSD .NET API
description: 学习使用 Aspose.PSD 在 .NET 中轻松旋转图像。按照我们的分步教程进行操作。
weight: 15
url: /zh/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for .NET 中旋转图像

## 介绍

如果您正在使用 .NET 进行图像处理，Aspose.PSD 是您进行无缝高效图像处理的首选工具。在本教程中，我们将重点介绍一项基本任务 - 使用 Aspose.PSD for .NET 旋转图像。请继续关注，我们将该过程分解为简单、可操作的步骤。

## 先决条件

在开始之前，请确保您已满足以下先决条件：

-  Aspose.PSD for .NET Library：从以下网站下载并安装该库[Aspose.PSD .NET 文档](https://reference.aspose.com/psd/net/).

- 您的文档目录：设置存储图像的目录。将代码片段中的“您的文档目录”替换为此目录的路径。

## 导入命名空间

确保包含访问 Aspose.PSD 功能所需的命名空间。在 .NET 项目的开头添加以下几行：

```csharp
using Aspose.PSD.ImageOptions;
```

## 步骤 1：加载图像

```csharp
string sourceFile = dataDir + @"sample.psd";

//将现有图像加载到 RasterImage 类的实例中
using (Image image = Image.Load(sourceFile))
{
```

## 第 2 步：旋转图像

```csharp
    //将图像顺时针旋转 270 度
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 步骤 3：保存旋转后的图像

```csharp
    //将旋转后的图像保存为 JPEG 文件
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

就是这样！只需几行代码，您就成功使用 Aspose.PSD for .NET 旋转了图像。

## 结论

在本教程中，我们探索了使用 Aspose.PSD for .NET 旋转图像的基础知识。Aspose.PSD 提供了一套强大的图像处理工具，使其成为 .NET 开发人员必不可少的库。尝试不同的旋转并探索更多功能以增强您的图像处理工作流程。

## 常见问题解答

### 问题 1：我可以使用 Aspose.PSD 按自定义角度旋转图像吗？

是的，Aspose.PSD 允许您指定自定义旋转角度。只需替换`RotateFlipType.Rotate270FlipNone`与您想要的旋转角度一致。

### Q2：Aspose.PSD 是否兼容各种图像格式？

当然。Aspose.PSD 支持多种图像格式，包括 PSD、JPEG、PNG 等。查看[文档](https://reference.aspose.com/psd/net/)以获取完整列表。

### Q3: 如何获取 Aspose.PSD 的临时许可证？

访问[临时执照页面](https://purchase.aspose.com/temporary-license/)在 Aspose 网站上获取用于评估目的的临时许可证。

### Q4：在哪里可以找到对 Aspose.PSD 的支持？

如有任何疑问或需要帮助，请访问[Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)并与社区建立联系。

### Q5：我可以购买 Aspose.PSD 用于商业用途吗？

当然。探索[购买页面](https://purchase.aspose.com/buy)获取满足您需求的许可证。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
