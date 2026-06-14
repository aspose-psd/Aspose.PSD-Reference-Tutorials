---
date: 2026-03-15
description: 在本分步指南中，了解如何使用 Aspose.PSD for Java 创建 PSD 文件、生成 PSD 调色板并设置 PSD 颜色模式。
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 创建 PSD 文件
url: /zh/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 创建 PSD 文件

## 介绍
如果你曾经想过**如何以编程方式创建 PSD**文件，那么你来对地方了。Aspose.PSD for Java 为你提供对 Photoshop 文档的完整控制，让你无需打开 Photoshop 就能生成、编辑和保存 PSD 文件。在本教程中，我们将演示如何创建**索引 PSD**文件、设置 PSD 颜色模式以及生成自定义颜色调色板——全部使用清晰的、一步一步的 Java 代码。无论你是在构建图形流水线、自动化资源创建，还是仅仅进行实验，这里的概念都能帮助你将视觉创意付诸实现。

## 快速回答
- **我需要哪个库？** Aspose.PSD for Java
- **我可以创建索引 PSD 吗？** 是的，只需将颜色模式设置为 `Indexed`
- **需要安装 Photoshop 吗？** 不需要，Aspose.PSD 可独立工作
- **需要哪个 Java 版本？** JDK 8 或更高
- **画布可以多大？** 任意尺寸；本例使用 500 × 500 px

## 什么是索引 PSD 文件？
索引 PSD 将颜色存储在调色板中，而不是为每个像素存储完整的颜色值。这可以减小文件大小，适用于颜色受限的图形，如图标或 UI 资源。通过生成自定义调色板，你可以精确控制最终图像中出现的颜色。

## 为什么要生成 PSD 颜色调色板？
创建 **PSD 颜色调色板** 可以让你：
- 保持文件体积小，适用于网页或移动端使用  
- 通过限制颜色为企业调色板，确保品牌一致性  
- 加快支持索引图像的应用程序的渲染速度  

## 前置条件
在深入代码之前，请确保你具备以下条件：

1. **Java 基础知识** – 你应熟悉类、方法和对象创建。  
2. **Java Development Kit (JDK) 8+** – 已在 IDE 中安装并配置。  
3. **IDE（IntelliJ IDEA、Eclipse 等）** – 可选，但强烈建议使用以便更轻松调试。  
4. **Aspose.PSD for Java 库** – 在 **[此处](https://releases.aspose.com/psd/java/)** 下载并将 JAR 添加到项目的类路径中。  
5. **基本的平面设计概念** – 了解颜色模式、调色板和基本形状有助于你跟随教程。  

## 导入包
在继续代码之前，让我们确保已在 Java 应用程序中导入所有必需的包。以下是你需要的内容：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

这些导入将允许你通过 Aspose.PSD 使用 PSD 选项、颜色和图形操作。

现在，让我们逐步拆解代码，了解**如何创建 PSD**文件并使用索引颜色模式。

## 步骤 1：设置文档目录
首先，定义生成的 PSD 将保存的位置。

```java
String dataDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为绝对或相对路径，例如 `"/Users/YourName/Documents/"`。

## 步骤 2：创建 PsdOptions 实例
`PsdOptions` 保存即将生成的文件的所有设置。

```java
PsdOptions createOptions = new PsdOptions();
```

## 步骤 3：设置 PsdOptions 的核心属性
在这里我们指定输出位置、将 **set psd color mode** 设置为 `Indexed`，以及 PSD 版本。

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – 新文件的完整路径。  
- **Color Mode** – `Indexed` 告诉 Aspose.PSD 使用基于调色板的图像。  
- **Version** – PSD 格式版本（5 适用于大多数现代 Photoshop 版本）。

## 步骤 4：创建颜色调色板（生成 PSD 颜色调色板）
定义索引图像中可用的颜色。

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette` 数组可容纳最多 256 个 `Color` 对象。  
- `CompressionMethod.RLE` 为索引图像提供高效的无损压缩。

## 步骤 5：创建 PSD 图像画布
现在我们创建一个具有所需尺寸的空白 PSD。

```java
Image psd = Image.create(createOptions, 500, 500);
```

这将创建一个 500 × 500 像素的画布，使用前面定义的调色板。

## 步骤 6：在 PSD 上绘制图形
添加可视内容——这里我们在白色背景上绘制一个简单的红色椭圆。

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` 将背景填充为白色。  
- `drawEllipse` 绘制一个红色椭圆，线宽为 6 像素。

## 步骤 7：保存 PSD 文件
最后，将图像持久化到磁盘。

```java
psd.save();
```

文件 `Newsample_out.psd` 将出现在你之前指定的目录中。

## 常见问题与技巧
- **调色板大小** – 如果需要超过 4 种颜色，只需将它们添加到 `palette` 数组中（最多 256）。  
- **文件权限** – 确保 Java 进程对 `dataDir` 有写入权限。  
- **颜色模式错误** – 忘记调用 `createOptions.setColorMode(ColorModes.Indexed)` 会生成 RGB PSD，而不是索引 PSD。  

## 常见问答

**Q: 什么是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一个库，能够使用 Java 以编程方式操作 PSD（Photoshop）文件。

**Q: 我可以免费使用 Aspose.PSD 吗？**  
A: 可以，你可以在 **[此处](https://releases.aspose.com/)** 获取 Aspose.PSD 的免费试用版。

**Q: 使用 Aspose.PSD 是否需要安装 Photoshop？**  
A: 不需要，你可以在没有 Photoshop 的情况下创建和操作 PSD 文件，因为 Aspose.PSD 独立处理所有操作。

**Q: 如何获取 Aspose.PSD 的临时许可证？**  
A: 你可以在 **[此处](https://purchase.aspose.com/temporary-license/)** 申请临时许可证。

**Q: 哪里可以获得 Aspose.PSD 的支持？**  
A: 你可以在 Aspose 论坛 **[此处](https://forum.aspose.com/c/psd/34)** 获取支持。

## 结论
你已经学习了**如何创建 PSD**文件并使用索引颜色模式，生成了自定义调色板，并添加了简单的图形——全部使用 Aspose.PSD for Java。掌握这些基础后，你可以扩展到更复杂的绘图、图层管理和批处理。想进一步探索，请查阅官方 API 参考 **[此处](https://reference.aspose.com/psd/java/)**，并继续尝试不同的调色板和绘图原语。

---

**最后更新：** 2026-03-15  
**测试环境：** Aspose.PSD for Java 24.12 (latest)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}