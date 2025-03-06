---
title: 使用 Aspose.PSD for Java 向 PSD 添加新的常规图层
linktitle: 向 PSD 添加新的常规图层
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 向 PSD 文件添加新的常规图层。按照我们的分步指南进行无缝 PSD 操作。
weight: 11
url: /zh/java/advanced-image-effects/add-new-regular-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 向 PSD 添加新的常规图层

## 介绍

欢迎阅读本篇关于使用 Aspose.PSD for Java 向 PSD 文件添加新常规层的综合教程。Aspose.PSD 是一个功能强大的 Java 库，允许开发人员高效地操作和使用 PSD 文件。在本教程中，我们将指导您完成向 PSD 文件添加新常规层的过程，并提供详细的步骤和代码示例。

## 先决条件

在深入学习本教程之前，请确保您已满足以下先决条件：

- Java 开发环境：确保您的系统上已设置 Java 开发环境。
-  Aspose.PSD 库：下载并安装 Aspose.PSD for Java 库。您可以找到库[这里](https://releases.aspose.com/psd/java/).

## 导入包

首先，将必要的包导入到您的 Java 项目中。这些包对于使用 Aspose.PSD 功能至关重要。在 Java 文件的开头包含以下几行：

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 步骤 1：加载 PSD 文件

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

## 步骤3：初始化层数据

使用默认值初始化数据数组：

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## 步骤 4：添加常规图层

向 PSD 图像添加两个常规图层：

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

## 步骤 5：保存 PSD 和 PNG

保存修改后的 PSD 和附加 PNG 文件：

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

恭喜！您已成功使用 Aspose.PSD for Java 向 PSD 文件添加了新的常规图层。

## 结论

在本教程中，我们介绍了使用 Aspose.PSD for Java 向 PSD 文件添加新常规层的过程。这个功能强大的库简化了 PSD 操作，使 Java 开发人员可以访问它。尝试不同的参数和功能，探索 Aspose.PSD 的全部潜力。

## 常见问题解答

### 问题1：Aspose.PSD 与 Java 8 兼容吗？

A1：是的，Aspose.PSD 支持 Java 8 及更高版本。

### 问题 2：我可以对添加的图层应用变换吗？

A2：当然！Aspose.PSD 为图层提供了一系列转换选项。

### 问题 3：在哪里可以找到其他 Aspose.PSD 文档？

 A3：您可以参考文档[这里](https://reference.aspose.com/psd/java/).

### Q4: 如何获取 Aspose.PSD 的临时许可证？

 A4：参观[此链接](https://purchase.aspose.com/temporary-license/)以获得临时许可证选项。

### Q5：有没有Aspose.PSD支持的社区论坛？

 A5：是的，您可以找到支持和讨论[这里](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
