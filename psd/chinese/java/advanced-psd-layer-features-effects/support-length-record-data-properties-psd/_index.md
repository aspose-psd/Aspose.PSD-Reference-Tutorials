---
date: 2026-02-20
description: 了解如何使用 Aspose.PSD for Java 支持长度记录属性并批量处理 PSD 文件。分步指南，附代码示例。
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: 支持长度记录属性 – 修改 PSD 矢量形状（Java）
url: /zh/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 支持长度记录属性 – 修改 PSD 矢量形状（Java）

## 介绍
如果您需要以编程方式 **修改 PSD 矢量形状**，Aspose.PSD for Java 库可以让您直接在 Java 代码中完全控制 Photoshop 文件。在本教程中，我们将逐步讲解如何 **支持长度记录属性**——这是编辑矢量形状图层时的关键步骤。完成后，您将能够打开 PSD，调整其矢量形状属性，并在不离开 IDE 的情况下保存更新后的文件。让我们开始吧！

## 快速答案
- **“修改 PSD 矢量形状” 是什么意思？** 调整 PSD 文件中基于矢量的图层的几何形状、路径操作或其他属性。  
- **哪个库负责此操作？** Aspose.PSD for Java。  
- **我需要许可证吗？** 免费试用可用于评估；生产环境需要商业许可证。  
- **实现大概需要多长时间？** 基本的形状修改脚本约需 10‑15 分钟。  
- **主要前置条件是什么？** Java JDK、Aspose.PSD for Java 和一个示例 PSD 文件。

## 什么是“支持长度记录属性”？
支持长度记录属性意味着访问并更新描述 PSD 中每条矢量路径的 `LengthRecord` 对象。修改这些记录可以控制形状之间的组合、相交或相减方式。

## 为什么使用 Aspose.PSD for Java 来支持长度记录属性？
- **无需 Photoshop** – 直接在任何服务器上处理 PSD 文件。  
- **丰富的 API** – 使用强类型类访问图层、资源和矢量数据。  
- **跨平台** – 在 Windows、Linux 或 macOS 上使用任意 JDK 运行。  
- **性能导向** – 高效的内存管理和快速保存操作。  

## 前置条件
1. **Java Development Kit (JDK)** – 从 [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下载或使用您喜欢的包管理器。  
2. **Aspose.PSD for Java** – 从 [Aspose releases page](https://releases.aspose.com/psd/java/) 获取最新的 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何支持 Java 的编辑器。  
4. **PSD 文件** – 在 Photoshop 中创建或获取一个示例 PSD 进行实验。  
5. **基础 Java 知识** – 熟悉类、对象和异常处理。

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

## 步骤 1：设置源目录和输出目录
定义原始 PSD 所在位置以及修改后文件的保存路径。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 步骤 2：加载 PSD 文件
使用 `Image.load` 打开文件，并将其强制转换为 `PsdImage` 以使用 PSD 专属功能。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 步骤 3：在图层中定位 Vsms 资源
矢量形状数据存储在 `VsmsResource` 中。遍历第二个图层的资源以找到它。

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 步骤 4：访问 LengthRecord
每个 `LengthRecord` 代表一条独立的矢量路径。获取您计划修改的记录。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 步骤 5：修改 PathOperation 属性
现在您可以通过更改 `PathOperations` 来 **修改 PSD 矢量形状**。这决定了形状之间的交互方式（例如排除、相交、相减）。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 步骤 6：保存修改后的 PSD 文件
将更改持久化到新文件中。

```java
psdImage.save(outPsdFilePath);
```

## 步骤 7：清理资源
释放 `PsdImage` 以释放内存。

```java
psdImage.dispose();
```

## 如何使用支持长度记录属性批量处理 PSD 文件
如果需要对多个 PSD 进行相同的矢量形状调整，可将上述代码包装在遍历文件目录的循环中。为每次迭代更新 `inPsdFilePath` 和 `outPsdFilePath`，即可高效 **批量处理 PSD 文件**。

## 常见陷阱与技巧
- **空值检查** – 在访问路径前务必确认 `resource` 不为 `null`。  
- **路径索引范围** – 确保使用的索引（`[2]`、`[7]`、`[11]`）在您编辑的特定 PSD 中实际存在。  
- **许可证** – 未使用有效许可证运行时，保存的 PSD 将嵌入水印。  

## 结论
现在您已经拥有一个完整的端到端示例，能够通过 Aspose.PSD for Java **修改 PSD 矢量形状**，并支持长度记录属性。无论是自动化资产流水线还是构建自定义设计工具，这些 API 都让您无需手动使用 Photoshop 即可操作矢量图层。进一步探索可尝试其他 `PathOperations`，或组合多个 `LengthRecord` 编辑以实现复杂形状。

## 常见问题

**Q: 如何处理不包含矢量形状图层的 PSD？**  
A: `VsmsResource` 将不存在，`resource` 会保持 `null`。请添加检查并跳过修改步骤或提示用户。

**Q: 我可以更改填充颜色或描边宽度等其他属性吗？**  
A: 可以，`LengthRecord` 提供了填充、描边和不透明度的额外 setter。请参考 API 文档获取完整细节。

**Q: 能否批量处理多个 PSD 文件？**  
A: 完全可以。将代码放入遍历 PSD 文件目录的循环中，每次调整输入输出路径即可。

**Q: 从文件路径加载时需要手动关闭流吗？**  
A: `Image.load` 方法内部会处理文件流，但如果您使用 `InputStream` 加载，请在使用后记得关闭它。

**Q: 这些 API 需要哪个版本的 Aspose.PSD？**  
A: `LengthRecord` 和 `PathOperations` 类自 Aspose.PSD 20.10 起可用。建议使用最新版本。

---

**最后更新：** 2026-02-20  
**测试环境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}