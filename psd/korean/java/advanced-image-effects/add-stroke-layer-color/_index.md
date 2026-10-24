---
date: 2026-10-24
description: Aspose.PSD for Java를 사용하여 Java에서 스트로크 레이어를 만드는 방법을 배웁니다. 이 단계별 가이드는 스트로크
  레이어를 추가하고, 색상을 변경하며, 불투명도를 조정하고, PSD를 저장하는 방법을 보여줍니다.
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: 스트로크 레이어 색상 추가
og_description: Aspose.PSD for Java를 사용하여 Java에서 스트로크 레이어를 만듭니다. 이 간결한 튜토리얼을 따라 스트로크
  레이어를 추가하고, 색상을 변경하며, 불투명도를 조정하고, PSD 파일을 내보내세요.
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: Aspose.PSD와 함께 Java에서 스트로크 레이어 만들기 – 빠른 가이드
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: Aspose.PSD를 사용하여 Java에서 스트로크 레이어를 만드는 방법
url: /ko/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD를 사용하여 Java에서 스트로크 레이어 만들기

## 소개

프로그램matically Photoshop 문서에서 **create stroke layer Java**가 필요하다면, Aspose.PSD for Java는 깔끔하고 코드‑우선 접근 방식을 제공합니다. 이 튜토리얼에서는 새 스트로크 레이어를 추가하고, 색상을 변경하고, 불투명도를 조정하고, 결과를 저장하는 방법을 배웁니다—Photoshop을 실행하지 않고도 가능합니다. 마지막에는 기존 레이어의 스트로크를 편집하는 방법도 알게 되어 Java 애플리케이션에서 직접 전체 창작 제어를 할 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.PSD for Java (latest version).  
- **스트로크 색상을 변경할 수 있나요?** Yes – use `ColorFillSettings` to set any `Color`.  
- **라이선스가 필요합니까?** A temporary license works for evaluation; a full license is required for production.  
- **지원되는 Java 버전은?** Java 8 or higher.  
- **구현에 얼마나 걸립니까?** Typically under 10 minutes for a basic stroke change.

## PSD에서 스트로크 레이어란?
스트로크 레이어는 레이어 내용 주위에 외곽선을 그리는 벡터 효과입니다. 색상, 두께, 불투명도 및 혼합 모드로 맞춤 설정할 수 있습니다. 이 효과를 프로그래밍으로 수정하면 자동 브랜딩, 배치 처리 또는 동적 그래픽 생성이 가능합니다.

## 스트로크 색상 변경에 Aspose.PSD를 사용하는 이유
Aspose.PSD는 **150+** PSD 기능을 지원합니다—벡터 마스크, 스마트 오브젝트, 레이어 효과 등을 포함하며, 전체 문서를 메모리에 로드하지 않고도 수백 페이지 파일을 처리합니다. 라이브러리는 JVM이 설치된 모든 OS에서 실행되며, 일반 자산에 대해 서브초 성능을 제공하고 Photoshop 설치가 필요 없습니다.

## Java에서 스트로크 레이어를 만드는 방법

PSD를 로드하고, 스트로크 효과를 추가하고, 외관을 구성한 뒤 파일을 저장합니다—몇 줄의 간단한 코드로 가능합니다. 아래 답변은 단계별 walkthrough에 들어가기 전에 정확히 해야 할 일을 알려줍니다.

**직접 답변 (40‑70 단어):**  
`PsdImage` represents a PSD document and provides methods to load and save files. Start by loading your PSD with `PsdImage.load("input.psd", loadOptions)`. Create a new `StrokeEffect`, set its `ColorFillSettings` to the desired `Color`, adjust opacity and size, then attach the effect to the target layer’s `BlendingOptions`. Finally, call `psd.save("output.psd", SaveFormat.PSD)`. This sequence creates a stroke layer in Java with Aspose.PSD.

### 사전 요구 사항

- **Aspose.PSD 라이브러리** – download from the [official documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – version 8 or newer.  
- **IDE** – Eclipse, IntelliJ IDEA, or any Java‑compatible editor.

### 패키지 가져오기

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

### 단계 1: 프로젝트 설정

Create a new Java project, add the Aspose.PSD JAR to the build path, and verify the library loads without errors.

### 단계 2: PSD 파일 로드

Enable loading of effect resources so the stroke information is available.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 단계 3: 스트로크 효과 레이어 접근

`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied to a layer. Retrieve the first stroke effect from the second layer (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### 단계 4: 스트로크 속성 검증

`ColorFillSettings` holds the color and opacity values for a stroke. Confirm the existing properties before making changes to avoid unexpected results.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### 단계 5: 색상 및 불투명도 설정 (스트로크 색상 변경 방법)

Here we **change stroke color** to yellow and reduce opacity to 50 % (127 / 255). `ColorFillSettings` also lets you specify blend mode and size.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### 단계 6: 수정된 PSD 저장

Write the updated image back to disk. The new file now contains the modified stroke.

```java
im.save(exportPath);
```

## Java에서 스트로크 색상 변경 방법

`Color` represents an ARGB color value. Load your PSD, locate the target layer, update the `ColorFillSettings` with a new `Color`, and save the file. This operation requires only a few lines of code and completes in under a second for typical assets, making it fast and efficient.

**직접 답변 (40‑70 단어):**  
Use `layer.getEffects().getStrokeEffect()` to obtain the existing stroke, call `stroke.getColorFillSettings().setColor(Color.getRed())` (or any `Color` you need), optionally adjust `setOpacity((byte)200)` for 78 % opacity, then save the PSD with `psd.save("output.psd", SaveFormat.PSD)`. The change is applied instantly without re‑rendering the whole document.

## 스트로크 불투명도 수정 방법

If you only need to adjust the opacity while keeping the original color, change the `setOpacity` value (0‑255) on the `ColorFillSettings`. For example, `colorStroke.setOpacity((byte)200);` will make the stroke roughly 78 % opaque. Adjusting opacity lets you create subtle outlines or fully solid strokes, depending on your design requirements.

**직접 답변 (40‑70 단어):**  
Retrieve the `StrokeEffect` from the desired layer, then call `stroke.getColorFillSettings().setOpacity((byte)desiredValue)`, where `desiredValue` ranges from 0 (transparent) to 255 (fully opaque). Save the PSD and the new opacity is reflected immediately. This approach works for any existing stroke, regardless of its original color.

## 스트로크 효과 적용 방법

To add a new stroke effect to a layer that doesn’t already have one, create a `StrokeEffect` instance, configure its `ColorFillSettings`, and attach it to the layer’s `BlendingOptions`. The same `setColor` and `setOpacity` methods are used to define appearance overall.

**직접 답변 (40‑70 단어):**  
Instantiate `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`. After attaching the effect, save the PSD. This adds a fresh, fully‑customizable stroke layer to any existing layer in your document.

## 스트로크 색상 변경의 일반적인 사용 사례
- **브랜딩 자동화:** 단일 배치 실행으로 수백 개의 PSD 자산에 있는 로고에 기업 색상을 적용합니다.  
- **동적 UI 생성:** 웹 기반 디자인 도구에서 사용자가 선택한 테마에 따라 스트로크 색상을 실시간으로 변경합니다.  
- **프리플라이트 준비:** 파일을 인쇄소에 보내기 전에 모든 스트로크 색상이 인쇄 사양을 충족하는지 확인합니다.

## 일반적인 함정 및 팁

- **Null 체크** – always verify that `getEffects()` returns a non‑null array before casting.  
- **레이어 인덱스** – PSD 레이어는 0부터 시작하므로 올바른 레이어를 대상으로 하는지 확인하세요.  
- **색상 형식** – `Color.getYellow()`는 예시일 뿐이며 `new Color(r, g, b)`로 사용자 정의 색상을 만들 수 있습니다.  
- **불투명도 범위** – opacity는 바이트(0–255)이며 255를 초과하는 값은 클램프됩니다.  
- **리소스 로드** – `loadOptions.setLoadEffectsResource(true)`를 잊으면 `null` 효과 배열이 발생합니다.

## 자주 묻는 질문

**Q: Aspose.PSD를 다른 Java 그래픽 라이브러리와 함께 사용할 수 있나요?**  
A: Yes, Aspose.PSD can be combined with libraries such as Apache Commons Imaging or Java2D for extended functionality.

**Q: Aspose.PSD가 최신 PSD 파일 형식과 호환되나요?**  
A: Absolutely. The library supports the newest Photoshop specifications and over 150 PSD features.

**Q: Aspose.PSD 사용 중 예외를 어떻게 처리하나요?**  
A: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34) for detailed troubleshooting examples.

**Q: 구매 전에 Aspose.PSD를 체험할 수 있나요?**  
A: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore all features.

**Q: Aspose.PSD의 임시 라이선스는 어디서 얻을 수 있나요?**  
A: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/) to evaluate the library in your development environment.

**Last Updated:** 2026-10-24  
**Tested with:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## 관련 튜토리얼

- [Java에서 Aspose.PSD를 사용하여 스트로크 색상 변경 방법](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [Java를 사용하여 PSD에 그림자 추가 – 고급 레이어 효과](/psd/java/advanced-psd-layer-features-effects/)
- [Pattern Overlay PSD: Aspose.PSD for Java로 효과 추가](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}