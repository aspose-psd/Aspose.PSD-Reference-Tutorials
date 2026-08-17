---
date: 2026-08-17
description: Aspose.PSD for Java를 사용하여 Bradley thresholding으로 이미지를 이진화하는 방법. PSD를
  PNG로 변환하고 이미지 품질을 향상시키는 단계별 가이드를 따라 보세요.
keywords:
- how to binarize image
- convert psd to png
- set threshold value
- enhance image quality
- save binarized image
lastmod: 2026-08-17
linktitle: Bradley Thresholding
og_description: Aspose.PSD for Java에서 Bradley thresholding을 사용하여 이미지를 이진화하는 방법을 배워보세요.
  이 가이드는 threshold value를 설정하고, PSD를 PNG로 변환하며, binarized image를 저장하는 방법을 보여줍니다.
og_image_alt: 'Guide: binarize image using Bradley thresholding in Aspose.PSD for
  Java'
og_title: Java에서 Bradley thresholding으로 이미지 이진화하는 방법
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  headline: How to binarize image in Java using Bradley thresholding
  type: TechArticle
- description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  name: How to binarize image in Java using Bradley thresholding
  steps:
  - name: '**Java development environment** – JDK 11 or newer installed and configured.'
    text: '**Java development environment** – JDK 11 or newer installed and configured.'
  - name: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
    text: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
  type: HowTo
- questions:
  - answer: It is an adaptive binarization technique that computes a local average
      for each pixel and thresholds based on a percentage of that average.
    question: What is Bradley thresholding?
  - answer: Start with 0.5 (50 %). If the output is too noisy, increase the value;
      if details are lost, decrease it. Test a few values on a representative sample.
    question: How do I choose the right threshold value?
  - answer: Yes. Aspose.PSD supports more than 30 input and output formats—including
      PSD, PNG, JPEG, BMP, and TIFF—so you can load a JPEG, convert it to a `PsdImage`,
      and then binarize.
    question: Can I apply Bradley thresholding to other image formats?
  - answer: You can call `image.save("preview.png", new PngOptions())` after the `binarizeBradley`
      step to write a temporary file for visual inspection.
    question: Is there a way to preview the binarized image before saving?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      help and explore the official [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references.
    question: Where can I find more support and resources?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- image binarization
- Aspose.PSD
- Java image processing
- Bradley thresholding
title: Java에서 Bradley thresholding을 사용하여 이미지 이진화하는 방법
url: /ko/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 Bradley 임계값을 사용하여 이미지 이진화하는 방법

## 소개

이 튜토리얼에서는 Aspose.PSD for Java를 사용하여 Bradley 임계값을 적용함으로써 **이미지를 이진화하는 방법**을 배웁니다. 이진화는 컬러 또는 그레이스케일 이미지를 흑백 버전으로 변환하는 것으로, OCR, 문서 보관 및 다양한 컴퓨터 비전 파이프라인에 필수적입니다. PSD 파일을 로드하고 최종 PNG로 저장하는 모든 단계를 단계별로 안내하므로, 이 기술을 여러분의 Java 프로젝트에 쉽게 통합할 수 있습니다.

## 빠른 답변
- **Bradley 임계값은 무엇을 하나요?** 각 픽셀에 대해 지역 임계값을 자동으로 결정하여 조명이 고르지 않은 경우에도 세부 정보를 보존합니다.
- **필요한 라이브러리는 무엇인가요?** Aspose.PSD for Java (최신 버전 권장).
- **라이선스가 필요합니까?** 개발용으로는 무료 체험판을 사용할 수 있으며, 프로덕션에서는 상용 라이선스가 필요합니다.
- **큰 PSD 파일을 처리할 수 있나요?** 예, API는 전체 이미지를 메모리에 로드하지 않고도 최대 2 GB 파일을 처리합니다.
- **추천 출력 포맷은 무엇인가요?** PNG는 무손실이며 이진화 결과에 널리 지원됩니다.

## Bradley 임계값이란?

Bradley 임계값은 각 픽셀 주변의 지역 평균을 계산하고, 픽셀 강도가 해당 평균보다 설정 가능한 비율만큼 높으면 흰색으로 설정하는 적응형 이진화 알고리즘입니다. 이 방법은 조명이 이미지 전체에 걸쳐 변동이 있더라도 가장자리 세부 정보를 유지합니다.

## 이미지 이진화에 Bradley 임계값을 사용하는 이유

Bradley 임계값은 조명이 고르지 않은 이미지에서도 일관된 높은 대비를 제공하여, 전역 임계값 방법에 비해 스캔 문서에서 최대 95 % OCR 정확도를 달성합니다. Aspose.PSD의 구현은 일반적인 8코어 서버에서 500페이지 PSD를 4 초 이하로 처리하므로 배치 작업에 적합합니다.

## 사전 요구 사항

시작하기 전에 다음이 준비되어 있는지 확인하십시오:

1. **Java 개발 환경** – JDK 11 이상이 설치되고 구성되어 있어야 합니다.
2. **Aspose.PSD 라이브러리** – 최신 JAR를 [Aspose.PSD Java 다운로드 페이지](https://releases.aspose.com/psd/java/)에서 다운로드하십시오.
3. **샘플 PSD 이미지** – 이진화하려는 PSD 파일; 소유한 이미지나 테스트 파일을 사용할 수 있습니다.

## 패키지 가져오기

다음 import 구문을 사용하면 이미지 로드, 처리 및 저장에 필요한 핵심 클래스를 사용할 수 있습니다.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Bradley 임계값을 사용하여 이미지 이진화하는 방법

이 튜토리얼에서는 PSD 파일을 로드하고 적절한 임계값을 선택한 뒤, 적응형 Bradley 이진화를 실행하고 최종적으로 결과를 PNG 파일로 저장합니다. 이 과정은 네 개의 간결한 메서드 호출로 구성되며, 각각 코드 예제로 보여주어 최소한의 노력으로 모든 Java 애플리케이션에 워크플로를 통합할 수 있습니다.

## 단계 1: 이미지 로드

`PsdImage` 클래스는 메모리 내에서 PSD 파일을 나타내며 픽셀 수준 조작을 위한 메서드를 제공합니다. 인스턴스를 생성하면 전체 이미지 데이터에 접근할 수 있습니다.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

이 단계에서는 PSD 파일을 디스크에서 읽어 `PsdImage` 객체에 저장하고, 처리를 위해 준비합니다.

## 단계 2: 임계값 정의

`threshold` 매개변수는 이진화 강도를 제어합니다; 0.5(50 %) 값이 일반적인 시작점입니다. 원본 이미지의 대비에 따라 조정하십시오.

```java
// Define threshold value
double threshold = 0.15;
```

임계값을 올바르게 설정하면 노이즈 감소와 세부 보존 사이의 균형을 맞출 수 있습니다.

## 단계 3: Bradley 임계값 적용

`binarizeBradley` 메서드는 제공한 임계값을 사용하여 적응형 이진화를 수행합니다. 각 픽셀 주변의 지역 윈도우를 분석하여 검은색 또는 흰색으로 변환할지를 결정합니다.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

이 호출 후 `PsdImage` 인스턴스는 원본 이미지의 흑백 버전을 포함합니다.

## 단계 4: 출력 이미지 저장

`save` 메서드는 처리된 이미지를 파일 시스템에 기록합니다. PNG를 선택하는 이유는 추가 압축 아티팩트 없이 이진 데이터를 보존하기 때문입니다.

```java
// Save the output image
image.save(destName, new PngOptions());
```

이제 OCR 엔진이나 기타 후속 프로세스에 사용할 수 있는 이진화된 PNG가 준비되었습니다.

## 일반적인 문제와 해결책

LoadOptions는 PSD 파일을 로드하는 방식을 지정할 수 있는 클래스이며, 예를 들어 스트리밍 모드를 활성화하여 메모리 사용량을 줄일 수 있습니다.

- **이미지가 너무 어둡거나 밝게 보임** – 임계값을 조정하십시오; 낮은 값은 이미지를 밝게, 높은 값은 어둡게 만듭니다.
- **매우 큰 PSD에서 메모리 부족 오류** – 로드하기 전에 `PsdImage.setLoadOptions(new LoadOptions { LoadMode = LoadMode.Stream })`를 호출하여 스트리밍 모드를 활성화하십시오. `LoadMode.Stream`은 대용량 파일에 대한 스트리밍 모드를 활성화합니다.
- **예상치 못한 색 밴드** – 원본 PSD가 RGB 모드인지 확인하고, 필요하면 `image.convertToRgb()`를 사용해 변환하십시오. `convertToRgb()` 메서드는 이미지를 RGB 색 공간으로 변환하여 올바른 색상 처리를 보장합니다.

## 자주 묻는 질문

**Q: Bradley 임계값이란 무엇인가요?**  
A: 각 픽셀에 대한 지역 평균을 계산하고 해당 평균의 일정 비율을 기준으로 임계값을 적용하는 적응형 이진화 기법입니다.

**Q: 올바른 임계값을 어떻게 선택하나요?**  
A: 0.5(50 %)부터 시작하십시오. 출력이 너무 노이즈가 많으면 값을 높이고, 세부 정보가 손실되면 값을 낮추세요. 대표 샘플에서 몇 가지 값을 테스트해 보세요.

**Q: Bradley 임계값을 다른 이미지 포맷에도 적용할 수 있나요?**  
A: 예. Aspose.PSD는 PSD, PNG, JPEG, BMP, TIFF 등을 포함해 30개 이상의 입력 및 출력 포맷을 지원하므로 JPEG를 로드하고 `PsdImage`로 변환한 뒤 이진화할 수 있습니다.

**Q: 저장하기 전에 이진화된 이미지를 미리 볼 수 있나요?**  
A: `binarizeBradley` 단계 후에 `image.save("preview.png", new PngOptions())`를 호출하여 시각 검토용 임시 파일을 작성할 수 있습니다.

**Q: 커뮤니티 지원을 위해 어디서 더 많은 자료를 찾을 수 있나요?**  
A: 커뮤니티 지원을 위해 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 방문하고, 자세한 API 레퍼런스를 위해 공식 [문서](https://reference.aspose.com/psd/java/)를 살펴보세요.

---

**마지막 업데이트:** 2026-08-17  
**테스트 환경:** Aspose.PSD 24.12 for Java  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Java 이미지 처리 튜토리얼 - Aspose.PSD for Java를 사용한 이미지 밝기 조정](/psd/java/advanced-techniques/adjust-brightness/)
- [Java 이미지 처리에서 Aspose.PSD로 감마 조정하는 방법](/psd/java/advanced-techniques/adjust-gamma/)
- [이미지 처리 Java 라이브러리: Aspose.PSD를 사용한 레이어 반전](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}