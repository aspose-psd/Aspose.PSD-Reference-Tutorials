---
date: 2026-09-23
description: 了解如何使用 Aspose.PSD for Java 修改 PSD 矢量形状并批量处理 PSD 文件。提供详细步骤、技巧以及代码占位符，帮助您实现完整解决方案。
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: 在 PSD 中支持 Length Record 数据属性 - Java
og_description: 了解如何使用 Aspose.PSD for Java 修改 PSD 矢量形状并批量处理 PSD 文件。提供逐步指南、代码占位符和专家技巧。
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: 使用 Aspose.PSD for Java 修改 PSD 矢量形状
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: 使用 Aspose.PSD for Java 修改 PSD 矢量形状
url: /zh/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 修改 PSD 矢量形状

## 介绍
如果您需要以编程方式**修改 PSD 矢量形状**，Aspose.PSD for Java 可让您直接在 Java 代码中完全控制 Photoshop 文件。本教程将引导您支持长度记录属性——这是编辑矢量形状图层时的关键步骤。完成后，您将能够打开 PSD，调整其矢量形状数据，并在无需启动 Photoshop 的情况下保存更新后的文件。

## 快速答案
- **“修改 PSD 矢量形状”是什么意思？** 调整 PSD 文件中基于矢量的图层的几何形状、路径操作或其他属性。  
- **哪个库处理此操作？** Aspose.PSD for Java。  
- **我需要许可证吗？** 免费试用可用于评估；生产环境需要商业许可证。  
- **实现需要多长时间？** 基本的形状修改脚本大约需要 10‑15 分钟。  
- **主要前提条件是什么？** Java JDK、Aspose.PSD for Java 和一个示例 PSD 文件。

## 什么是“支持长度记录属性”？
支持长度记录属性意味着访问并更新描述 PSD 中每个矢量路径的 `LengthRecord` 对象。这些记录存储路径的长度、类型以及与其他路径的连接方式等信息。修改它们可以控制形状之间的组合、相交或相减，从而实现精确的矢量编辑。

## 为什么使用 Aspose.PSD for Java 来支持长度记录属性？
加载 PSD，编辑矢量数据并保存——全部无需 Photoshop。Aspose.PSD 在普通服务器上可在 2 秒内处理数百页的 PSD，提供超过 150 个类（其中包括 30 多个矢量相关类型），并可在 Windows、Linux 或 macOS 上运行，支持任何 JDK 11+。这个注重性能的库消除了昂贵桌面软件的需求。

## 先决条件
1. **Java 开发工具包 (JDK)** – 从 [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下载，或使用您喜欢的包管理器。  
2. **Aspose.PSD for Java** – 从 [Aspose releases page](https://releases.aspose.com/psd/java/) 获取最新的 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何兼容 Java 的编辑器。  
4. **PSD 文件** – 在 Photoshop 中创建，或获取一个示例 PSD 进行实验。  
5. **基本的 Java 知识** – 熟悉类、对象和异常处理。

## 导入包
导入语句将核心 Aspose.PSD 类（如 `PsdImage`、`VsmsResource` 和 `LengthRecord`）引入作用域。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 步骤 1：设置源目录和输出目录
定义原始 PSD 所在位置以及修改后文件的写入位置。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 步骤 2：加载 PSD 文件
使用 `Image.load` 打开文件，并将其强制转换为 `PsdImage` 以使用 PSD‑specific 功能。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 步骤 3：在图层中定位 Vsms 资源
`VsmsResource` 是存储图层矢量形状数据的容器。遍历第二个图层的资源以找到它。

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
`LengthRecord` 表示一个独立的矢量路径。获取您打算修改的记录。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 步骤 5：修改路径操作属性
`PathOperations` 定义各个形状的交互方式（例如排除、相交、相减）。更改这些值会更新矢量图层的视觉组合。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 步骤 6：保存修改后的 PSD 文件
将更改持久化到新文件。

```java
psdImage.save(outPsdFilePath);
```

## 步骤 7：清理资源
释放 `PsdImage` 实例以释放内存并避免资源泄漏。

```java
psdImage.dispose();
```

## 如何使用支持长度记录属性批量处理 PSD 文件
将单文件工作流包装在循环中，遍历 PSD 目录，对每个文件更新 `inPsdFilePath` 和 `outPsdFilePath`。此方法可在几分钟内对数十或数百个文件应用相同的矢量形状调整，适用于自动化资产流水线。

## 常见陷阱与技巧
- **空值检查** – 在访问成员之前始终确认 `resource` 不为 `null`。  
- **路径索引范围** – 确保您使用的索引（例如 `[2]`、`[7]`、`[11]`）在您编辑的特定 PSD 中存在。  
- **许可证** – 未使用有效许可证运行时，会在保存的 PSD 中嵌入水印。  

## 结论
现在，您已经拥有一个完整的端到端示例，展示如何通过使用 Aspose.PSD for Java 支持长度记录属性来**修改 PSD 矢量形状**。无论是自动化资产流水线还是构建自定义设计工具，这些 API 都为您提供了在无需手动 Photoshop 操作的情况下操作矢量图层的灵活性。尝试其他 `PathOperations` 值或组合多个 `LengthRecord` 编辑，以创建复杂形状。

## 常见问题

**问：如何处理不包含矢量形状图层的 PSD？**  
答：`VsmsResource` 将不存在，因此 `resource` 为 `null`。添加检查并跳过修改步骤，或通知用户。

**问：我可以更改其他属性，如填充颜色或笔画宽度吗？**  
答：可以，`LengthRecord` 提供了填充、笔画和不透明度的 setter。请参阅 API 文档获取完整列表。

**问：是否可以批量处理多个 PSD 文件？**  
答：完全可以。将代码包装在遍历 PSD 文件目录的循环中，每次调整输入和输出路径。

**问：从文件路径加载时是否需要手动关闭流？**  
答：`Image.load` 会自动处理文件流，但如果从 `InputStream` 加载，使用后请记得关闭它。

**问：这些 API 需要哪个版本的 Aspose.PSD？**  
答：`LengthRecord` 和 `PathOperations` 类自 Aspose.PSD 20.10 起已提供。建议使用最新版本（撰写时为 24.11）。

---

**最后更新：** 2026-09-23  
**测试环境：** Aspose.PSD for Java 24.11  
**作者：** Aspose

## 相关教程

- [将 PSD 转换为 PNG 并创建矢量蒙版 Java – PSD 文件中的 Vmsk 资源](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [使用 Aspose.PSD for Java 将 PSD 转换为 PNG 并支持图层蒙版](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [为 PSD 文件添加图层支持](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}