---
date: 2025-11-30
description: Aspose.PSD for Java를 사용하여 스트로크를 추가하고 PSD 스트로크 색상을 변경하는 방법을 배워보세요. 이 단계별
  가이드를 따라 스트로크 레이어 색상과 불투명도를 수정하세요.
language: ko
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java에서 스트로크 레이어 색상 추가 방법
url: /java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java에서 스트로크 레이어 색상 추가하는 방법

## Introduction

프로그램matically 포토샵 문서에 **how to add stroke** 를 추가해야 한다면, Aspose.PSD for Java가 이를 간단하게 만들어 줍니다. 이 튜토리얼에서는 스트로크 레이어 색상을 추가하고, 불투명도를 조정한 뒤 결과를 저장하는 과정을 단계별로 안내합니다. 마지막에는 **how to change stroke color** (또는 *change PSD stroke color*) 를 사용하여 기존 레이어의 스트로크 색상을 변경하는 방법도 확인할 수 있어, Java 코드만으로 완전한 창의적 제어가 가능합니다.

## Quick Answers
- **What library is required?** Aspose.PSD for Java (latest version).  
- **Can I change the stroke color?** Yes – use `ColorFillSettings` to set any `Color`.  
- **Do I need a license?** A temporary license works for evaluation; a full license is required for production.  
- **Which Java version is supported?** Java 8 or higher.  
- **How long does the implementation take?** Typically under 10 minutes for a basic stroke change.

## What is a Stroke Layer in a PSD?
스트로크 레이어는 레이어 내용 주위에 외곽선을 그리는 벡터 효과입니다. 색상, 두께, 불투명도 및 블렌드 모드로 사용자 정의할 수 있습니다. 이 효과를 프로그래밍으로 수정하면 자동 브랜딩, 일괄 처리 또는 동적 그래픽 생성이 가능해집니다.

## Why Use Aspose.PSD to Change Stroke Color?
- **No Photoshop required** – work entirely in Java.  
- **Full PSD spec compliance** – all modern PSD features are supported.  
- **High performance** – process large files quickly.  
- **Cross‑platform** – run on any OS with a JVM.

## Prerequisites

- **Aspose.PSD Library** – download from the [official documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – version 8 or newer.  
- **IDE** – Eclipse, IntelliJ IDEA, or any Java‑compatible editor.

## Import Packages

First, import the classes you’ll need. This gives your project access to the PSD handling and stroke‑effect APIs.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Step 1: Set Up Your Project

Create a new Java project, add the Aspose.PSD JAR to the build path, and verify the library loads without errors.

## Step 2: Load the PSD File

Enable loading of effect resources so the stroke information is available.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 3: Access the Stroke Effect Layer

Retrieve the first stroke effect from the second layer (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Step 4: Validate Stroke Properties

Confirm the existing properties before making changes. This helps avoid unexpected results.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Step 5: Set Color and Opacity (How to Change Stroke Color)

Here we **change PSD stroke color** to yellow and reduce opacity to 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Step 6: Save the Modified PSD

Write the updated image back to disk. The new file now contains the modified stroke.

```java
im.save(exportPath);
```

## Common Pitfalls & Tips

- **Null checks** – always verify that `getEffects()` returns a non‑null array before casting.  
- **Layer index** – PSD layers are zero‑based; ensure you target the correct layer.  
- **Color format** – `Color.getYellow()` is just an example; you can create custom colors with `new Color(r, g, b)`.  
- **Opacity range** – opacity is a byte (0–255); values above 255 will be clamped.

## Conclusion

You’ve now learned **how to add stroke** to a PSD file and **how to change stroke color** using Aspose.PSD for Java. Experiment with different colors, blend modes, and opacities to achieve the exact visual style your project needs.

## Frequently Asked Questions

**Q: Can I use Aspose.PSD with other Java graphic libraries?**  
A: Yes, Aspose.PSD can be combined with libraries such as Apache Commons Imaging or Java2D for extended functionality.

**Q: Is Aspose.PSD compatible with the latest PSD file format?**  
A: Absolutely. The library is regularly updated to support the newest Photoshop specifications.

**Q: How do I handle exceptions while using Aspose.PSD?**  
A: Refer to the [support forum](https://forum.aspose.com/c/psd/34) for detailed troubleshooting and sample error‑handling code.

**Q: Can I try Aspose.PSD before purchasing?**  
A: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore all features.

**Q: Where can I get a temporary license for Aspose.PSD?**  
A: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/) to evaluate the library in your development environment.

---

**Last Updated:** 2025-11-30  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
