---
title: 支持 PSD 中的长度记录数据属性 - Java
linktitle: 支持 PSD 中的长度记录数据属性 - Java
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD 在 Java 中操作具有长度记录数据属性的 PSD 文件。请按照此分步指南了解所有详细信息。
type: docs
weight: 14
url: /zh/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
---
## 介绍
您是否曾经使用过 Photoshop 文件并希望以编程方式操作图层或形状？如果是这样，那么您就发现了 Aspose.PSD for Java 库的美妙之处。这个强大的工具允许开发人员通过 Java 代码无缝地与 PSD 文件交互和修改 PSD 文件。在今天的文章中，我们将深入探讨如何使用此库在 PSD 文件中支持长度记录数据属性。 
无论您是经验丰富的 Java 开发人员还是刚刚入门，本指南都会逐步引导您了解所有需要了解的内容。最后，您将能够打开 PSD 文件、修改其矢量形状属性并保存更改 - 所有这些都无需离开舒适的 Java 环境。让我们撸起袖子开始行动吧！
## 先决条件
在我们开始之前，您需要准备一些东西。确保一切准备就绪可使流程更加顺利，而且没人喜欢最后一刻手忙脚乱！以下是您需要准备的东西：
1.  Java 开发工具包 (JDK)：确保您的机器上安装了 JDK。您可以从此处下载[Oracle 网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)或者使用包管理器。
2.  Aspose.PSD for Java 库：您需要下载 Aspose.PSD for Java 库并将其包含在您的项目中。从[Aspose 发布页面](https://releases.aspose.com/psd/java/).
3. IDE：使用集成开发环境 (IDE)，如 IntelliJ IDEA、Eclipse 或您选择的任何 Java IDE，以更好地处理代码。
4. PSD 文件：本教程需要 PSD 文件。您可以在 Adobe Photoshop 中创建一个 PSD 文件，也可以下载示例 PSD 文件。
5. 基本 Java 知识：熟悉 Java 语法将帮助您轻松地跟进。
## 导入包
现在您已设置好所有先决条件，下一步是导入必要的包。此步骤对于访问我们将要使用的类和方法至关重要。以下是如何在 Java 项目中导入所需包的示例：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```
通过这些导入，您就可以开始处理 PSD 文件了！

## 步骤 1：设置源目录和输出目录
在加载任何文件之前，让我们指定输入的 PSD 文件的来源以及我们想要保存修改后的文件的位置。根据您的本地机器调整目录路径。
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```
## 步骤2：加载PSD文件
是时候加载 PSD 文件了！为此，我们将使用`Image.load`来自 Aspose.PSD 库的方法。此方法允许我们打开 PSD 文件并访问其图层和资源。
```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```
这就像打开一本书——您可以浏览它的页面（图层和资源）。
## 步骤 3：在层中找到 Vsms 资源
接下来，我们需要在 PSD 文件中找到特定的 VsmsResource。这些资源保存矢量形状图层的数据。这就是奇迹发生的地方！在此代码片段中，我们循环遍历图层的资源以找到此资源。
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```
就像寻宝一样，您正在层层搜索以找到有价值的矢量数据！
## 步骤 4：访问长度记录
一旦我们有了 VsmsResource，我们就可以提取 LengthRecord 对象。每个 LengthRecord 代表矢量形状内的一条路径。在这里，我们访问三个 LengthRecord 来操作它们的属性。
```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```
这就像选择想要修饰绘画的哪些部分一样！
## 步骤5：修改路径操作属性
现在到了最有趣的部分——修改路径属性！在这里，setPathOperations 方法允许更改形状之间的交互方式。我们可以设置诸如排除重叠区域或从后面减去前面形状之类的操作。
```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```
将其想象成调整蛋糕的层数——根据切片方式，每一层都会有不同的互动方式！
## 步骤6：保存修改后的PSD文件
完成必要的更改后，下一步是保存修改后的 PSD 文件。这是您所有辛勤工作的回报。 
```java
psdImage.save(outPsdFilePath);
```
您的杰作现已整齐地包装起来，供全世界观看！
## 步骤 7：清理资源
最后，处理已使用的对象以释放内存和资源至关重要。
```java
psdImage.dispose();
```
可以将其想象为在完成艺术项目后清理工作空间 - 确保一切都整洁干净！
## 结论
就是这样！您刚刚完成了使用 Aspose.PSD for Java 支持 PSD 文件中的长度记录数据属性的全面教程。从加载文件到修改形状属性并保存最终产品 - 每个步骤都揭示了这个库的强大功能。无论您是在从事创意项目还是自动化图形资产，Aspose.PSD 都能为您打开一个全新的可能性世界。准备好开始了吗？深入研究您的 PSD 文件并释放您的创造力！
## 常见问题解答
### 什么是 Aspose.PSD for Java？
Aspose.PSD for Java 是一个库，允许开发人员使用 Java 以编程方式操作和使用 Photoshop PSD 文件。
### 我可以在免费项目中使用 Aspose.PSD 吗？
是的，您可以使用 Aspose 网站上提供的试用版免费试用该库。
### 我可以对 PSD 文件进行哪些类型的修改？
您可以操作 PSD 文件中的图层、形状、文本、路径操作等。
### Aspose.PSD 与其他编程语言兼容吗？
是的，Aspose 为不同的编程语言提供各种库，包括.NET 和 Python。
### 在哪里可以找到 Aspose.PSD 的文档？
您可以访问完整文档[这里](https://reference.aspose.com/psd/java/).