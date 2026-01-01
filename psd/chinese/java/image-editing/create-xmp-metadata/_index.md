---
date: 2026-01-01
description: 学习如何创建 XMP 元数据、将 XMP 添加到 PSD 文件以及使用 Aspose.PSD for Java 更新图像元数据。立即跟随本分步指南。
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 创建 XMP 元数据
url: /zh/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 创建 XMP 元数据

## 介绍

管理图像元数据是处理 Photoshop（PSD）文件的 Java 开发者的常见需求。在本教程中，你将学习 **如何使用 Aspose.PSD 库创建 XMP 元数据**，将 XMP 添加到 PSD 图像，并以编程方式更新图像元数据。我们将逐步演示每一步，解释每个环节的重要性，并提供可在实际项目中应用的实用技巧。

## 快速答案
- **什么是 XMP 元数据？** 一种标准化的格式，用于在图像文件内部嵌入描述性信息（作者、关键字等）。  
- **为什么使用 Aspose.PSD？** 它提供了纯 Java API，可在无需 Photoshop 的情况下创建、读取和编辑 PSD 文件。  
- **我可以向已有的 PSD 添加 XMP 吗？** 可以——使用 `setXmpData` 可以即时更新图像元数据。  
- **主要步骤是什么？** 设置图像尺寸、创建 header/trailer、构建 XMP 包、附加它们并保存。  
- **需要许可证吗？** 免费试用可用于开发；生产环境需要商业许可证。

## 在 Java 中“创建 XMP 元数据”是什么？

创建 XMP 元数据指的是构建一个 XMP 包（包括 header、body、trailer），该包描述图像信息，然后将该包嵌入到 PSD 文件中。Aspose.PSD 库抽象了底层细节，让你专注于想要存储的内容。

## 为什么要向 PSD 文件添加 XMP？

- **可搜索性：** 基于作者、标题或自定义标签实现强大的资产管理搜索。  
- **互操作性：** XMP 被 Adobe 产品、Lightroom 以及众多 DAM 系统识别。  
- **版本控制：** 将处理历史（例如城市、颜色模式）直接存储在文件内部。

## 前置条件

- **Java 开发环境：** 已安装 JDK 8 或更高版本，并具备基本的 Java 知识。  
- **Aspose.PSD 库：** 下载并设置 Aspose.PSD for Java 库。你可以在[此处](https://reference.aspose.com/psd/java/)找到库及详细文档。  
- **文档目录：** 确定在系统上读取/写入 PSD 文件的路径。

## 导入包

在你的 Java 项目中，导入使用 Aspose.PSD 功能所需的包：

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## 步骤 1：指定图像尺寸

首先，为新 PSD 图像定义画布尺寸。

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## 步骤 2：创建新图像

创建一个空白 PSD 图像，稍后我们将在其上添加 XMP 元数据。

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## 步骤 3：创建 XMP Header

Header 包含打开的 XML 处理指令和用于标识文档的 GUID。

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## 步骤 4：创建 XMP Trailer

Trailer 标记 XMP 包的结束。将 `true` 标志设为 true 可写入关闭的处理指令。

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 步骤 5：创建 XMP 元数据

向核心 XMP 元数据对象添加通用属性，如作者和描述。

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## 步骤 6：创建 XMP 包包装器

将 header、trailer 和核心元数据包装成一个可附加到图像的单一包。

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## 步骤 7：设置 Photoshop 属性

填充许多 Adobe 工具期望的 Photoshop 特定字段（城市、国家、颜色模式）。

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## 步骤 8：将 Photoshop 包添加到 XMP 元数据

将 Photoshop 包附加到 XMP 包中。

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## 步骤 9：设置 DublinCore 属性

添加 Dublin Core 元数据，如作者、标题以及自定义的 movie 标签。

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## 步骤 10：将 DublinCore 包添加到 XMP 元数据

将 Dublin Core 包与已有的 XMP 包合并。

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## 步骤 11：将 XMP 元数据更新到图像中

现在将完整的 XMP 包嵌入到 PSD 图像中。

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## 步骤 12：保存图像

最后，将 PSD 文件写入磁盘（或内存流），以确保元数据被持久化。

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## 常见问题及解决方案

| 问题 | 发生原因 | 解决方案 |
|------|----------|----------|
| **`NullPointerException` 在 `setXmpData` 上** | XMP 包未完整构建（缺少 header/trailer）。 | 确保在调用 `setXmpData` 前创建 `XmpHeaderPi`、`XmpTrailerPi`，并添加所有包。 |
| **Photoshop 中看不到元数据** | Photoshop 期望 XMP 包被正确包装。 | 验证使用了 `XmpTrailerPi(true)`，并且在保存图像时包含了该包。 |
| **文件路径错误** | 使用相对路径且权限不足。 | 使用绝对路径或确保应用对目标文件夹具有写入权限。 |

## 常见问答

**问：Aspose.PSD 是否兼容不同的图像格式？**  
答：是的，Aspose.PSD 支持 PSD、PSB、BMP、GIF、JPEG、PNG、TIFF 等多种格式，提供跨格式的灵活性。

**问：我可以使用 Aspose.PSD 操作已有的元数据吗？**  
答：完全可以。你可以加载已有的 PSD，使用 `getXmpData()` 获取其 XMP 数据，修改包后再保存回去。

**问：Aspose.PSD 对图像尺寸有何限制？**  
答：Aspose.PSD 设计用于处理大图像（最高可达数千兆像素），唯一限制是可用内存。

**问：是否提供 Aspose.PSD 的试用版？**  
答：提供，你可以在[此处](https://releases.aspose.com/)获取免费试用。

**问：在哪里可以获得 Aspose.PSD 相关的支持？**  
答：如需帮助或提问，请访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34)。

## 结论

现在，你已经掌握了 **如何创建 XMP 元数据**、将 XMP 添加到 PSD，以及使用 Aspose.PSD for Java 更新图像元数据的完整流程。这些步骤让你能够完全控制嵌入图像的描述信息，使其可搜索、可管理，并为后续工作流做好准备。欢迎尝试更多 XMP 架构或将此代码集成到更大的图像处理流水线中。

---

**最后更新：** 2026-01-01  
**测试环境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}