---
date: 2026-01-09
description: Aspose.PSD를 사용하여 Java에서 PSD를 PNG로 변환하고 PSD 파일을 자르는 방법을 배워보세요. 정밀한 이미지
  조작을 쉽게 할 수 있습니다.
linktitle: Crop PSD File
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 자르기
url: /ko/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 PNG로 변환하고 PSD 파일 자르기

## Introduction

이미지를 원하는 정확한 영역으로 잘라내면서 **PSD를 PNG로 변환**해야 할 경우, Aspose.PSD for Java는 깔끔하고 프로그래밍 방식으로 이를 수행할 수 있는 방법을 제공합니다. 이 튜토리얼에서는 프로젝트 설정부터 잘라낸 PSD와 PNG 파일을 저장하는 전체 과정을 단계별로 안내하므로, Java 애플리케이션 어디에서든 정밀한 이미지 조작을 통합할 수 있습니다.

## Quick Answers
- **Can Aspose.PSD convert PSD to PNG?** Yes, it supports direct conversion with full layer fidelity.  
- **Do I need a license for cropping?** A free trial works for development; a license is required for production.  
- **What Java version is required?** Java 8 or higher is recommended.  
- **Will the PNG retain transparency?** Yes, using `PngColorType.TruecolorWithAlpha`.  
- **Is the operation fast for large files?** Aspose.PSD is optimized for performance on high‑resolution PSDs.

## What is “convert PSD to PNG” and why crop it?

Photoshop Document(PSD)를 PNG로 변환하는 것은 웹에 사용할 이미지나 디자인의 경량 버전이 필요할 때 일반적인 단계입니다. 크롭을 하면 캔버스에서 필요한 부분만 추출할 수 있어 파일 크기를 줄이고 핵심 콘텐츠에 집중할 수 있습니다. 두 작업을 하나의 워크플로우로 결합하면 시간을 절약하고 코드베이스를 단순하게 유지할 수 있습니다.

## Prerequisites

Before we dive in, make sure you have:

- **Java Development Environment** – JDK 8+ installed and configured.  
- **Aspose.PSD for Java** – Download the library and add it to your project. You can find the library and its documentation [here](https://reference.aspose.com/psd/java/).  
- **Sample PSD File** – A PSD file placed inside your project directory that you want to crop and convert.

## Import Packages

In your Java project, begin by importing the necessary packages to leverage Aspose.PSD functionalities. Add the following import statements:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

## Step 1: Set Document Directory

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 PSD 파일이 실제로 위치한 경로로 교체합니다.

## Step 2: Load PSD File

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

크롭하려는 PSD 파일을 `RasterImage` 객체로 로드합니다.

## Step 3: Define Crop Area

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

`Rectangle` 클래스를 사용해 **x**, **y**, **width**, **height** 값을 지정하여 크롭 영역을 정의합니다.

## Step 4: Save Cropped PSD

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

지정한 경로에 잘라낸 이미지를 PSD 형식으로 저장합니다.

## Step 5: Save Cropped Image as PNG

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

또한 투명성을 유지한 채 잘라낸 이미지를 PNG 파일로 내보냅니다.

## Why use Aspose.PSD for Java to crop PSD files?

- **Full PSD fidelity** – All layers, masks, and effects stay intact during conversion.  
- **No native Photoshop required** – Works completely on the server side.  
- **High performance** – Optimized for large files and batch processing.  
- **Simple API** – A handful of lines of code achieve cropping and conversion.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **File not found** | Verify `dataDir` ends with a path separator (`/` or `\\`). |
| **Transparent background lost** | Ensure `PngOptions.setColorType(PngColorType.TruecolorWithAlpha)` is set. |
| **Out‑of‑memory for huge PSDs** | Process the image in chunks or increase JVM heap (`-Xmx`). |
| **License exception** | Apply your Aspose license before loading the image (`License license = new License(); license.setLicense("Aspose.PSD.lic");`). |

## Frequently Asked Questions

**Q: Can I use Aspose.PSD for Java to crop images in other formats?**  
A: While the primary focus is PSD, the library also supports PNG, JPEG, BMP, and other raster formats.

**Q: Is Aspose.PSD suitable for large‑scale image processing?**  
A: Yes, it’s optimized for performance and can handle batch operations efficiently.

**Q: Are there licensing considerations for production use?**  
A: Yes, refer to the [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy) for details.

**Q: Where can I get community support?**  
A: Visit the [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) for help from other developers.

**Q: Can I try the library before buying?**  
A: Absolutely—download a free trial [here](https://releases.aspose.com/).

## Conclusion

You now have a complete, end‑to‑end solution for **converting PSD to PNG** while cropping the image to the exact region you need. Integrate these snippets into your Java projects to automate Photoshop‑style image manipulation without the overhead of Photoshop itself.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-09  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

---