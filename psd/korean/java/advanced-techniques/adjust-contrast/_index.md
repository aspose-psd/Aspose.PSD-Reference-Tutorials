---
date: 2026-07-27
description: 선도적인 Java 이미지 조작 라이브러리인 Aspose.PSD for Java를 사용하여 PSD를 TIFF로 변환하고 이미지
  대비 조정을 수행하는 방법을 배웁니다.
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: PSD를 TIFF로 변환하고 대비 조정
og_description: Aspose.PSD for Java를 사용하여 대비 조정과 함께 PSD를 TIFF로 변환합니다. 이 가이드는 단계별 코드,
  성능 팁 및 고품질 TIFF 출력을 위한 내보내기 옵션을 보여줍니다.
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: PSD를 TIFF로 변환 및 대비 조정 – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: Aspose.PSD for Java를 사용하여 PSD를 TIFF로 변환하고 대비를 조정하기
url: /ko/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD를 TIFF로 변환하고 Aspose.PSD for Java로 대비 조정하는 방법

## 소개

그래픽의 시각적 품질을 미세 조정하면서 **PSD를 TIFF로 변환**해야 한다면, 여기가 바로 적합한 곳입니다. 이 튜토리얼에서는 강력한 **java image manipulation** 라이브러리인 Aspose.PSD for Java를 사용한 전체 워크플로우를 단계별로 안내합니다. **이미지 대비 조정**을 향상시키고, 성능을 위해 대용량 래스터 데이터를 캐시하며, 마지막으로 **이미지를 TIFF로 저장**하여 후속 처리에 활용하는 방법을 배웁니다. 시작해 보겠습니다!

## 빠른 답변
- **“adjust contrast”는 무엇을 의미하나요?** 가장 어두운 픽셀과 가장 밝은 픽셀 사이의 차이를 변경하여 디테일을 돋보이게 합니다.  
- **어떤 라이브러리가 이를 처리하나요?** Aspose.PSD for Java – 전체 기능을 갖춘 이미지 처리 툴킷.  
- **라이선스가 필요합니까?** 테스트용 **temporary Aspose license**는 작동하지만, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **PSD를 TIFF로 변환할 수 있나요?** 물론입니다 – `TiffOptions`를 사용해 처리된 이미지를 내보냅니다.  
- **변환 속도는 어느 정도인가요?** 일반적인 30 MB PSD의 경우 전체 파이프라인이 최신 CPU에서 1초 미만에 실행됩니다.

## 이미지 대비 조정이란?

대비 조정은 이미지의 톤 범위를 변경하여 밝은 영역과 어두운 영역 사이의 차이를 확대합니다. 이는 스캔 후 이미지가 평평하게 보이거나 인쇄용 그래픽을 준비할 때 특히 유용합니다. 픽셀 강도의 히스토그램을 늘리거나 압축함으로써 그림자를 더 깊게, 하이라이트를 더 밝게 만들어 인지된 깊이와 디테일을 향상시킵니다.

## 왜 Aspose.PSD for Java를 사용하나요?

Aspose.PSD는 **50+ raster and vector formats**를 처리할 수 있는 고성능·다기능 엔진을 제공하며, 전체 메모리 로드 없이 최대 500 MB 파일을 처리하고, 비트‑퍼‑샘플 및 포토메트릭 해석에 대한 정밀한 제어를 통해 TIFF로 내보낼 수 있습니다. 이러한 정량화된 기능 덕분에 엔터프라이즈 수준 이미지 파이프라인에 최적의 선택이 됩니다.

## 전제 조건

시작하기 전에 다음을 확인하세요:

- Java 프로그래밍에 대한 기본 지식.  
- Aspose.PSD for Java 라이브러리가 설치되어 있어야 합니다. [here](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

## 패키지 가져오기

Java 클래스에 필요한 import를 추가합니다:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1단계: 이미지 로드

`Image` 클래스는 Aspose.PSD의 진입점으로, 메모리 내에서 지원되는 모든 래스터 이미지를 나타냅니다.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

`sample.psd` 소스 PSD 파일을 `Image` 객체에 로드하면, 이후 모든 처리의 진입점이 됩니다.

## 2단계: RasterImage로 캐스팅하고 데이터 캐시

`RasterImage`는 픽셀 수준의 직접 접근을 제공하고 대용량 파일에 대한 캐싱을 가능하게 합니다.  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage`로 캐스팅하면 픽셀 수준 연산에 접근할 수 있습니다. 캐싱은 특히 대용량 파일에서 성능을 향상시킵니다.

## 이미지 대비를 조정하는 방법

`adjustContrast` 메서드는 이미지 대비를 백분율 값으로 변경하는 간단한 API 호출입니다.  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 메서드는 백분율 변화를 나타내는 정수를 인수로 받습니다. 이 예제에서는 대비를 **50 %** 상승시킵니다.

## Aspose.PSD를 사용해 PSD를 TIFF로 변환

`TiffOptions`를 사용하면 비트‑퍼‑샘플, 압축 유형, 포토메트릭 해석 등 TIFF 전용 설정을 지정할 수 있습니다.  
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

여기서는 `TiffOptions`(비트‑퍼‑샘플, 포토메트릭 해석)를 구성하고 **이미지를 TIFF로 저장**합니다. 이 단계가 **PSD를 TIFF로 변환** 워크플로우를 완료합니다.

## 일반적인 문제와 해결책
- **Image not cached:** 대용량 PSD에서는 `OutOfMemoryError`를 방지하기 위해 항상 `cacheData()`를 호출하세요.  
- **Unexpected color shift:** `setPhotometric`이 목표 색상 공간(RGB vs. CMYK)과 일치하는지 확인하세요.  
- **File not found:** `dataDir`이 올바른 폴더를 가리키고 파일 이름이 정확히 입력되었는지 확인하세요.

## 자주 묻는 질문

### Q1: Aspose.PSD가 다양한 이미지 형식과 호환되나요?
A1: 네, Aspose.PSD는 **50+ input and output formats**를 지원하며, PSD, TIFF, PNG, JPEG, BMP, GIF 등을 포함해 프로젝트 전반에 걸쳐 유연성을 제공합니다.

### Q2: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?
A2: [here](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

### Q3: Aspose.PSD 문서는 어디서 찾을 수 있나요?
A3: 문서는 [here](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

### Q4: Aspose.PSD에 대한 지원 옵션은 무엇인가요?
A4: 지원을 원하시면 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 를 방문하세요.

### Q5: Aspose.PSD를 구매할 수 있나요?
A5: 네, [here](https://purchase.aspose.com/buy)에서 Aspose.PSD를 구매할 수 있습니다.

## 결론

이제 Aspose.PSD for Java를 사용해 **PSD를 TIFF로 변환**하고 **이미지 대비 조정**을 수행하는 방법을 알게 되었습니다. 이러한 단계는 코드가 깔끔하고 유지 관리가 쉬운 상태에서 이미지 품질을 세밀하게 제어할 수 있게 해줍니다. 필요에 따라 `adjustBrightness`나 `adjustGamma`와 같은 다른 조정 메서드를 자유롭게 실험해 보세요.

---

**마지막 업데이트:** 2026-07-27  
**테스트 환경:** Aspose.PSD for Java 24.12  
**작성자:** Aspose

## 관련 튜토리얼

- [Java 이미지 처리 튜토리얼 - Aspose.PSD for Java로 이미지 밝기 조정](/psd/java/advanced-techniques/adjust-brightness/)
- [Aspose.PSD와 함께 Java 이미지 처리에서 감마 조정하는 방법](/psd/java/advanced-techniques/adjust-gamma/)
- [Aspose.PSD for Java로 PSD를 래스터 이미지 형식으로 변환](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}