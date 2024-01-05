---
title: 使用 Aspose.PSD for Java 添加新的常规图层到 PSD
linktitle: 向 PSD 添加新的常规图层
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 向 PSD 文件添加新的常规图层。按照我们的分步指南进行无缝 PSD 操作。
type: docs
weight: 11
url: /zh/java/advanced-image-effects/add-new-regular-layer/
---
## 介绍

欢迎来到这个关于使用 Aspose.PSD for Java 向 PSD 文件添加新的常规图层的综合教程。 Aspose.PSD 是一个功能强大的 Java 库，允许开发人员有效地操作和使用 PSD 文件。在本教程中，我们将指导您完成向 PSD 文件添加新的常规图层的过程，并提供详细的步骤和代码示例。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

- Java 开发环境：确保您的系统上设置了 Java 开发环境。
-  Aspose.PSD 库：下载并安装 Aspose.PSD for Java 库。你可以找到图书馆[这里](https://releases.aspose.com/psd/java/).

## 导入包

首先，将必要的包导入到您的 Java 项目中。这些包对于使用 Aspose.PSD 功能至关重要。在 Java 文件的开头包含以下行：

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 第 1 步：加载 PSD 文件

使用以下代码加载要编辑的 PSD 文件：

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 第 2 步：准备数据数组和矩形

准备两个 int 数组和两个 Rectangle 对象，如下所示：

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## 第三步：初始化图层数据

使用默认值初始化数据数组：

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## 第四步：添加常规图层

将两个常规图层添加到 PSD 图像：

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## 第5步：保存PSD和PNG

保存修改后的 PSD 和附加 PNG 文件：

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

恭喜！您已使用 Aspose.PSD for Java 成功将新的常规图层添加到 PSD 文件中。

## 结论

在本教程中，我们介绍了使用 Aspose.PSD for Java 向 PSD 文件添加新的常规图层的过程。这个强大的库简化了 PSD 操作，使其可供 Java 开发人员使用。尝试不同的参数和功能，探索 Aspose.PSD 的全部潜力。

## 常见问题解答

### Q1：Aspose.PSD 与 Java 8 兼容吗？

A1：是的，Aspose.PSD 支持 Java 8 及更高版本。

### Q2：我可以对添加的图层应用变换吗？

A2：当然！ Aspose.PSD 提供了一系列图层转换选项。

### Q3：在哪里可以找到额外的 Aspose.PSD 文档？

 A3：可以参考文档[这里](https://reference.aspose.com/psd/java/).

### Q4：如何获得Aspose.PSD的临时许可证？

 A4：参观[这个链接](https://purchase.aspose.com/temporary-license/)用于临时许可证选项。

### Q5：是否有支持 Aspose.PSD 的社区论坛？

 A5：是的，您可以找到支持和讨论[这里](https://forum.aspose.com/c/psd/34).