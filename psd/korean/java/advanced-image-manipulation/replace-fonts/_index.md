---
date: 2026-06-23
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 저장하고, 누락된 글꼴을 교체하며, 이미지를 내보내는 방법을
  배웁니다 – 누락된 글꼴이 포함된 PSD 파일을 빠르게 처리합니다.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: 글꼴 교체
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose를 사용하여 Java에서 PSD를 PNG로 저장하고 누락된 글꼴을 교체하는 방법
url: /ko/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 PNG로 저장 – Java에서 누락된 글꼴 교체

## 소개

Photoshop(PSD) 파일 내부에서 누락되었거나 원하지 않는 글꼴을 교체하면서 **save PSD as PNG**해야 한다면, Aspose PSD 글꼴 대체 기능이 손쉽게 해결해 줍니다. Java 애플리케이션에서는 PSD를 로드하고 Aspose에 대체 글꼴을 지정한 뒤 원하는 형식으로 수정된 이미지를 내보낼 수 있습니다. 이 튜토리얼은 프로젝트 설정부터 업데이트된 PNG 내보내기까지 전체 워크플로우를 단계별로 안내하므로, Photoshop을 전혀 열지 않고도 **handle missing fonts PSD** 상황을 안정적으로 처리할 수 있습니다.

## 빠른 답변
- **글꼴 대체를 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java  
- **구현에 얼마나 걸리나요?** About 5‑10 minutes for a basic scenario  
- **기본 대체 글꼴로 어떤 글꼴이 사용되나요?** You can set any TrueType font, e.g., “Arial”  
- **PNG 외의 형식으로 저장할 수 있나요?** Yes – PSD, JPEG, BMP, and more are supported  
- **프로덕션에 라이선스가 필요합니까?** A valid Aspose.PSD license is required for non‑trial use  

## Aspose PSD 글꼴 대체란 무엇인가요?

Aspose PSD 글꼴 대체는 라이브러리가 PSD 파일에서 누락되었거나 지원되지 않는 글꼴을 만나면 대체 글꼴을 지정하는 과정입니다. 이를 통해 Photoshop에서 수동 편집 없이 텍스트 레이어가 올바르게 렌더링되며 **handle missing fonts PSD** 파일을 자동으로 처리할 수 있습니다.

## 왜 Java용 Aspose.PSD를 사용하나요?

Aspose.PSD for Java는 Java 코드에서 직접 Photoshop 파일을 작업할 수 있는 포괄적이고 고성능의 솔루션을 제공하여 Photoshop 자체가 필요 없게 합니다. 다양한 레이어 유형, 효과 및 대용량 파일을 지원하며 글꼴 대체, 이미지 변환, 메타데이터 처리와 같은 작업을 위한 간단한 API를 제공합니다.

- **Full‑featured PSD handling** – Aspose.PSD supports **30+ layer types**, **20+ effects**, and can process files up to **2 GB** without loading the entire document into memory.  
- **Cross‑platform** – works on any OS that supports Java 8+.  
- **No external dependencies** – the library handles font substitution internally, so you don’t need to ship extra fonts with your app.  

## Aspose PSD를 사용하여 PSD에서 누락된 글꼴 교체하는 방법

누락된 글꼴을 교체하려면 먼저 로드 옵션에 정의된 대체 글꼴을 사용해 PSD를 로드한 다음 이미지를 렌더링하거나 저장합니다. 라이브러리는 지정한 글꼴로 누락된 글꼴을 자동으로 대체하여 수동 편집 없이도 시각적 출력이 기대에 부합하도록 합니다.

## 전제 조건

- **Java Development Kit (JDK)** – version 8 or higher installed.  
- **Aspose.PSD for Java** – download the latest JAR from the [release page](https://releases.aspose.com/psd/java/).  
- **An IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.  

## 패키지 가져오기

The `PsdImage` class represents a Photoshop document in memory, providing access to layers, text, and rendering capabilities. `PsdLoadOptions` controls how the file is read, including the fallback font, while `SaveOptions` (or format‑specific subclasses) define how the image is written.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: 문서 디렉터리 설정

Specify the folder that contains the source PSD file. Replace the placeholder with the actual path on your machine.

The `File` object simply points to the PSD you want to process; no additional configuration is required here.  

```java
String dataDir = "Your Document Directory";
```

## 2단계: 교체 글꼴로 이미지 로드

Create a `PsdLoadOptions` instance, set the default replacement font (e.g., **Arial**), and load the PSD. Aspose will automatically apply the fallback whenever it encounters a missing font.

`PsdLoadOptions` lets you define loading behavior, including the fallback font that substitutes any missing typeface during the import phase.  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## 3단계: 교체된 이미지를 PNG로 저장

After the font substitution, you can export the image in any supported format. Here we save it as PNG, but you could also choose JPEG, BMP, or even write it back to PSD.

The `save` method of `PsdImage` accepts a `SaveOptions` object; using `PngOptions` ensures the output is a loss‑less PNG suitable for web or further processing.  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## 글꼴을 교체한 후 PSD를 PNG로 저장하려면 어떻게 해야 하나요?

Load the PSD with a fallback font, then call `psdImage.save("output.png", new PngOptions())`. This single‑line save operation writes a fully rendered PNG that reflects the substituted typeface, letting you embed the image anywhere without worrying about missing fonts. Ensure you have applied the replacement font before saving, and optionally adjust PNG compression settings via the `PngOptions` object for optimal file size.

## 일반적인 문제와 해결책

| 문제 | 원인 | 해결책 |
|-------|-------|-----|
| 텍스트가 교체 후 깨져 보임 | The fallback font does not contain required glyphs | Choose a font that supports the needed Unicode range (e.g., “Arial Unicode MS”). |
| `OutOfMemoryError` on large PSDs | Loading a very high‑resolution file without enough heap | Increase JVM heap size (`-Xmx2g`) or load the image in a streaming mode if available. |
| License exception | Using the trial version in production | Apply a valid permanent or temporary license before loading the image. |

## 자주 묻는 질문

**Q: Can I replace fonts in other image formats besides PSD?**  
A: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG, JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.

**Q: Is the default replacement font mandatory?**  
A: No. You can set any TrueType font you prefer, or omit the setting to let Aspose use its internal default.

**Q: Are there licensing requirements for using Aspose.PSD?**  
A: A commercial license is required for production deployments. See the [purchase page](https://purchase.aspose.com/buy) for details.

**Q: Can I obtain a temporary license for testing?**  
A: Absolutely. Aspose offers free temporary licenses for evaluation – visit the [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Where can I find additional support or discuss Aspose.PSD‑related issues?**  
A: The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: How do I handle PSD files that contain multiple missing fonts?**  
A: Set the default replacement font once (as shown) – it will be applied to *all* missing fonts during the load operation.

**Q: Is it possible to replace fonts after the image has been saved?**  
A: Font substitution must occur during the load phase. To change fonts later, reload the PSD with a different replacement font and resave.

## 결론

You’ve now seen a complete **save psd as png** workflow in Java—from importing the right classes, configuring a fallback font, loading the PSD, to exporting the corrected PNG. Incorporate this pattern into your image‑processing pipelines to ensure consistent typography across all your PSD assets and to **handle missing fonts PSD** automatically.

---

**마지막 업데이트:** 2026-06-23  
**테스트 환경:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.PSD for Java에서 누락된 글꼴 교체 설정](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Aspose.PSD for Java에서 PSD를 PNG로 저장하고 렌더링 드롭 섀도우 적용](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java를 사용해 PSD를 PNG로 변환하고 비율에 맞게 크기 조정하는 방법](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}