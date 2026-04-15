---
date: 2026-03-26
description: Aspose.PSD for Java를 사용하여 텍스트 레이어 PSD 파일을 편집하고 텍스트 색상을 변경하는 방법을 배워보세요.
  개발자와 디자이너를 위한 단계별 가이드.
linktitle: Edit Text Layers PSD Files using Java
second_title: Aspose.PSD Java API
title: Java를 사용하여 PSD 파일의 텍스트 레이어 편집 – Aspose.PSD 튜토리얼
url: /ko/java/psd-image-modification-conversion/format-text-portions-psd-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Edit Text Layers PSD Files Using Java

## Introduction

우리의 시각적인 세상이 점점 더 중요해지는 오늘날, **edit text layers PSD** 파일을 프로그래밍 방식으로 편집할 수 있다면 수작업 시간을 크게 절감할 수 있습니다. 배치로 그래픽을 업데이트해야 하는 디자이너이든, 동적 이미지 생성 서비스를 구축하는 개발자이든, Aspose.PSD for Java를 사용하면 Photoshop에서와 동일하게 PSD 텍스트를 코드로 수정할 수 있습니다. 이번 튜토리얼에서는 텍스트 레이어 PSD 파일을 편집하는 전체 과정을 단계별로 살펴보며, 개별 텍스트 부분에 대해 **change text color PSD** 하는 방법도 다룹니다.

## Quick Answers
- **What library lets you edit text layers PSD?** Aspose.PSD for Java  
- **Can you change text color PSD programmatically?** Yes, using `ITextStyle.setFillColor`  
- **Do I need a license for production?** A commercial license is required; a free trial is available.  
- **Which Java version is supported?** Java 8 and later.  
- **Is memory management required?** Yes—dispose of the `PsdImage` after saving.

## What is edit text layers PSD?

Editing text layers PSD는 Photoshop PSD 파일 내부에 저장된 텍스트 데이터를 접근하여 문자, 스타일 또는 서식을 수정하고, 그 변경 사항을 파일에 다시 기록하는 작업을 의미합니다. 이 기능은 브랜드 업데이트 자동화, 현지화된 그래픽 제작, 또는 수작업 Photoshop 작업 없이 개인화된 마케팅 자산을 생성하는 데 필수적입니다.

## Why edit text layers PSD with Aspose.PSD?

- **Full control** – Change fonts, colors, justification, and even add or remove text portions.  
- **Cross‑platform** – Works on any OS that supports Java.  
- **No Photoshop required** – Perform batch operations on a server or CI pipeline.  
- **High fidelity** – Preserve layer effects, masks, and other PSD features.

## Prerequisites

Before we jump into coding, make sure you have the following:

1. **Java Development Kit (JDK)** – Java 8+ installed and configured.  
2. **Aspose.PSD for Java Library** – Download it from [here](https://releases.aspose.com/psd/java/) or start with a [free trial](https://releases.aspose.com/).  
3. **IDE for Java Development** – IntelliJ IDEA, Eclipse, or NetBeans, with the Aspose.PSD JAR added to your project’s classpath.  
4. **Basic Knowledge of Java** – Familiarity with objects, loops, and exception handling.

## Importing Necessary Packages

When using Aspose.PSD for Java, you'll need to import specific packages to access the classes and methods you'll use. Let's check them out:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.fileformats.psd.layers.text.ITextPortion;
import com.aspose.psd.fileformats.psd.layers.text.ITextStyle;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.internal.Exceptions.Exception;
```

These imports give you access to the essential functionalities of Aspose.PSD that we'll require in our example.

## Step 1: Define Your Directories

Before we start working with the PSD file, we need to define where our source PSD file is located and where we want to save the modified file.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "ThreeColorsParagraphs.psd";
String outPsdFilePath = outputDir + "ThreeColorsParagraph_out.psd";
```

Replace the placeholder paths with the actual locations on your machine.

## Step 2: Load the PSD File

The next step is to load the PSD file you want to work with. Aspose makes this super simple.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

`Image.load` opens the file so we can start inspecting its layers.

## Step 3: Loop Through the Layers

Once the PSD file is loaded, it’s time to dig into its layers. Not all layers contain text, and we want to find only the text layers. Let's filter them out:

```java
for (Layer layer : psdImage.getLayers()) {
    if (!(layer instanceof TextLayer)) {
        continue;
    }
    // Process only text layers…
}
```

The loop iterates over every layer, and we skip any that aren’t instances of `TextLayer`.

## Step 4: Access Text Portions

After we identify a text layer, we can access its text portions for editing. This is where the magic begins!

```java
TextLayer textLayer = (TextLayer) layer;
ITextPortion[] portions = textLayer.getTextData().getItems();
```

Think of text portions as the individual words or sentences that you can edit independently.

## Step 5: Modify Text Portions

Now, let’s edit the text. We’ll change existing text, remove some portions, and even add new text:

```java
portions[0].setText("Hello ");
portions[1].setText("World");
// Removing text portions
textLayer.getTextData().removePortion(3);
textLayer.getTextData().removePortion(2);
// Adding new text portion
ITextPortion createdPortion = textLayer.getTextData().producePortion();
createdPortion.setText("!!!\r");
textLayer.getTextData().addPortion(createdPortion);
```

You can see how straightforward it is to rewrite or delete parts of the paragraph.

## Step 6: Justify and Style Text

After modifying the text, we may want to adjust the styling. Are you ready for a make‑over? Let's adjust text justification and colors:

```java
// Set right justification
portions[0].getParagraph().setJustification(1); // Right
portions[1].getParagraph().setJustification(1);
portions[2].getParagraph().setJustification(1);

// Set fill colors individually
portions[0].getStyle().setFillColor(Color.getAquamarine());
portions[1].getStyle().setFillColor(Color.getViolet());
portions[2].getStyle().setFillColor(Color.getLightBlue());
```

Here we **change text color PSD** for each portion by setting a different `fillColor`. This gives each word its own visual identity.

## Step 7: Update Layer Data

After making all those changes, we need to ensure those changes are reflected in the layer data:

```java
textLayer.getTextData().updateLayerData();
```

This call commits the modifications back to the underlying PSD structure.

## Step 8: Save the Modified PSD File

Finally, let’s save the changes we made to the PSD file:

```java
psdImage.save(outPsdFilePath, new PsdOptions(psdImage));
```

Specify the output path where you want the edited file to be written.

## Step 9: Dispose of Resources

To keep memory usage low, always dispose of the image resources when you’re finished:

```java
finally {
    psdImage.dispose();
}
```

Cleaning up prevents memory leaks, especially when processing many files in a batch.

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **NullPointerException on `portions[2]`** | The source PSD has fewer than three portions. | Verify the number of portions with `portions.length` before accessing indexes. |
| **Colors not applied** | Using an outdated Aspose.PSD version. | Upgrade to the latest Aspose.PSD for Java release. |
| **File not found** | Incorrect path in `sourceDir` or `outputDir`. | Use absolute paths or double‑check relative paths. |
| **License not set** | Trial version may add watermarks. | Apply a valid license with `License license = new License(); license.setLicense("Aspose.PSD.lic");` |

## Frequently Asked Questions

### What is Aspose.PSD for Java?
Aspose.PSD for Java is a library that allows developers to manipulate and work with Photoshop PSD files programmatically.

### Can I use Aspose.PSD for free?
Yes, you can start with a free trial available on the Aspose website before deciding to purchase.

### What prerequisites do I need?
You need the Java Development Kit (JDK) installed, the Aspose.PSD library, and basic knowledge of Java programming.

### Are there any limitations with the free trial?
Yes, the free trial may have certain limitations regarding the features available, such as watermarking or limited usage.

### Where can I find more information about Aspose.PSD?
You can check the documentation for detailed usage scenarios and API references [here](https://reference.aspose.com/psd/java/).

---

**Last Updated:** 2026-03-26  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}