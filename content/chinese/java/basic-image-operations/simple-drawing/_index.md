---
title: 使用 Aspose.PSD for Java 执行简单绘图
linktitle: 进行简单绘图
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 在 PSD 文件中绘制形状。本分步指南涵盖了创建、添加图层以及使用代码示例进行绘图的内容。
type: docs
weight: 10
url: /zh/java/basic-image-operations/simple-drawing/
---
## 介绍

欢迎阅读有关使用 Aspose.PSD for Java 执行简单绘图的分步指南！在本教程中，我们将探索创建新 PSD 文档、添加图层以及使用不同颜色绘制形状的基础知识。 Aspose.PSD for Java 是一个功能强大的库，使您能够以编程方式操作 PSD 文件，为图形设计任务提供广泛的功能。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

- 您的计算机上安装了 Java 开发工具包 (JDK)。
-  Java 库的 Aspose.PSD。您可以从[Aspose.PSD for Java 文档](https://reference.aspose.com/psd/java/).

## 导入包

首先，将必要的包导入到您的 Java 项目中。在 Java 文件的开头包含以下代码：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 第 1 步：创建一个新文档

让我们首先创建一个具有指定宽度和高度的新 PSD 文档：

```java
//ExStart:创建文档
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:创建文档
```

## 第 2 步：添加图层

现在，让我们使用无参构造函数向文档添加一个图层：

```java
//ExStart:添加图层
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//结束：添加图层
```

## 第三步：绘制形状

在此步骤中，我们将使用 Graphics 类在创建的图层上绘制形状：

### 画一个黄色的矩形

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd：绘制矩形黄色
```

### 画一个红色矩形

```java
//ExStart：绘制红色矩形
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd：绘制红色矩形
```

### 画一个蓝色矩形

```java
//ExStart：绘制蓝色矩形
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd：绘制蓝色矩形
```

## 第 4 步：保存更改

最后，保存已加载 PSD 文件的副本（包括更改）：

```java
//ExStart:保存更改
image.save(outPsdFilePath);
//ExEnd：保存更改
```

## 结论

恭喜！您已经使用 Aspose.PSD for Java 成功执行了简单的绘图。本教程介绍了创建新文档、添加图层以及绘制不同颜色的矩形。请随意探索该库为您的图形设计需求提供的更多高级功能。

## 常见问题解答

### Q1：我可以使用Aspose.PSD for Java来操作现有的PSD文件吗？

A1：是的，Aspose.PSD for Java 提供了广泛的功能来编辑和操作现有的 PSD 文件。

### Q2：在哪里可以找到 Aspose.PSD for Java 的支持？

 A2：您可以访问[Aspose.PSD for Java 论坛](https://forum.aspose.com/c/psd/34)任何与支持相关的查询。

### Q3：Aspose.PSD for Java 有免费试用版吗？

A3：是的，您可以访问免费试用版。[这里](https://releases.aspose.com/).

### Q4：如何购买 Aspose.PSD for Java 的许可证？

 A4：您可以从[Aspose.PSD购买页面](https://purchase.aspose.com/buy).

### Q5：Aspose.PSD for Java 是否有临时许可证？

A5：是的，您可以从以下机构获得临时许可证：[这里](https://purchase.aspose.com/temporary-license/).