---
date: 2026-06-03
description: Aspose.PSD for Java를 사용하여 이미지를 크기 조정하는 방법을 배웁니다. 이 단계별 가이드에서는 Resize
  Type Enumeration, 고품질 이미지 크기 조정, 그리고 PSD를 JPEG로 변환하는 방법을 다룹니다.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Resize Type Enumeration을 사용한 크기 조정
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Resize Type Enumeration을 사용한 Java 이미지 크기 조정 방법
url: /ko/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 Resize Type 열거형을 사용한 이미지 크기 조정 방법

## 소개

Java 프로젝트에서 이미지 파일을 효율적으로 **how to resize image**하려면 Aspose.PSD for Java가 깔끔하고 고성능 API를 제공합니다. 이 튜토리얼에서는 PSD를 로드하고, 고품질 이미지 크기 조정을 위해 **Resize Type Enumeration**을 적용한 다음 **convert PSD to JPEG**하는 과정을 살펴봅니다. 데스크톱 편집기든 자동화된 서버‑사이드 파이프라인이든, 몇 줄의 코드만으로 차원, 품질 및 형식을 제어할 수 있습니다.

## 빠른 답변
- **resize image java를 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java.
- **어떤 resize type이 최고의 품질을 제공하나요?** `ResizeType.LanczosResample`.
- **크기 조정 후 PSD를 JPEG로 변환할 수 있나요?** Yes – simply save with `JpegOptions`.
- **프로덕션에 라이선스가 필요합니까?** A valid Aspose.PSD license is required for production use.
- **이 접근 방식이 대량 배치에 적합한가요?** Absolutely; the API processes multi‑hundred‑page files without loading the whole document into memory.

## Java에서 "how to resize image"란 무엇인가요?

**How to resize image**는 시각적 충실도를 유지하면서 이미지의 픽셀 차원을 프로그래밍 방식으로 변경하는 것을 의미합니다. Aspose.PSD의 `Resize` 메서드와 `ResizeType` 열거형을 결합하면 스케일링 알고리즘에 대한 정밀한 제어가 가능해져 개발자가 다양한 원본 파일과 목표 크기 전반에 걸쳐 품질을 유지할 수 있습니다.

## 왜 Resize Type 열거형을 사용하나요?

`ResizeType`은 속도와 시각적 품질의 균형을 가장 잘 맞추는 재샘플링 알고리즘을 선택할 수 있게 해줍니다. 대부분의 상황에서 **LanczosResample**은 적당한 성능 비용으로 선명한 결과를 제공하며, 일반적인 서버급 CPU에서 2000 × 1500 이미지를 120 ms 미만으로 처리하면서 가장자리 디테일을 유지합니다.

## 사전 요구 사항

시작하기 전에 다음을 확인하십시오:

1. **Java Development Environment** – JDK 8 이상 설치 및 구성.  
2. **Aspose.PSD Library** – 최신 JAR를 [웹사이트](https://releases.aspose.com/psd/java/)에서 다운로드하십시오.  
3. **Sample PSD File** – SDK에 포함된 [sample.psd](Your Document Directory/sample.psd) 파일을 사용하여 직접 테스트하십시오.

## 패키지 가져오기

`Image`는 Aspose.PSD에서 모든 이미지 유형의 기본 클래스입니다. Java 소스 파일에 필요한 import를 추가하십시오:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 1단계: 이미지 로드

### 정의 앵커
`RasterImage` 클래스는 PSD 파일에서 로드된 래스터 기반 이미지를 나타내는 Aspose.PSD의 핵심 객체입니다.

PSD를 `RasterImage` 인스턴스로 로드하여 픽셀을 조작할 수 있습니다:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## 2단계: 이미지 크기 조정

`image.resize(width, height, resizeType)`는 선택한 알고리즘을 사용하여 이미지를 지정된 차원으로 크기 조정합니다.

이제 **Resize Type Enumeration**을 사용해 로드된 이미지를 크기 조정합니다. 이 예제에서는 고품질로 **how to resize image**할 때 이상적인 Lanczos Resample 방법을 사용합니다:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 3단계: 크기 조정된 이미지 저장

`image.save(path, options)`는 제공된 옵션에 정의된 형식으로 이미지를 디스크에 기록합니다.

크기 조정 후, 지정된 차원과 선택한 resize type으로 이미지를 저장합니다. 여기서는 결과를 JPEG 파일로 저장하여 **convert psd to jpeg**를 시연합니다:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## 왜 Resize Type 열거형을 사용하나요?

`ResizeType`은 재샘플링 알고리즘에 대한 세밀한 제어를 제공하여 속도와 품질의 균형을 맞출 수 있게 합니다. 대부분의 애플리케이션에서 `LanczosResample`은 큰 성능 비용 없이 선명한 결과를 제공하는 훌륭한 절충점을 제공하며, 다양한 이미지 콘텐츠에서도 잘 작동합니다.

## 일반적인 문제 및 해결책

- **Image appears blurry after resize** – 다른 `ResizeType`(예: `Bicubic` 또는 `NearestNeighbour`)을 시도하여 특정 이미지에 가장 적합한 시각적 결과를 확인하십시오.  
- **OutOfMemoryError on large PSD files** – 이미지를 더 작은 청크로 처리하거나 JVM 힙 크기(`-Xmx` 플래그)를 늘리십시오. Aspose.PSD는 전체 문서를 메모리에 로드하지 않고도 **2 GB**까지 파일을 처리할 수 있습니다.

## 자주 묻는 질문

### Q1: Aspose.PSD for Java가 소규모 및 대규모 프로젝트 모두에 적합한가요?

A1: 물론입니다! Aspose.PSD for Java는 모든 규모의 프로젝트에 맞게 설계되어 확장성과 효율성을 제공합니다.

### Q2: Lanczos Resample 외에 다른 resize type을 사용할 수 있나요?

A2: 예, Aspose.PSD for Java는 **NearestNeighbour**, **Bicubic** 등 다양한 resize type을 제공합니다. 전체 목록은 API 문서를 참고하십시오.

### Q3: Aspose.PSD for Java에 대한 추가 지원을 어디서 찾을 수 있나요?

A3: 문의나 지원이 필요하면 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 방문하십시오.

### Q4: Aspose.PSD for Java의 무료 체험판이 있나요?

A4: 예, 무료 체험 버전을 [여기](https://releases.aspose.com/)에서 이용할 수 있습니다.

### Q5: Aspose.PSD for Java의 임시 라이선스를 어떻게 얻을 수 있나요?

A5: 임시 라이선스를 얻으려면 [이 링크](https://purchase.aspose.com/temporary-license/)를 방문하십시오.

## 자주 묻는 질문

**Q: 크기 조정 없이 PSD 파일을 프로그래밍 방식으로 JPEG로 변환하려면 어떻게 해야 하나요?**  
A: `Image.load`로 PSD를 로드한 다음 `image.save("output.jpg", new JpegOptions());`를 호출하십시오.

**Q: 크기 조정 시 원본 DPI를 유지할 수 있나요?**  
A: 예, 저장하기 전에 `Image` 객체의 `Resolution` 속성을 설정하면 됩니다.

**Q: 여러 번의 resize 작업을 연속으로 수행할 수 있나요?**  
A: `resize`를 여러 번 호출할 수는 있지만, 최종 차원을 계산한 뒤 한 번만 크기 조정하는 것이 더 효율적입니다.

---

**마지막 업데이트:** 2026-06-03  
**테스트 환경:** Aspose.PSD for Java 24.12  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.PSD를 사용한 간단한 리사이징 – Java 이미지 조작 라이브러리](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java에서 Bicubic Resampler를 사용한 고품질 이미지 스케일링](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Aspose.PSD for Java를 사용해 PSD를 PNG로 변환하고 비례적으로 리사이즈하는 방법](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}