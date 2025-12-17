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

## Introduction
如果您需要**修改 PSD 矢量形状**，Aspose.PSD for Java 库让您可以直接在 Java 代码中完全控制 Photoshop 文件。在本教程中，我们将逐步讲解支持长度记录数据属性所需的全部内容——这是编辑矢量形状图层的关键步骤。完成后，您将能够打开 PSD，调整其矢量形状属性，并在不离开 IDE 的情况下保存更新后的文件。让我们开始吧！

## Quick Answers
- **“修改 PSD 矢量形状”是什么意思？** 调整 PSD 文件中基于矢量的图层的几何形状、路径操作或其他属性。  
- **哪个库负责此功能？** Aspose.PSD for Java。  
- **我需要许可证吗？** 免费试用可用于评估；生产环境需要商业许可证。  
- **实现需要多长时间？** 基本的形状修改脚本大约需要 10‑15 分钟。  
- **主要前提条件是什么？** Java JDK、Aspose.PSD for Java 和一个示例 PSD 文件。

## What is “modify PSD vector shapes”?
修改 PSD 矢量形状是指更改底层矢量路径数据——例如长度记录和路径操作——从而相应地更新形状的视觉外观。这在自动化图形流水线、批处理或自定义设计工具中尤为有用。

## Why use Aspose.PSD for Java to modify PSD vector shapes?
- **无需 Photoshop** – 可直接在任何服务器上处理 PSD 文件。  
- **丰富的 API** – 使用强类型类访问图层、资源和矢量数据。  
- **跨平台** – 在 Windows、Linux 或 macOS 上使用任何 JDK 运行。  
- **性能导向** – 高效的内存管理和快速保存操作。

## Prerequisites
1. **Java Development Kit (JDK)** – 从[Oracle 官方网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)下载，或使用您喜欢的包管理器。  
2. **Aspose.PSD for Java** – 从[Aspose 发布页面](https://releases.aspose.com/psd/java/)获取最新的 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何兼容 Java 的编辑器。  
4. **PSD 文件** – 在 Photoshop 中创建，或获取一个示例 PSD 进行实验。  
5. **基本的 Java 知识** – 熟悉类、对象和异常处理。

## Import Packages
First, import the classes you’ll need to work with PSD files and vector shape resources.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Step 1: Set Up Your Source and Output Directories
Define where the original PSD lives and where you want the modified file to be saved.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Step 2: Load the PSD File
Use `Image.load` to open the file and cast it to `PsdImage` for PSD‑specific features.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Step 3: Locate the Vsms Resource in the Layer
Vector shape data lives inside a `VsmsResource`. Loop through the second layer’s resources to find it.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Step 4: Access Length Records
Each `LengthRecord` represents a distinct vector path. Grab the ones you intend to modify.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Step 5: Modify Path Operation Properties
Now you can **modify PSD vector shapes** by changing their `PathOperations`. This determines how shapes interact (e.g., exclusion, intersection, subtraction).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Step 6: Save the Modified PSD File
Persist your changes to a new file.

```java
psdImage.save(outPsdFilePath);
```

## Step 7: Clean Up Resources
Dispose of the `PsdImage` to free memory.

```java
psdImage.dispose();
```

## Common Pitfalls & Tips
- **空值检查** – 在访问路径之前始终确认 `resource` 不为 `null`。  
- **路径索引范围** – 确保您使用的索引（`[2]`、`[7]`、`[11]`）在您编辑的特定 PSD 中存在。  
- **许可证** – 未使用有效许可证运行时，保存的 PSD 将嵌入水印。  

## Conclusion
现在，您已经拥有一个完整的端到端示例，展示如何使用 Aspose.PSD for Java 通过支持长度记录数据属性来**修改 PSD 矢量形状**。无论是自动化资产流水线还是构建自定义设计工具，这些 API 都能让您在无需手动使用 Photoshop 的情况下灵活操作矢量图层。通过尝试其他 `PathOperations` 或组合多个 `LengthRecord` 编辑来实现更复杂的形状，进一步探索吧。

## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java 是一个库，允许开发者使用 Java 以编程方式操作和处理 Photoshop PSD 文件。

### Can I use Aspose.PSD in a free project?
可以，您可以使用 Aspose 网站提供的试用版免费尝试该库。

### What types of modifications can I make to PSD files?
您可以在 PSD 文件中操作图层、形状、文本、路径操作等多种内容。

### Is Aspose.PSD compatible with other programming languages?
是的，Aspose 提供针对不同编程语言的库，包括 .NET 和 Python。

### Where can I find the documentation for Aspose.PSD?
您可以在[此处](https://reference.aspose.com/psd/java/)访问完整文档。

## Frequently Asked Questions

**Q: How do I handle a PSD that contains no vector shape layers?**  
A: The `VsmsResource` will be absent, so `resource` will stay `null`. Add a check and skip the modification step or inform the user.  
**答:** `VsmsResource` 将不存在，`resource` 会保持为 `null`。请添加检查，跳过修改步骤或提示用户。

**Q: Can I change other properties like fill color or stroke width?**  
A: Yes, `LengthRecord` provides additional setters for fill, stroke, and opacity. Refer to the API docs for full details.  
**答:** 可以，`LengthRecord` 提供了填充、描边和不透明度等额外的 setter。请参阅 API 文档获取完整细节。

**Q: Is it possible to batch‑process multiple PSD files?**  
A: Absolutely. Wrap the code inside a loop that iterates over a directory of PSD files, adjusting the input and output paths each time.  
**答:** 完全可以。将代码放入遍历 PSD 文件目录的循环中，并在每次迭代时调整输入和输出路径。

**Q: Do I need to close streams manually when loading from a file path?**  
A: The `Image.load` method handles file streams internally, but if you load from an `InputStream`, remember to close it after use.  
**答:** `Image.load` 方法会内部处理文件流，但如果使用 `InputStream` 加载，请在使用后记得关闭它。

**Q: What version of Aspose.PSD is required for these APIs?**  
A: The `LengthRecord` and `PathOperations` classes are available since Aspose.PSD 20.10. Using the latest version is recommended.  
**答:** `LengthRecord` 和 `PathOperations` 类自 Aspose.PSD 20.10 起可用。建议使用最新版本。

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}