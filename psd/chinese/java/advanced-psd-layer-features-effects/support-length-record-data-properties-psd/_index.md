---
date: 2025-12-17
description: 了解如何使用 Aspose.PSD for Java 通过支持长度记录数据属性来修改 PSD 矢量形状。分步指南并附有代码示例。
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: 如何修改 PSD 矢量形状 – 在 Java 中支持 Length Record 数据属性
url: /zh/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 中支持长度记录数据属性 - Java

## 介绍
如果您需要**修改 PSD 矢量形状**，Aspose.PSD for Java 库让您可以直接在 Java 代码中完全控制 Photoshop 文件。在本教程中，我们将逐步讲解支持长度记录数据属性所需的全部内容——这是编辑矢量形状图层的关键步骤。完成后，您将能够打开 PSD，调整其矢量形状属性，并在不离开 IDE 的情况下保存更新后的文件。让我们开始吧！

## 快速解答
- **“修改 PSD 矢量形状”是什么意思？** 调整 PSD 文件中基于矢量的图层的几何形状、路径操作或其他属性。  
- **哪个库负责此功能？** Aspose.PSD for Java。  
- **我需要许可证吗？** 免费试用可用于评估；生产环境需要商业许可证。  
- **实现需要多长时间？** 基本的形状修改脚本大约需要 10‑15 分钟。  
- **主要前提条件是什么？** Java JDK、Aspose.PSD for Java 和一个示例 PSD 文件。

## 什么是“修改PSD矢量图形”？
修改 PSD 矢量形状是指更改底层矢量路径数据——例如长度记录和路径操作——从而相应地更新形状的视觉外观。这在自动化图形流水线、批处理或自定义设计工具中尤为有用。

## 为什么使用 Aspose.PSD for Java 来修改 PSD 矢量图形？
- **无需 Photoshop** – 可直接在任何服务器上处理 PSD 文件。  
- **丰富的 API** – 使用强类型类访问图层、资源和矢量数据。  
- **跨平台** – 在 Windows、Linux 或 macOS 上使用任何 JDK 运行。  
- **性能导向** – 高效的内存管理和快速保存操作。

## 先决条件
1. **Java Development Kit (JDK)** – 从[Oracle 官方网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)下载，或使用您喜欢的包管理器。  
2. **Aspose.PSD for Java** – 从[Aspose 发布页面](https://releases.aspose.com/psd/java/)获取最新的 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何兼容 Java 的编辑器。  
4. **PSD 文件** – 在 Photoshop 中创建，或获取一个示例 PSD 进行实验。  
5. **基本的 Java 知识** – 熟悉类、对象和异常处理。

## 导入包

首先，导入处理 PSD 文件和矢量形状资源所需的类。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 第一步：设置源目录和输出目录

定义原始 PSD 文件所在的位置以及修改后的文件保存的位置。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 步骤 2：加载 PSD 文件

使用 `Image.load` 打开文件并将其转换为 `PsdImage` 类型，以便使用 PSD 特有的功能。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 步骤 3：在图层中查找 Vsms 资源

矢量形状数据存储在 `VsmsResource` 中。遍历第二个图层的资源以查找它。
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 步骤 4：访问长度记录

每个 `LengthRecord` 代表一个不同的向量路径。获取您想要修改的记录。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 第 5 步：修改路径操作属性

现在您可以通过更改 PSD 矢量形状的 `PathOperations` 属性来**修改 PSD 矢量形状**。这决定了形状之间的交互方式（例如，排除、相交、减法）。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 第六步：保存修改后的PSD文件

将更改保存到新文件中。

```java
psdImage.save(outPsdFilePath);
```

## 第 7 步：清理资源

释放 `PsdImage` 以释放内存。

```java
psdImage.dispose();
```

## 常见陷阱和技巧
- **空值检查** – 在访问路径之前始终确认 `resource` 不为 `null`。  
- **路径索引范围** – 确保您使用的索引（`[2]`、`[7]`、`[11]`）在您编辑的特定 PSD 中存在。  
- **许可证** – 未使用有效许可证运行时，保存的 PSD 将嵌入水印。  

## 结论
现在，您已经拥有一个完整的端到端示例，展示如何使用 Aspose.PSD for Java 通过支持长度记录数据属性来**修改 PSD 矢量形状**。无论是自动化资产流水线还是构建自定义设计工具，这些 API 都能让您在无需手动使用 Photoshop 的情况下灵活操作矢量图层。通过尝试其他 `PathOperations` 或组合多个 `LengthRecord` 编辑来实现更复杂的形状，进一步探索吧。

## 常见问题解答

**问：如何处理不包含矢量形状图层的PSD文件？**  
 
**答:** `VsmsResource` 将不存在，`resource` 会保持为 `null`。请添加检查，跳过修改步骤或提示用户。

**问：我可以更改其他属性吗，例如填充颜色或描边宽度？**  
 
**答:** 可以，`LengthRecord` 提供了填充、描边和不透明度等额外的 setter。请参阅 API 文档获取完整细节。

**问：是否可以批量处理多个PSD文件？**  

**答:** 完全可以。将代码放入遍历 PSD 文件目录的循环中，并在每次迭代时调整输入和输出路径。

**问：从文件路径加载时，是否需要手动关闭流？**  

**答:** `Image.load` 方法会内部处理文件流，但如果使用 `InputStream` 加载，请在使用后记得关闭它。

**问：这些 API 需要哪个版本的 Aspose.PSD？**  

**答:** `LengthRecord` 和 `PathOperations` 类自 Aspose.PSD 20.10 起可用。建议使用最新版本。

---

**上次更新时间：** 2025-12-17
**测试版本：** Aspose.PSD for Java 24.11
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}