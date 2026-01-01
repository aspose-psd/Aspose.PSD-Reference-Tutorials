---
date: 2026-01-01
description: 学习如何使用 Aspose.PSD 在 Java 中创建 PSD 图像。本指南展示了如何设置路径以及使用 Java 创建 Photoshop
  文档的逐步代码。
linktitle: Create Image by Setting Path
second_title: Aspose.PSD Java API
title: 如何创建 PSD – 在 Aspose.PSD for Java 中通过设置路径创建图像
url: /zh/java/image-editing/create-image-by-setting-path/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何创建 PSD – 通过在 Aspose.PSD for Java 中设置路径创建图像

## 介绍

欢迎阅读本分步教程，了解 **如何创建 PSD** 图像，使用 Aspose.PSD for Java。我们将逐步演示如何设置文件路径、配置选项并以编程方式生成 Photoshop 文档。完成后，您将掌握 **java create photoshop document** 文件的创建方法，可进一步编辑或集成到您的应用程序中。

## 快速回答
- **Aspose.PSD 的作用是什么？** 它提供了纯 Java API，能够读取、编辑和创建 Photoshop（PSD）文件，无需安装 Photoshop。  
- **我可以自定义输出路径吗？** 可以 – 使用 `FileCreateSource` 指定确切的位置和文件名。  
- **支持哪些压缩方式？** RLE、ZIP 和 RAW；本示例使用 RLE 进行无损压缩。  
- **开发阶段需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。  
- **支持哪些 Java 版本？** Aspose.PSD 兼容 Java 8 及更高版本。

## 什么是“如何创建 PSD”？

创建 PSD 文件即生成兼容 Photoshop 的图像，保留图层、通道以及其他 Photoshop 特有的数据。Aspose.PSD 抽象了复杂的文件格式，让您专注于业务逻辑。

## 为什么使用 Java 来 **java create photoshop document**？

- **跨平台** – Java 可在任何环境运行，您的 PSD 生成可在 Windows、Linux 或 macOS 上工作。  
- **无需 Photoshop** – 无需安装 Adobe Photoshop，即可生成或修改 PSD 文件。  
- **完全控制** – 通过简洁的对象模型设置压缩、颜色模式、尺寸等。

## 前置条件

在开始之前，请确保您具备：

- 基本的 Java 编程知识。  
- 已安装 Aspose.PSD for Java 库。您可以在 [此处](https://releases.aspose.com/psd/java/) 下载。

## 导入包

在 Java 项目中导入必要的包：

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## 第一步：如何为文档目录设置路径

设置文档目录的路径，以便在该位置创建图像。

```java
String dataDir = "Your Document Directory";
```

## 第二步：定义输出文件名

定义输出文件名，包括文档目录。

```java
String desName = dataDir + "CreatingAnImageBySettingPath_out.psd";
```

## 第三步：配置 PsdOptions

创建 `PsdOptions` 实例并配置其属性，例如压缩方式。

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setCompressionMethod(CompressionMethod.RLE);
```

## 第四步：设置 Source 属性

为 `PsdOptions` 实例定义 source 属性，指定输出文件以及是否为临时文件。

```java
psdOptions.setSource(new FileCreateSource(desName, false));
```

## 第五步：创建 Image

创建 `Image` 实例，并通过传入 `PsdOptions` 对象和图像尺寸调用 `create` 方法。

```java
Image image = Image.create(psdOptions, 500, 500);
```

## 第六步：保存图像

保存创建好的图像。

```java
image.save();
```

重复这些步骤，您就成功地通过设置路径使用 Aspose.PSD for Java 创建了图像。

## 常见问题与技巧

- **目录无效** – 确保 `dataDir` 以正确的文件分隔符（`/` 或 `\\`）结尾。  
- **权限错误** – 以对目标文件夹具有写入权限的方式运行应用程序。  
- **未设置许可证** – 如果收到许可证异常，请在创建图像前加载 Aspose.PSD 许可证。

## 结论

本教程介绍了使用 Aspose.PSD for Java **如何创建 PSD** 文件，演示了 **如何设置路径**，并展示了生成 Photoshop 文档的完整流程。此方法使 Java 开发者能够将 PSD 创建直接嵌入工作流，无论是自动化报表、动态图形还是批量处理。

## 常见问题

### Q1: Aspose.PSD 是否兼容不同的 Java IDE？

A1: 是的，Aspose.PSD 可无缝工作于各种 Java 集成开发环境（IDE）。

### Q2: 我可以在商业项目中使用 Aspose.PSD 吗？

A2: 可以，Aspose.PSD 可用于个人和商业项目。请查看 [购买页面](https://purchase.aspose.com/buy) 获取许可证详情。

### Q3: 如何获取 Aspose.PSD 的支持？

A3: 访问 [Aspose.PSD 论坛](https://forum.aspose.com/c/psd/34) 获取社区支持和讨论。

### Q4: 是否提供免费试用？

A4: 是的，您可以在此处获取免费试用 [here](https://releases.aspose.com/)。

### Q5: 测试时需要临时许可证吗？

A5: 您可以在此处获取用于测试的临时许可证 [here](https://purchase.aspose.com/temporary-license/)。

**附加问答**

**问：创建后可以更改图像尺寸吗？**  
答：可以，在保存之前使用 `image.resize(width, height)` 调整图像大小。

**问：支持哪些颜色模式？**  
答：Aspose.PSD 支持 RGB、CMYK、灰度和索引颜色模式。

---

**最后更新：** 2026-01-01  
**测试环境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}