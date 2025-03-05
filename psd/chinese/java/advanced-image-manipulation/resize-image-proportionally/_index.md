---
title: 使用 Aspose.PSD for Java 按比例调整图像大小
linktitle: 按比例调整图像大小
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 增强您的 Java 应用程序。按照我们的指南，轻松按比例调整图像大小。立即提升您的图像处理能力。
type: docs
weight: 17
url: /zh/java/advanced-image-manipulation/resize-image-proportionally/
---
## 介绍

欢迎阅读我们关于使用 Aspose.PSD for Java 按比例调整图像大小的分步指南。如果您希望通过高效的图像调整功能增强 Java 应用程序，那么您来对地方了。在本教程中，我们将使用清晰简洁的步骤引导您完成整个过程。

## 先决条件

在深入学习本教程之前，请确保您已满足以下先决条件：

1. Java 环境：确保您的系统上安装了 Java。
2.  Aspose.PSD 库：下载并安装 Aspose.PSD 库。您可以找到必要的资源[这里](https://releases.aspose.com/psd/java/).

## 导入包

整理好先决条件后，将所需的包导入 Java 项目。确保项目中正确引用了 Aspose.PSD 库。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## 步骤 1：加载图像

首先将要调整大小的图像加载到 Java 应用程序中。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## 步骤 2：指定宽度和高度

确定调整后图像的新宽度和高度。在此示例中，我们将图像大小调整为原始尺寸的一半。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## 步骤 3：保存调整大小后的图像

将调整大小的图像保存到所需位置，并指定格式选项（在本例中为 PNG）。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

就这样！您已成功使用 Aspose.PSD for Java 按比例调整了图像大小。

## 结论

在本教程中，我们介绍了使用 Java 版 Aspose.PSD 库按比例调整图像大小的基本步骤。现在，您可以毫不费力地将此功能集成到 Java 应用程序中，以改进图像处理。

## 常见问题解答

### 问题1：Aspose.PSD 是否兼容所有图像格式？

 A1：Aspose.PSD 支持多种图像格式，包括 PSD、PNG、JPEG 等。请查看[文档](https://reference.aspose.com/psd/java/)以获取完整列表。

### 问题2：我可以将Aspose.PSD用于商业项目吗？

 A2：可以。请访问[购买页面](https://purchase.aspose.com/buy)了解许可详情。

### 问题 3： 临时许可证可用于测试目的吗？

 A3：是的，您可以获得临时驾照[这里](https://purchase.aspose.com/temporary-license/)进行评估。

### Q4：在哪里可以找到对 Aspose.PSD 的支持？

 A4：参观[Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)寻求社区的支持和援助。

### Q5: 如何访问 Aspose.PSD 文档？

 A5: 请参阅详细文档[这里](https://reference.aspose.com/psd/java/).
`