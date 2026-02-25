---
date: 2026-02-25
description: Aspose.PSD for Java, 선도적인 Java 이미지 조작 라이브러리를 사용하여 PSD를 TIFF로 변환하고 이미지
  대비 조정을 수행하는 방법을 배워보세요.
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 PSD를 TIFF로 변환하고 대비를 조정하는 방법
url: /ko/java/advanced-techniques/adjust-contrast/
weight: 22
---

, code block placeholders unchanged.

Let's write translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 TIFF로 변환하고 대비 조정하는 방법

## Introduction

그래픽의 시각적 품질을 미세 조정하면서 **PSD를 TIFF로 변환**해야 한다면, 여기가 바로 적합한 곳입니다. 이 튜토리얼에서는 강력한 **java image manipulation** 라이브러리인 Aspose.PSD for Java를 사용한 전체 워크플로우를 단계별로 살펴봅니다. **이미지 대비 조정**을 강화하고, 대용량 래스터 데이터를 캐시하여 성능을 향상시키며, 마지막으로 **이미지를 TIFF로 저장**하여 후속 처리에 활용하는 방법을 배웁니다. 시작해 보겠습니다!

## Quick Answers
- **adjust contrast**는 무엇을 의미하나요? 가장 어두운 픽셀과 가장 밝은 픽셀 사이의 차이를 변경하여 디테일을 돋보이게 합니다.  
- **어떤 라이브러리가 이를 처리하나요?** Aspose.PSD for Java – 전체 기능을 갖춘 이미지 처리 툴킷.  
- **라이선스가 필요합니까?** 테스트용 **temporary aspose license**는 작동하지만, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **PSD를 TIFF로 변환할 수 있나요?** 물론입니다 – 처리된 이미지를 내보내기 위해 `TiffOptions`를 사용할 것입니다.  
- **코드 실행 시간은 얼마나 걸리나요?** 최신 하드웨어에서 일반적인 크기의 PSD 파일은 보통 1초 미만에 완료됩니다.

## What is Image Contrast Adjustment?

대비 조정은 이미지의 톤 범위를 변경하여 밝은 영역과 어두운 영역 사이의 구분을 강화합니다. 스캔 후 이미지가 평평하게 보이거나 인쇄용 그래픽을 준비할 때 특히 유용합니다.

## Why Use Aspose.PSD for Java?
- **Rich format support** – 열기, 편집 및 **save image as TIFF**, PNG, JPEG 등 다양한 포맷으로 저장할 수 있습니다.  
- **High performance** – 캐싱 및 래스터 이미지 최적화를 통해 메모리 사용량을 줄여 대용량 PSD 파일 처리에 필수적입니다.  
- **Straight‑forward API** – `adjustContrast`와 같은 단일 메서드 호출로 코드 가독성과 유지보수성을 높입니다.  
- **Comprehensive java image manipulation** 기능을 제공하여 간단한 스크립트부터 엔터프라이즈급 애플리케이션까지 모두에 적합합니다.

## Prerequisites

시작하기 전에 다음이 준비되어 있어야 합니다:

- Java 프로그래밍에 대한 기본 지식.  
- Aspose.PSD for Java 라이브러리 설치. 라이브러리는 [here](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

## Import Packages

Add the required imports to your Java class:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

우리는 소스 PSD 파일(`sample.psd`)을 `Image` 객체에 로드합니다. 이 객체는 이후 모든 처리를 위한 진입점 역할을 합니다.

## Step 2: Cast to RasterImage and Cache Data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage`로 캐스팅하면 픽셀 수준 작업에 접근할 수 있습니다. 캐싱을 통해 특히 큰 파일의 성능이 크게 향상됩니다.

## How to Adjust Contrast of an Image

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 메서드는 변화 비율을 나타내는 정수를 인수로 받습니다. 이 예제에서는 대비를 **50 %** 상승시킵니다.

## Convert PSD to TIFF Using Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

여기서는 `TiffOptions`(샘플당 비트 수, 포토메트릭 해석)를 설정하고 **save image as TIFF**합니다. 이 단계가 **convert PSD to TIFF** 워크플로우를 완성합니다.

## Common Issues and Solutions
- **Image not cached:** 대용량 PSD 파일에서는 `cacheData()`를 반드시 호출하여 `OutOfMemoryError`를 방지하십시오.  
- **Unexpected color shift:** `setPhotometric`이 목표 색 공간(RGB vs. CMYK)과 일치하는지 확인하십시오.  
- **File not found:** `dataDir`이 올바른 폴더를 가리키고 파일 이름이 정확히 입력되었는지 확인하십시오.

## Frequently Asked Questions

### Q1: Aspose.PSD가 다양한 이미지 포맷과 호환되나요?

A1: 네, Aspose.PSD는 다양한 이미지 포맷을 지원하므로 프로젝트에서 유연하게 활용할 수 있습니다.

### Q2: Aspose.PSD 임시 라이선스는 어떻게 얻나요?

A2: 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

### Q3: Aspose.PSD 문서는 어디서 찾을 수 있나요?

A3: 문서는 [here](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

### Q4: Aspose.PSD 지원 옵션은 어떤 것이 있나요?

A4: 지원이 필요하면 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)에서 문의하십시오.

### Q5: Aspose.PSD를 구매할 수 있나요?

A5: 네, Aspose.PSD는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

## Conclusion

이제 Aspose.PSD for Java를 사용하여 **PSD를 TIFF로 변환**하고 **이미지 대비 조정**을 수행하는 방법을 알게 되었습니다. 이러한 단계는 이미지 품질을 세밀하게 제어하면서 코드를 깔끔하고 유지보수하기 쉽게 만들어 줍니다. 필요에 따라 `adjustBrightness`나 `adjustGamma`와 같은 다른 조정 메서드를 실험해 보세요.

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}