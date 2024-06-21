---
title: 使用 Aspose.PSD for Java 按比例调整图像大小
linktitle: 按比例调整图像大小
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 增强您的 Java 应用程序。按照我们的指南轻松按比例调整图像大小。立即提高您的图像处理能力。
type: docs
weight: 17
url: /zh/java/advanced-image-manipulation/resize-image-proportionally/
---
## 介绍

欢迎来到我们关于使用 Aspose.PSD for Java 按比例调整图像大小的分步指南。如果您希望通过高效的图像调整功能来增强 Java 应用程序，那么您来对地方了。在本教程中，我们将使用清晰简洁的步骤引导您完成整个过程。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

1. Java 环境：确保您的系统上安装了 Java。
2.  Aspose.PSD 库：下载并安装 Aspose.PSD 库。你可以找到需要的资源[这里](https://releases.aspose.com/psd/java/).

## 导入包

整理好先决条件后，将所需的包导入到您的 Java 项目中。确保您的项目中正确引用了 Aspose.PSD 库。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## 第 1 步：加载图像

首先将要调整大小的图像加载到 Java 应用程序中。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## 第 2 步：指定宽度和高度

确定调整后的图像的新宽度和高度。在此示例中，我们将图像大小调整为其原始尺寸的一半。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## 第 3 步：保存调整大小的图像

将调整大小的图像保存到所需位置，并指定格式选项（在本例中为 PNG）。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

现在你就得到了它！您已成功使用 Aspose.PSD for Java 按比例调整图像大小。

## 结论

在本教程中，我们介绍了使用 Java 的 Aspose.PSD 库按比例调整图像大小的基本步骤。现在，您可以轻松地将此功能集成到您的 Java 应用程序中，以改进图像处理。

## 常见问题解答

### Q1：Aspose.PSD 是否兼容所有图像格式？

 A1：Aspose.PSD支持多种图像格式，包括PSD、PNG、JPEG等。检查[文档](https://reference.aspose.com/psd/java/)以获得完整的列表。

### Q2：我可以将Aspose.PSD用于商业项目吗？

 A2: 是的，可以。参观[购买页面](https://purchase.aspose.com/buy)了解许可详细信息。

### Q3：临时许可证是否可用于测试目的？

 A3：是的，您可以获得临时许可证。[这里](https://purchase.aspose.com/temporary-license/)进行评估。

### Q4：哪里可以找到对 Aspose.PSD 的支持？

 A4：访问[Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)以获得社区的支持和帮助。

### Q5：如何访问Aspose.PSD文档？

 A5：参考详细文档[这里](https://reference.aspose.com/psd/java/).
`