---
title: PSD 文件中的渲染级别调整层 - Java
linktitle: PSD 文件中的渲染级别调整层 - Java
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 轻松增强图像对比度和鲜艳度。通过本分步指南掌握色阶调整图层。
weight: 17
url: /zh/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD 文件中的渲染级别调整层 - Java

## 介绍

您是否曾经打开 PSD 文件却发现图像缺乏对比度或活力？图像编辑勇士们，别担心！Aspose.PSD for Java 凭借其强大的色阶调整层操作功能为您解忧。本指南将为您提供使用色阶轻松微调图像的知识。 

## 先决条件

- Java 开发工具包 (JDK)：确保您的系统上安装了最新版本的 JDK。您可以从 Oracle 网站 ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)）。
- Aspose.PSD for Java 库：从下载页面 ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/))。您需要有效的许可证才能使用全部功能，但可以免费试用以帮助您入门（[https://releases.aspose.com/](https://releases.aspose.com/)）。

## 导入包

在深入研究代码之前，我们需要导入必要的 Aspose.PSD 类来与 PSD 文件交互。以下是您需要的内容：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

这`com.aspose.psd`软件包提供了对 PSD 操作功能的访问，同时`com.aspose.psd.imaging.PngOptions`允许我们在将图像保存为 PNG 时定义选项。

现在，让我们开始我们的级别调整冒险：

## 步骤1：设置文件路径：

- 为文档目录定义变量 (`dataDir`)、源 PSD 文件名（`sourceFileName`)、修改后的目标PSD文件名（`psdPathAfterChange`）以及最终的 PNG 导出路径（`pngExportPath`）。考虑使用描述性名称来提高代码的可读性。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## 步骤2：加载PSD图像：

- 使用`Image.load`方法打开源 PSD 文件并将其存储在`PsdImage`目的 （`im`）。Aspose.PSD 自动检测文件格式。

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 步骤 3：遍历各层：

- 我们需要在您的 PSD 中找到色阶调整层。Aspose 提供了一种使用循环遍历所有层的便捷方法。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ...（检查 Levels Layer 的代码将添加在此处）
}
```

## 步骤4：识别级别层：

- 在循环中，检查当前层（`im.getLayers()[i]` ）是`LevelsLayer`使用类`instanceof`操作员。 
- 如果是，则将图层投射到`LevelsLayer`对象以进行进一步的操作。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ...（调整级别的代码将添加到这里）
   }
}
```
## 步骤 5：微调级别（续）：

- 使用调整输出电平`setOutputShadowLevel`和`setOutputHighlightLevel`控制生成图像的暗度和亮度。这些值决定了将映射到输出范围的输入级别的范围。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   //调整输入级别（0-255）：
	   channel.setInputShadowLevel((short) 10); //稍微加深阴影
	   channel.setInputMidtoneLevel(2.0f);     //增加中间色调
	   channel.setInputHighlightLevel((short) 230); //减少高光

	   //调整输出级别（0-255）：
	   channel.setOutputShadowLevel((short) 20); //进一步加深阴影
	   channel.setOutputHighlightLevel((short) 200); //提亮亮点
   }
}
```

## 步骤6：保存修改后的PSD：

- 使用`save`方法`PsdImage`对象将修改后的图像保存到指定路径（`psdPathAfterChange`）。

```java
im.save(psdPathAfterChange);
```

## 步骤 7：导出为 PNG（可选）：

- 如果需要调整后图片的 PNG 版本，请创建`PngOptions`对象并将颜色类型设置为`TruecolorWithAlpha`。然后，使用`save`使用 PNG 导出路径和选项再次使用该方法。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

就这样！您已成功使用 Aspose.PSD for Java 调整了 PSD 文件中的色阶调整层。通过了解这些步骤并尝试不同的值，您可以增强图像的对比度和整体外观。

## 结论

Aspose.PSD for Java 让您能够控制图像编辑过程。通过掌握色阶调整层，您可以为照片和设计注入新的活力。请记住，熟能生巧，所以不要犹豫，尝试并探索这个强大工具的全部潜力。
 
## 常见问题解答

### 我可以分别调整各个颜色通道（RGB）吗？ 
是的，您可以使用`getChannel`方法`LevelsLayer`对象并独立修改其级别。

### 如何处理 PSD 中的多个色阶调整层？
代码会遍历所有层，因此它将自动处理图像中发现的任何其他 Levels 层。

### 除了色阶之外，还有其他方法可以调整图像对比度吗？
当然！Aspose.PSD 提供各种图像调整工具，如曲线、亮度/对比度等。

### 我可以对多幅图像自动执行这一过程吗？ 
是的，您可以将此代码合并到循环或批处理脚本中，以有效地处理多个 PSD 文件。

### 在哪里可以找到更多信息和支持？
Aspose 提供了广泛的文档（[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)）和支持论坛（[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) 以解决您可能遇到的任何问题。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
