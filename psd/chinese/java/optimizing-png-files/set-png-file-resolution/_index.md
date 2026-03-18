---
date: 2026-03-18
description: 了解如何使用 Aspose.PSD for Java 更改 PNG 分辨率并设置图像分辨率。请按照本分步指南快速优化您的图像。
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD 在 Java 中更改 PNG 分辨率
url: /zh/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 更改 PNG 分辨率（Java）

## 介绍
如果您需要 **快速且可靠地更改 PNG 分辨率（Java）**，这里就是您的最佳去处。在本教程中，我们将逐步演示如何使用 Aspose.PSD for Java 调整 PNG 文件的分辨率。无论您是在构建批处理工具、Web 服务，还是仅仅对少量资源进行打磨，同样的方法都适用。打开您喜欢的 IDE，开始吧！

## 快速回答
- **哪个库负责 PNG 分辨率？** Aspose.PSD for Java  
- **主要方法？** `PngOptions.setResolutionSettings`  
- **常用 DPI 值？** 72 × 96 适用于网页图片  
- **需要许可证吗？** 试用版可用于测试，生产环境必须购买许可证  
- **支持的 JDK？** Java 8 或更高版本  

## 什么是 “change PNG resolution java”？
在 Java 中更改 PNG 分辨率指的是修改 DPI（每英寸点数）元数据，告诉浏览器和打印机图像应以多大尺寸显示。像素数据保持不变，但分辨率标签被更新，这会影响打印尺寸和质量。

## 为什么选择 Aspose.PSD 来完成此任务？
Aspose.PSD 提供了高级 API，抽象了底层 PNG 处理细节，让您专注于业务逻辑，而无需关心文件格式的怪癖。它支持数百种 PSD 功能，可在任何运行 Java 的平台上使用，且无需本地库。

## 前置条件
在开始之前，请确保您已经具备：

1. **Java Development Kit (JDK) 8+** – 代码可在任何近期的 JDK 上运行。  
2. **Aspose.PSD for Java** – 从 [download link](https://releases.aspose.com/psd/java/) 下载。  
3. **IDE** – IntelliJ IDEA、Eclipse 或带有 Java 支持的 VS Code。  
4. **示例 PSD 文件** – 我们将把它转换为 PNG 并更改分辨率。  
5. **基础 Java 知识** – 您可以直接理解下面的代码片段，无需额外解释。

## 导入包
现在一切就绪，导入您需要的类。这些导入让您能够加载图像、设置分辨率以及导出 PNG 选项。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步骤 1：设置 Java 项目
创建一个新的 Java 项目（或 Maven/Gradle 模块），并将 Aspose.PSD JAR 添加到构建路径。如果使用 Maven，请从 Aspose 仓库添加相应的依赖。

## 步骤 2：定义文档目录
告诉程序源 PSD 文件所在位置以及输出 PNG 的保存路径。

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

将 `"Your Document Directory"` 替换为包含 `sample.psd` 的绝对或相对路径。

## 步骤 3：加载 PSD 图像
使用 `PsdImage` 类从磁盘读取 PSD 文件。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

确保文件名与实际要处理的 PSD 文件匹配。

## 步骤 4：创建并配置 PNG 选项
这里就是实际 **更改 PNG 分辨率（Java）** 的地方。实例化 `PngOptions` 并通过 `ResolutionSetting` 设置水平和垂直 DPI。

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

可以将 `72` 和 `96` 替换为适合目标设备的任意数值。这就是 **set image resolution java** 操作的核心。

## 步骤 5：保存生成的 PNG
最后，将 PSD 导出为带有新分辨率元数据的 PNG。

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

文件 `SettingResolution_output.png` 将出现在同一文件夹中，已携带您指定的 DPI 值。

## 常见问题与技巧
- **路径错误** – 请再次确认 `dataDir` 以文件分隔符（`/` 或 `\`）结尾。  
- **不支持的 DPI** – 大多数浏览器会忽略 300 以上的 DPI，保持在合理范围内。  
- **内存使用** – 大型 PSD 可能占用大量 RAM，保存后请考虑调用 `psdImage.dispose()` 释放资源。  

## 结论
您已经学会了如何使用 Aspose.PSD **更改 PNG 分辨率（Java）**。通过调整 `ResolutionSetting`，您可以在不改变像素数据的前提下，控制 PNG 在打印机和设计工具中的呈现方式。进一步探索压缩级别、颜色深度或批处理等选项，以实现工作流的全自动化。

欲了解更深入的内容，请查阅官方 [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)。

## 常见问题
### 我可以使用 Aspose.PSD for Java 将 PSD 文件转换为什么格式？
您可以将 PSD 文件转换为 PNG、JPEG、BMP 和 TIFF 等格式。  
### 使用 Aspose.PSD for Java 是否需要许可证？
是的，虽然提供免费试用版，但评估结束后需要有效许可证才能继续使用。  
### 我可以在同一个程序中多次更改分辨率吗？
当然可以！您可以在同一应用中为不同的导出设置创建多个 `PngOptions` 实例。  
### 如果我的 PSD 文件损坏怎么办？
Aspose.PSD 能处理许多常见问题，但如果文件严重损坏，可能无法加载。请始终保留备份。  
### Aspose.PSD 适合高性能应用吗？
适合。它专为高效处理大文件而设计，能够满足性能密集型的图像处理任务。

## 常见问答
**问：如何为水平和垂直轴分别设置不同的 DPI？**  
答：如 PNG 选项示例所示，使用 `new ResolutionSetting(horizontalDpi, verticalDpi)`。

**问：能否一次性批处理多个 PSD 文件？**  
答：可以——将加载、选项配置和保存步骤放入遍历文件集合的循环中即可。

**问：更改 DPI 会影响文件大小吗？**  
答：通常不会；DPI 只是元数据。只有在修改压缩方式或像素尺寸时文件大小才会变化。

**问：有没有办法读取已有 PNG 的当前 DPI？**  
答：使用 `Image.load()` 加载 PNG，然后检查 `image.getResolutionSettings()`（PNG 文件支持此方法）。

**问：官方支持哪些 JDK 版本？**  
答：Aspose.PSD for Java 支持 JDK 8 至 JDK 21。

---

**最后更新：** 2026-03-18  
**测试环境：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}