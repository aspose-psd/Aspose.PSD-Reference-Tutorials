---
title: 在 Java 中从 PSD 中提取缩略图
linktitle: 在 Java 中从 PSD 中提取缩略图
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 从 PSD 文件中提取缩略图。本分步指南涵盖了从设置到保存提取的图像的所有内容。
type: docs
weight: 15
url: /zh/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## 介绍
在本教程中，我们将探讨如何使用 Aspose.PSD for Java 从 PSD 文件中提取缩略图。缩略图对于快速预览或创建嵌入 PSD 文档中的图像的较小版本非常有用。让我们深入了解使用 Aspose.PSD 实现此目的所需的步骤。
## 先决条件
在开始之前，请确保您已进行以下设置：
- 您的系统上安装了 Java 开发工具包 (JDK)。
-  Java 库的 Aspose.PSD。您可以从以下位置下载：[这里](https://releases.aspose.com/psd/java/).
- Java 编程的基础知识。
## 导入包
首先，在您的 Java 类中包含必要的 Aspose.PSD 包：
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## 第 1 步：加载 PSD 文件
首先，加载包含要提取的缩略图的 PSD 文件。
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
代替`"Your_Document_Directory/"`与 PSD 文件所在的目录路径，以及`"your_file.psd"`与您的 PSD 文件的名称。
## 第 2 步：迭代图像资源
迭代图像资源以查找缩略图资源。
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        //提取缩略图数据
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        //使用提取的缩略图数据创建新图像
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        //将提取的缩略图另存为单独的 JPEG 文件
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        //输出成功信息
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; //找到并处理缩略图后退出循环
    }
}
```
## 第 3 步：保存提取的缩略图
将提取的缩略图另存为单独的图像文件（在本例中为 JPEG 文件）。
## 步骤 4：处理不同的缩略图类型
如果您的 PSD 文件可能包含多种类型的缩略图，例如`Thumbnail4Resource`，您可以扩展逻辑以类似地处理这些情况。

## 结论
在本教程中，我们探讨了如何使用 Aspose.PSD for Java 从 PSD 文件中提取缩略图。通过执行上述步骤，您可以有效地检索和保存 PSD 文档中嵌入的缩略图。

## 常见问题解答
### 什么是 Aspose.PSD？
Aspose.PSD 是一个 Java 库，允许开发人员以编程方式使用 PSD 和其他图像文件格式。
### 在哪里可以找到有关 Aspose.PSD for Java 的更多文档？
您可以参考[文档](https://reference.aspose.com/psd/java/)获取详细的 API 参考和示例。
### 我可以在购买前免费试用 Aspose.PSD 吗？
是的，您可以下载一个[免费试用](https://releases.aspose.com/)评估图书馆的能力。
### 我如何获得 Aspose.PSD 的临时许可证？
临时许可证可以从[这里](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD适合商业用途吗？
是的，根据其许可条款，Aspose.PSD 可用于个人和商业项目。