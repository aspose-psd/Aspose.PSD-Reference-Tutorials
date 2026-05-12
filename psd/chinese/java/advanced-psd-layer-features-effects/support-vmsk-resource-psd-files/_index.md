---
date: 2026-02-22
description: 学习如何使用 Aspose.PSD for Java 创建矢量蒙版、添加矢量蒙版 PSD，并以编程方式操作 Vmsk 资源。
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: 在 PSD 文件中创建矢量蒙版（Java）– Vmsk 资源
url: /zh/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

 With:", "Author:" translate.

Then closing shortcodes.

Also note "Provide ONLY the translated content, no explanations."

Let's produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 创建 Vector Mask Java – PSD 文件中的 Vmsk 资源

## Introduction
如果您需要在 Photoshop（PSD）文件中 **create vector mask**（Vmsk）资源，Aspose.PSD for Java 为您提供了一种简洁的编程方式来实现。无论您是在构建设计自动化工具，还是在现有图形流水线中添加自定义遮罩支持，本教程都会一步步引导您——加载 PSD、读取 Vmsk 资源、调整其属性并保存结果。完成后，您将能够轻松处理矢量遮罩、将 PSD 转换为 PNG，并通过 **create vector mask java** 技术向文件中添加额外的矢量数据。

## Quick Answers
- **What is a Vmsk resource?** 它是存储在 PSD 文件中的矢量遮罩数据，用于定义图层的复杂矢量形状。  
- **Which library supports it?** Aspose.PSD for Java 提供对 Vmsk 资源的完整读写访问。  
- **Do I need a license?** 提供免费试用版；生产环境需要商业许可证。  
- **Can I convert the edited PSD to PNG?** 可以——保存后，您可以再次加载 PSD 并使用相同的 API 导出为 PNG。  
- **Is Maven support available?** 当然；Aspose.PSD 可以作为 Maven 依赖添加（参见 “aspose psd maven” 关键字）。

## What is a Vector Mask (Vmsk Resource)?
矢量遮罩（Vmsk）是一种非像素基的遮罩，使用贝塞尔曲线和路径记录来定义图层的透明和不透明区域。由于基于矢量，它可以在不失真情况下任意缩放——非常适合高分辨率图形。

## Why Create a Vector Mask with Aspose.PSD?
- **Automation:** 可在不打开 Photoshop 的情况下以编程方式添加或修改遮罩。  
- **Consistency:** 确保每个生成的 PSD 都遵循相同的遮罩规则。  
- **Cross‑platform:** 在支持 Java 的任何操作系统上运行。  
- **Integration:** 可与其他 Aspose API（如 PSD → PNG 转换）结合，实现端到端工作流。  
- **Scalability:** 矢量遮罩在任何尺寸下都保持清晰，适用于响应式设计。

## Why This Matters for Java Developers
使用 **create vector mask java** 技术，您可以将复杂的图形逻辑直接嵌入后端服务、CI 流水线或桌面工具中。无需设计师手动添加遮罩，代码即可实时生成或调整，节省时间并降低人为错误。

## Prerequisites
在开始编写代码之前，请确保具备以下条件：

### What You Need
- Java Development Kit (JDK)：确保机器上已安装 JDK。如未安装，可从 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) 下载。  
- Aspose.PSD for Java Library：这是一款强大的 PSD 管理库，可从 [Aspose release page](https://releases.aspose.com/psd/java/) 下载。想先试用再购买的用户，也可使用 [free trial](https://releases.aspose.com/)。  
- An IDE：任何 Java IDE（如 IntelliJ IDEA、Eclipse 等）均可用于本项目。

### Setting Up Your Workspace
1. **Create a New Java Project** – 在您喜欢的 IDE 中新建一个项目。  
2. **Add the Aspose Library** – 下载 Aspose JAR 后，将其添加到项目的构建路径，以便访问所有 PSD 相关类。

环境准备就绪后，让我们进入实际实现。

## How to create vector mask in PSD files with Java
下面提供逐步指南。代码块保持原样，仅添加了解释性文字，使每一步更加清晰。

### Import Packages
在处理 PSD 文件之前，需要导入 Aspose.PSD 库中的必要类。

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

现在我们已经做好准备，下面逐步演示每个操作。

### Step 1: Load Your PSD File
首先加载 PSD 文件，一切从这里开始。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- 将 `dataDir` 设置为 PSD 文件所在目录。  
- 使用 `sourceFileName` 字符串将目录与 PSD 文件名拼接。  
- 最后通过 `Image.load()` 将 PSD 加载为 `PsdImage` 对象。

### Step 2: Retrieve the Vmsk Resource
加载完 PSD 后，获取 Vmsk 资源。

```java
VmskResource resource = getVmskResource(im);
```

- 调用 `getVmskResource()` 方法，该方法负责在图像中搜索并返回 Vmsk 资源。

### Step 3: Validate Vmsk Resource Properties
在进行修改之前，先验证 Vmsk 资源的状态是否符合预期。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- 检查 Vmsk 资源的各项属性，确保它未被禁用、未反转、已链接，并且路径数量正确。

### Step 4: Access Each Path and Validate
进一步检查 Vmsk 资源中的路径记录。

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

- 提取三个特定的路径记录，并验证它们的类型和属性是否满足要求。

### Step 5: Edit the Vmsk Resource
进入修改阶段！根据需要调整 Vmsk 资源的属性。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 在此代码块中，我们切换了 Vmsk 资源的多个布尔属性。将它们设为 `true` 可控制遮罩在 PSD 中的行为。

### Step 6: Modify the Bezier Knot Points
贝塞尔结点决定了矢量路径的形状。这里对其进行修改。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 访问特定的 `BezierKnotRecord` 路径，并更改其坐标，以重新塑造矢量遮罩。

### Step 7: Save the Modified PSD File
完成所有编辑后，保存修改后的 PSD 文件。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- 设置导出 PSD 的路径，然后调用 `im.save()` 将更改写入新文件。

### Step 8: Clean Up Resources
最后，确保释放图像资源以防内存泄漏。

```java
im.dispose();
```

- 在完成后始终调用 `dispose()`，这是避免应用程序内存泄漏的良好实践。

## Common Issues and Solutions
| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **`VmskResource` not found** | PSD 中不包含矢量遮罩图层。 | 确认源 PSD 已包含矢量遮罩，或在 Photoshop 中手动添加后再运行代码。 |
| **`ArrayIndexOutOfBoundsException` on path access** | 实际路径记录数量与预期不符。 | 检查 `resource.getPaths().length`，并相应调整索引使用方式。 |
| **License exception** | 未使用有效的 Aspose.PSD 许可证。 | 使用 `License license = new License(); license.setLicense("Aspose.PSD.lic");` 加载试用或正式许可证。 |
| **Memory leak** | 长时间运行的进程未释放 Image 对象。 | 在 `finally` 块中调用 `im.dispose()`，或在支持的情况下使用 try‑with‑resources。 |

## Frequently Asked Questions

**Q: How do I add a new vector mask to an existing layer?**  
A: 创建 `VmskResource`，填充所需的路径记录（如 `BezierKnotRecord`），然后将其添加到图层的 resources 集合中。

**Q: Can I convert the edited PSD directly to PNG without opening Photoshop?**  
A: 可以——保存 PSD 后，使用 `Image.load()` 再次加载，并调用 `im.save("output.png")` 指定 PNG 格式即可。

**Q: Is there a way to automate this in a CI/CD pipeline?**  
A: 完全可以。由于整个过程纯 Java 实现，您可以将其嵌入 Maven/Gradle 构建、Docker 容器或任何支持 Java 的 CI 系统中。

**Q: What versions of Aspose.PSD are compatible with Java 11+?**  
A: 所有近期版本（2024‑2025）均支持 Java 8 及以上，包括 Java 11、17 以及更高的 LTS 版本。

**Q: Do I need a license for development builds?**  
A: 开发和测试阶段可使用免费评估许可证。生产部署则需要商业许可证。

---

**Last Updated:** 2026-02-22  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}