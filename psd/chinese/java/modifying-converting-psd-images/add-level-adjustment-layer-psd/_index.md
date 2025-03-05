---
title: 在 PSD 中添加色阶调整层
linktitle: 在 PSD 中添加色阶调整层
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 在 PSD 文件中有效添加色阶调整层。提升您的图像编辑技能。
type: docs
weight: 16
url: /zh/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## 介绍
在图像编辑方面，管理色阶可以对照片的活力和清晰度产生巨大影响。Photoshop 工具库中的一个方便的工具是“色阶调整层”，它允许您调整图像的色调范围和色彩平衡。在本指南中，我们将引导您了解如何使用 Aspose.PSD for Java 在 PSD 文件中实现色阶调整层。所以，请准备好您的 Java IDE。
## 先决条件
在进入水平调整的世界之前，您需要设置一些东西以确保顺利行驶：
1.  Java 开发工具包 (JDK)：确保您的机器上安装了 JDK。如果没有，可以从[Oracle 网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)或使用 OpenJDK。
2. Aspose.PSD for Java 库：要操作 PSD 文件，您需要下载 Aspose.PSD 库。您可以从此处获取最新版本[下载链接](https://releases.aspose.com/psd/java/)并确保您已将 JAR 包含在项目库中。
3. Java 基础知识：对 Java 编程有基本的了解会有所帮助，因为我们将在本教程中深入研究代码片段。
4. IDE 设置：您可以使用任何您喜欢的 Java IDE（如 IntelliJ IDEA、Eclipse 或 NetBeans）来编写和运行代码。只需确保您已设置 Java 项目并添加了 Aspose.PSD 库。

## 导入包
在开始编写代码之前，我们需要从 Aspose.PSD 库中导入必要的包。具体操作如下：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
通过导入这些包，我们将可以访问加载、修改和保存 PSD 文件所需的类。

现在，让我们将这个过程分解成易于理解的步骤。跟随我们一起了解如何加载 PSD 文件、调整级别，然后保存更改。 
## 步骤 1：设置文件路径
第一步是定义我们的 PSD 文件的位置以及我们想要保存修改后的输出的位置。您可以自定义目录路径以满足您的需要。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
在这里，替换`"Your Document Directory"`与您系统中存储 PSD 文件的实际路径。这为我们接下来要做的一切奠定了基础。
## 步骤2：加载PSD文件
现在，让我们使用`PsdImage`类。这一步至关重要，因为它允许我们访问和操作图层。
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
当你打电话时`Image.load()`，它将读取 PSD 文件并创建一个实例`PsdImage`你可以使用它。
## 步骤 3：遍历各个层
由于我们要调整色阶调整层，因此我们需要循环遍历 PSD 文件中的每个层。这有助于我们找到要修改的特定层。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        //进一步的操作将在这里进行...
    }
}
```
在这个循环中，`instanceof LevelsLayer`检查当前图层是否为色阶调整图层。如果是，我们可以继续调整其属性。
## 步骤 4：调整电平通道设置
一旦我们确定了正确的层，我们就可以修改其输入和输出级别。这就是奇迹发生的地方！调整不同的参数，看看它们如何影响图像。
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
每个参数的作用如下：
- 输入中间色调级别：调整中间色调。
- 输入阴影级别：调整图像较暗的区域。
- 输入高光级别：改变图像的明亮区域。
- 输出阴影级别：设置暗阴影的显示方式。
- 输出高光级别：设置光亮部分的显示方式。
请随意尝试不同的值！
## 步骤5：保存修改后的PSD文件
现在我们已经完成了调整，是时候保存修改后的 PSD 文件了。此步骤至关重要，以确保您的更改得到应用和存储。
```java
im.save(psdPathAfterChange);
```
您现在可以在指定的`psdPathAfterChange`. 
## 结论
您刚刚学会了如何使用 Aspose.PSD for Java 向 PSD 文件添加色阶调整层！按照本指南，您可以轻松调整图像的色调质量，为获得更生动、更具视觉吸引力的输出铺平道路。请记住，熟能生巧，因此请随意调整并探索不同的 PSD 文件以查看更改的效果。
## 常见问题解答
### 什么是色阶调整层？
通过色阶调整层，您可以校正图像中的色调范围，平衡阴影、中间色调和高光。
### 我可以不购买就使用 Aspose.PSD 吗？
是的！Aspose 提供免费试用，供您在购买前测试该库。
### 在哪里可以找到 Aspose.PSD 的文档？
您可以找到文档[这里](https://reference.aspose.com/psd/java/).
### Aspose 产品有社区支持吗？
当然！您可以在[Aspose 论坛](https://forum.aspose.com/c/psd/34).
### 如何获得 Aspose.PSD 的临时许可证？
您可以申请临时驾照[这里](https://purchase.aspose.com/temporary-license/).