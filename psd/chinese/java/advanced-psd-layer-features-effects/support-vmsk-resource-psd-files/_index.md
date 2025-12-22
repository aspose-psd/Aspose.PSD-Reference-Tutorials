---
date: 2025-12-18
description: 学习如何使用 Aspose.PSD for Java 在 PSD 文件中创建矢量蒙版（Vmsk 资源）。本分步教程展示了如何添加矢量蒙版、将
  PSD 转换为 PNG 等操作。
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: 使用 Java 在 PSD 文件中创建矢量蒙版（Vmsk 资源）
url: /zh/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 在 PSD 文件中创建矢量蒙版 (Vmsk 资源)

## 介绍
如果您需要在 Photoshop (PSD) 文件中 **创建矢量蒙版** (Vmsk) 资源，Aspose.PSD for Java 为您提供了一种简洁的编程方式。无论是构建设计自动化工具，还是为现有图形流水线添加自定义蒙版支持，本教程都会一步步演示——加载 PSD、读取 Vmsk 资源、修改属性并保存结果。完成后，您将能够熟练处理矢量蒙版、将 PSD 转换为 PNG，以及在文件中扩展其他矢量数据。

## 快速解答

- **什么是 Vmsk 资源？** 它是存储在 PSD 文件中的矢量蒙版数据，用于定义图层的复杂矢量形状。

- **哪个库支持它？** Aspose.PSD for Java 提供对 Vmsk 资源的完整读/写访问权限。

- **我需要许可证吗？** 提供免费试用版；生产环境使用需要商业许可证。

- **我可以将编辑后的 ​​PSD 文件转换为 PNG 格式吗？** 可以——保存后，您可以使用相同的 API 加载 PSD 文件并导出为 PNG 文件。

- **是否支持 Maven？** 当然支持；Aspose.PSD 可以添加为 Maven 依赖项（请参阅“aspose psd maven”关键字）。

## 什么是矢量蒙版（Vmsk 资源）？

矢量蒙版 (Vmsk) 是一种非像素级的蒙版，它使用贝塞尔曲线和路径记录来定义图层上的透明和不透明区域。由于它基于矢量，因此可以无损缩放——非常适合高分辨率图形。

## 为什么使用 Aspose.PSD 创建矢量蒙版？

- **自动化：**无需打开 Photoshop 即可通过编程方式添加或修改蒙版。

- **一致性：**确保您生成的每个 PSD 文件都遵循相同的蒙版规则。

- **跨平台：**可在任何支持 Java 的操作系统上运行。

- **集成：**可与其他 Aspose API（例如，将 PSD 转换为 PNG）结合使用，实现端到端的工作流程。

## 前提条件

在深入代码之前，请确保您已具备以下条件：

### 所需工具

- Java 开发工具包 (JDK)：请确保您的计算机上已安装 JDK。如果没有，您可以从 [Oracle 网站](https://www.oracle.com/java/technologies/javase-downloads.html) 下载。

- Aspose.PSD for Java 库：这是一个功能强大的 PSD 文件管理库。您可以从 [Aspose 发布页面](https://releases.aspose.com/psd/java/) 下载。如果您想在购买前试用，也可以从 [免费试用版](https://releases.aspose.com/) 开始。

- IDE：任何 Java IDE（例如 IntelliJ IDEA、Eclipse 等）都适用于此项目。

### 设置工作空间
1. **创建新的 Java 项目** – 打开您常用的 IDE 并创建一个新项目。

2. **添加 Aspose 库** – 下载 Aspose JAR 文件后，将其添加到项目的构建路径中，以便您可以访问所有与 PSD 相关的类。

环境准备就绪后，让我们开始实际操作。

## 如何使用 Java 在 PSD 文件中创建矢量蒙版

以下是分步指南。代码块与原始教程相同；我们添加说明文字只是为了让每个步骤都清晰明了。

## 导入包

在处理 PSD 文件之前，我们需要从 Aspose.PSD 库导入必要的类。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

现在一切准备就绪，让我们一步步完成每个步骤。

## 第一步：加载 PSD 文件

首先，你需要加载 PSD 文件。一切精彩的部分就此开始。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- 我们将 `dataDir` 设置为 PSD 文件所在的目录。

- 我们创建一个字符串作为 `sourceFileName`，将目录和 PSD 文件名组合在一起。

- 最后，我们使用 `Image.load()` 将 PSD 文件加载到 `PsdImage` 对象中。

## 步骤 2：获取 Vmsk 资源

现在 PSD 图像已经加载完毕，接下来获取 Vmsk 资源。

```java
VmskResource resource = getVmskResource(im);
```

- 我们调用 `getVmskResource()` 方法，该方法负责从镜像中搜索并检索 Vmsk 资源。

## 步骤 3：验证 Vmsk 资源属性

在进行任何修改之前，必须验证 Vmsk 资源是否处于预期状态。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- 在这里，我们将检查 Vmsk 资源的各项属性。我们要确保它未被禁用、反转或未链接，并且路径数量正确。

## 第 4 步：访问并验证每条路径

让我们更深入地检查一下 Vmsk 资源中的路径。

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- 我们正在提取三个特定的路径记录，并验证它们的类型和属性，以确保它们符合我们的标准。

## 第 5 步：编辑 Vmsk 资源

现在我们进入修改部分！您可以根据需要调整 Vmsk 资源的属性。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 在此代码块中，我们将切换 Vmsk 资源的各项属性。通过将它们设置为 `true`，我们可以控制掩码在 PSD 文件中的行为。

## 步骤 6：修改贝塞尔节点

贝塞尔节点对于矢量路径至关重要。让我们在这里修改一些值。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 我们正在访问特定的 `BezierKnotRecord` 路径并更改其上的点，以可能重塑矢量蒙版。

## 第 7 步：保存修改后的 PSD 文件

所有编辑完成后，即可保存修改后的 PSD 文件。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- 我们设置导出的 PSD 文件路径，然后调用 `im.save()` 将更改写入这个新文件。

## 第 8 步：清理资源

最后，我们需要确保正确释放图像资源。

```java
im.dispose();
```

- 使用完毕后，务必及时释放所有资源，这有助于避免应用程序中的内存泄漏。

## 总结

恭喜！您刚刚完成了使用 Aspose.PSD for Java 在 PSD 文件中创建矢量蒙版 (Vmsk) 资源的详细步骤。从加载图像、检索和验证 Vmsk 资源、编辑其属性，到保存修改后的 PSD 文件，您现在已经掌握了自动化矢量蒙版工作流程的坚实基础。使用这些技巧可以丰富您的设计流程，与其他 Aspose API 集成（例如将 PSD 转换为 PNG），或构建自定义图形工具。

## 常见问题解答

**问：如何向现有图层添加新的矢量蒙版？** 答：创建一个 `VmskResource`，填充所需的路径记录（例如 `BezierKnotRecord`），并将其附加到图层的资源集合中。

**问：我可以直接将编辑后的 ​​PSD 转换为 PNG 而无需打开 Photoshop 吗？** 答：可以——保存 PSD 后，使用 `Image.load()` 重新加载它，然后调用 `im.save("output.png")` 并指定 PNG 格式。

**问：是否有办法在 CI/CD 流程中实现自动化？** 答：当然可以。由于该流程完全基于 Java，您可以将其嵌入到 Maven/Gradle 构建、Docker 容器或任何支持 Java 的 CI 系统中。

**问：哪些版本的 Aspose.PSD 与 Java 11 及更高版本兼容？** 答：所有近期版本（2024-2025 年）均支持 Java 8 及更高版本，包括 Java 11、17 和更新的 LTS 版本。

**问：开发版本需要许可证吗？** 答：免费评估许可证适用于开发和测试。生产部署需要商业许可证。

---

**上次更新：** 2025-12-18
**测试版本：** Aspose.PSD 24.11 for Java
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
