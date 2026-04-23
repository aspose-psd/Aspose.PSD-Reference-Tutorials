---
date: 2026-03-07
description: 学习如何在 PSD 文件中使用 Aspose.PSD for Java 添加“色阶调整图层”来调整色阶，快速掌握色调微调。
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: 如何调整色阶 – 在 PSD 中添加色阶调整图层
url: /zh/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 中添加色阶调整图层

## 介绍
如果你想在 Photoshop 文档中 **如何调整色阶**，色阶调整图层是完美的工具。它可以在不永久更改原始像素的情况下微调阴影、中间调和高光。在本教程中，我们将演示如何使用 Aspose.PSD for Java 向 PSD 文件添加色阶调整图层，让你只需几步即可实现专业级的色调控制。

## 快速回答
- **色阶调整图层的作用是什么？** 它以非破坏性的方式修改图像的色调范围。  
- **使用的是哪个库？** Aspose.PSD for Java。  
- **需要许可证吗？** 开发阶段可以使用免费试用版；生产环境需要许可证。  
- **实现大约需要多长时间？** 基本调整大约需要 10‑15 分钟。  
- **可以调整多个通道吗？** 可以，您可以为每个颜色通道单独设置输入/输出色阶。

## 什么是色阶调整图层？
色阶调整图层通过调整输入阴影、中间调和高光以及输出色阶来校正图像的色调平衡。由于它位于独立图层上，您可以随时切换可见性或删除它，而不会影响底层的艺术作品。

## 为什么使用 Aspose.PSD 添加色阶调整图层？
- **自动化：** 将色阶微调集成到批处理流水线中。  
- **跨平台：** 在任何支持 Java 的操作系统上均可运行。  
- **精确度：** 通过编程方式访问每个通道的设置，获得精确结果。  

## 前置条件
1. Java Development Kit (JDK)。如果没有，请从 [Oracle 网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下载，或使用 OpenJDK。  
2. Aspose.PSD for Java 库 – 从此 [下载链接](https://releases.aspose.com/psd/java/) 获取最新的 JAR 包。  
3. 基本的 Java 编程知识。  
4. 一个 IDE（如 IntelliJ IDEA、Eclipse 或 NetBeans），并将 Aspose.PSD JAR 添加到项目的类路径中。

## 导入包
在编写代码之前，需要从 Aspose.PSD 库中导入必要的包。操作如下：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
这些导入让我们能够访问加载 PSD 文件、操作色阶调整图层以及操控各通道设置的类。

## 如何在 PSD 文件中调整色阶
下面是一份逐步指南，向你展示 **如何以编程方式调整色阶**。

### 步骤 1：设置文件路径
定义源 PSD 所在位置以及编辑后文件的保存路径。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
将 `"Your Document Directory"` 替换为你机器上的实际文件夹路径。

### 步骤 2：加载 PSD 文件
从源文件创建 `PsdImage` 实例。
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
现在你可以完全访问 PSD 中的所有图层。

### 步骤 3：遍历图层
查找需要修改的色阶调整图层。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
`instanceof LevelsLayer` 检查确保我们只处理色阶调整图层。

### 步骤 4：调整通道设置
微调所选通道的输入和输出值。
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **输入中间调水平：** 调整中间调范围。  
- **输入阴影水平：** 加深或提亮阴影。  
- **输入高光水平：** 控制最亮的部分。  
- **输出阴影/高光水平：** 定义最终的输出范围。

随意尝试不同的数值，观察它们对图像的影响。

### 步骤 5：保存修改后的 PSD 文件
将更改持久化到新文件中。
```java
im.save(psdPathAfterChange);
```
你将在 `psdPathAfterChange` 指定的位置找到更新后的 PSD。

## 常见问题及解决方案
- **文件未找到：** 确认 `dataDir` 指向正确的文件夹，并且源 PSD 确实存在。  
- **ClassCastException：** 确保加载的文件确实是 PSD；其他格式需要使用不同的类。  
- **许可证错误：** 生产构建请使用有效的 Aspose.PSD 许可证；开发阶段可使用试用版。

## 结论
现在你已经掌握了 **如何通过添加和配置色阶调整图层** 在 PSD 文件中使用 Aspose.PSD for Java 调整色阶。这一技术让你在保持工作流全自动化的同时，精准控制图像的色调平衡。继续尝试不同的通道数值，并探索批处理，以将相同的调整应用于多张图像。

## 常见问答

**问：什么是色阶调整图层？**  
答：它是一种非破坏性的图层，允许你修改图像的色调范围（阴影、中间调、高光）。

**问：可以在不购买许可证的情况下使用 Aspose.PSD 吗？**  
答：可以，您可以使用免费试用版评估库，但商业部署需要许可证。

**问：在哪里可以找到 Aspose.PSD 的文档？**  
答：文档可在 [此处](https://reference.aspose.com/psd/java/) 查看。

**问：Aspose 产品有社区支持吗？**  
答：当然！您可以在 [Aspose 论坛](https://forum.aspose.com/c/psd/34) 提问并获取帮助。

**问：如何获取 Aspose.PSD 的临时许可证？**  
答：您可以在 [此处](https://purchase.aspose.com/temporary-license/) 申请临时许可证。

---

**最后更新：** 2026-03-07  
**测试环境：** Aspose.PSD 最新版本（Java）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}