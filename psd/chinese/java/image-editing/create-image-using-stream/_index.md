---
date: 2026-01-01
description: 学习如何在 Aspose.PSD 中使用流创建 Java 位图，保存 Java 图像文件，并高效设置每像素位数。
linktitle: Create Image using Stream
second_title: Aspose.PSD Java API
title: 使用流在 Aspose.PSD 中创建 Java 位图
url: /zh/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 中的 Stream 创建 bitmap java

## 介绍

如果您需要 **创建 bitmap java** 图像，Aspose.PSD for Java 提供了一种干净、基于流的方式，既快速又节省内存。在本教程中，我们将演示如何从流生成位图图像、配置每像素位数，最后 **save image file java** 到磁盘。完成后，您将了解为何此方法非常适合服务器端图像处理、批处理作业或任何需要避免临时文件的场景。

## 快速答案
- **“create bitmap java” 是什么意思？** 指使用 Java 代码以编程方式生成 BMP 图像。  
- **哪个库处理流？** Aspose.PSD 的 `StreamSource` 和 `FileCreateSource` 类。  
- **可以设置颜色深度吗？** 可以 – 使用 `BmpOptions.setBitsPerPixel(int)`（例如 24 bpp）。  
- **如何保存结果？** 调用 `image.save(outputPath)` 即可 **save image file java**。  
- **生产环境需要许可证吗？** 商业使用需要有效的 Aspose.PSD 许可证。

## 创建 bitmap java 的前置条件

在开始之前，请确保您拥有：

- **Java Development Kit (JDK)** – 任意近期版本（8 或更高）。  
- **Aspose.PSD for Java** – 从 [documentation](https://reference.aspose.com/psd/java/) 下载最新 JAR。  
- **IDE** – Eclipse、IntelliJ IDEA 或您喜欢的任何 Java 兼容编辑器。

## 导入用于位图生成的包

首先导入所需的命名空间。这些命名空间为您提供图像创建、BMP 选项和流处理的访问权限。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## 步骤 1：设置文档目录

```java
String dataDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为您存放源文件和输出文件的绝对路径。

## 步骤 2：定义输出文件名

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

此路径即 **save image file java** 操作将写入位图的目标位置。

## 步骤 3：配置 BmpOptions（设置每像素位数）

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

这里我们 **set bits per pixel** 为 24 bpp，生成真彩位图。如需其他颜色深度，可调整该值。

## 步骤 4：创建 FileCreateSource（流源）

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

`FileCreateSource` 将文件流包装起来，使 Aspose.PSD 能直接写入目标而无需中间缓冲区。

## 步骤 5：生成位图图像

```java
Image image = Image.create(imageOptions, 500, 500);
```

此行代码 **generates a bitmap java** 图像，尺寸为 500 × 500 像素，使用前面定义的选项。

## 步骤 6：执行图像处理并保存

```java
// Perform desired image processing operations here
// For example, you could draw shapes, apply filters, etc.

// Save the processed bitmap to disk
image.save(desName);
```

在完成任何可选的操作后，调用 `image.save` 即 **saves the image file java** 到 `desName` 指定的位置。

## 结论

您现在已经学习了如何使用 Aspose.PSD 中的流 **create bitmap java** 图像，使用 **set bits per pixel** 控制颜色深度，并高效地 **save image file java**。可以尝试不同的尺寸、像素格式或额外的处理步骤，以满足项目需求。

## 常见问题

### Q1: 我可以将 Aspose.PSD 与其他 Java 库一起使用吗？

A1: 可以，Aspose.PSD 设计为能够无缝集成其他 Java 库，为您的项目提供灵活性。

### Q2: 在哪里可以找到 Aspose.PSD 相关的支持？

A2: 请访问 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 获取社区支持和讨论。

### Q3: Aspose.PSD 是否提供免费试用？

A3: 是的，您可以在 [here](https://releases.aspose.com/) 获取免费试用。

### Q4: 如何获取 Aspose.PSD 的临时许可证？

A4: 请在 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

### Q5: Aspose.PSD 的系统要求是什么？

A5: 请参阅 [documentation](https://reference.aspose.com/psd/java/) 了解详细的系统要求。

---

**最后更新：** 2026-01-01  
**测试环境：** Aspose.PSD Java 最新发布版  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}