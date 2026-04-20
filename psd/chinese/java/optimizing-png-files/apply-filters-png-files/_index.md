---
date: 2026-03-15
description: 了解如何使用 Aspose.PSD for Java 对 PNG 图像进行过滤。此分步指南涵盖 Java PNG 优化以及使用过滤类型将
  PSD 转换为 PNG。
linktitle: How to Filter PNG Files in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中过滤 PNG 文件
url: /zh/java/optimizing-png-files/apply-filters-png-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中过滤 PNG 文件

## 介绍
如果你在使用 Java 时想了解 **如何过滤 PNG** 图像，那么你来对地方了。在本教程中，我们将演示如何使用 Aspose.PSD for Java 应用 PNG 过滤器类型，该库还可以帮助你 **将 PSD 转换为 PNG** 并进行 **java png 优化**。完成后，你将能够微调压缩、提升视觉质量，并将此过程集成到任何 Java 项目中。

## 快速回答
- **什么库支持 Java 中的 PNG 过滤？** Aspose.PSD for Java。  
- **哪种过滤器在大多数图像上提供最佳压缩？** Paeth 过滤器（本例中使用）。  
- **运行代码是否需要许可证？** 免费试用可用于评估；生产环境需要许可证。  
- **我可以在同一工作流中将 PSD 转换为 PNG 吗？** 可以——加载 PSD 并使用所需的过滤器保存为 PNG。  
- **需要哪个 Java 版本？** Java 8 或更高。

## 实际上“如何过滤 png”是什么？
对 PNG 文件进行过滤是指选择一种预处理算法，在压缩之前准备像素数据。过滤器类型会影响文件大小以及 PNG 保存后颜色的保留程度。Aspose.PSD 通过 `PngOptions.setFilterType` 方法让你直接控制此步骤。

## 为什么使用 Aspose.PSD for Java 进行 PNG 优化？
- **完整的 PSD 支持：** 打开、编辑并导出 PSD 图层而不失真。  
- **内置过滤器选择：** 可在 Paeth、Sub、Up、Average 或 None 中选择。  
- **跨平台：** 在 Windows、Linux 和 macOS 上均可使用任意标准 JDK 运行。  
- **无外部本地依赖：** 纯 Java 实现简化部署。

## 前置条件
1. **Java Development Kit (JDK) 8+** – 确保 `java -version` 显示 1.8 或更高。  
2. **IDE (IntelliJ IDEA, Eclipse, or VS Code)** – 任选你熟悉的开发环境。  
3. **Aspose.PSD for Java library** – 从 [here](https://releases.aspose.com/psd/java/) 下载。  
4. **Basic Java knowledge** – 熟悉类、方法和文件 I/O。

## 导入包
首先，将所需的 Aspose.PSD 类引入你的 Java 文件：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngFilterType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

> **技巧提示：** 将 Aspose.PSD JAR 添加到项目的构建路径或 Maven/Gradle 依赖中，以确保导入能够正确解析。

## 步骤 1：设置文档目录
定义存放源 PSD 文件以及保存过滤后 PNG 的文件夹。

```java
String dataDir = "Your Document Directory"; // Adjust this path
```

将 `"Your Document Directory"` 替换为你机器上的绝对路径或相对路径。

## 步骤 2：加载 PSD 图像
打开你想要处理的 PSD 文件。将其强制转换为 `PsdImage` 可获得 PSD 专属功能。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

如果文件不存在，`Image.load` 会抛出异常——请确保路径正确。

## 步骤 3：创建 PNG 选项（Java PNG 优化）
配置 PNG 导出设置，包括直接回答 **如何过滤 png** 的过滤器类型。

```java
PngOptions options = new PngOptions();
options.setFilterType(PngFilterType.Paeth);
```

你可以尝试其他过滤器类型（`Sub`、`Up`、`Average`、`None`），观察它们对尺寸和质量的影响。此步骤同样展示了 **java png 优化**，因为所选过滤器会影响压缩效率。

## 步骤 4：保存 PNG 图像
最后，使用已定义的选项将处理后的图像写回磁盘。

```java
psdImage.save(dataDir + "ApplyFilterMethod_out.png", options);
```

生成的文件 `ApplyFilterMethod_out.png` 将是已过滤的 PNG，可用于网页或桌面。

## 常见问题及解决方案
| 症状 | 可能原因 | 解决办法 |
|---------|--------------|-----|
| `FileNotFoundException` | `dataDir` 路径不正确 | 确认目录字符串以分隔符结尾（`/` 或 `\\`）。 |
| 未观察到过滤效果 | 使用了 `PngFilterType.None` | 切换为 `Paeth` 或其他过滤器类型。 |
| 大 PSD 文件出现内存不足错误 | 未使用流式加载直接加载大文件 | 使用带 `loadOptions` 的 `PsdImage` 限制内存使用。 |

## 常见问答

**Q: 什么是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一个强大的 API，允许开发者读取、编辑和转换 PSD 文件，应用过滤器，并在无需 Adobe Photoshop 的情况下进行图像优化。

**Q: 如何下载 Aspose.PSD for Java？**  
A: 你可以从 Aspose 发布页面 [here](https://releases.aspose.com/psd/java/) 下载。

**Q: 我可以免费试用 Aspose.PSD 吗？**  
A: 可以，免费试用可在 [here](https://releases.aspose.com/) 获取。

**Q: 我可以对 PNG 图像应用哪些类型的过滤器？**  
A: Aspose.PSD 支持 Paeth、Sub、Up、Average 和 None。选择最能在尺寸和视觉保真度之间取得平衡的过滤器。

**Q: 我在哪里可以找到 Aspose.PSD 的支持？**  
A: 你可以访问 Aspose 论坛 [here](https://forum.aspose.com/c/psd/34) 获取帮助和支持。

## 结论
现在你已经了解了如何使用 Aspose.PSD for Java **过滤 PNG** 文件，如何 **将 PSD 转换为 PNG**，以及如何使用不同的过滤器类型进行 **java png 优化**。尝试各种过滤器，将此工作流集成到你的图像处理流水线中，享受更小且高质量的 PNG 资源。

---

**最后更新：** 2026-03-15  
**测试环境：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}