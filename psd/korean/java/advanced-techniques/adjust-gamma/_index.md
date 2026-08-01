---
date: 2026-08-01
description: Aspose.PSD를 사용한 Java 이미지 처리에서 감마를 조정하고, PSD를 TIFF로 변환하며, 색이 바랜 이미지를 간결한
  튜토리얼로 해결하는 방법을 배웁니다.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: 이미지의 감마 조정
og_description: Aspose.PSD를 사용한 Java 이미지 처리에서 감마를 조정하는 방법을 배우세요 – 색이 바랜 이미지를 복구하고
  PSD를 TIFF로 변환하는 빠른 서버‑사이드 라이브러리로, 몇 줄의 코드만으로 가능합니다.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: 감마 조정 방법 – Aspose.PSD와 함께하는 Java 처리
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Aspose.PSD를 사용한 Java 이미지 처리에서 감마 조정 방법
url: /ko/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 이미지 처리에서 Aspose.PSD를 사용한 감마 조정 방법

## 소개

**java image processing** 작업을 할 때, **감마를 조정하는 방법**을 배우는 것은 디테일을 잃지 않으면서 밝기와 대비를 개선하는 기본 기술입니다. 이 튜토리얼에서는 **Aspose.PSD for Java**를 사용하여 PSD 파일에 감마 보정을 적용하고, **PSD를 TIFF로 변환**하며, **색이 바랜 이미지**를 방지하는 방법을 단계별로 살펴봅니다. 이 접근 방식이 빠르고 신뢰할 수 있으며 **서버‑사이드 이미지 처리** 파이프라인에 완벽한 이유를 확인해 보세요.

## 빠른 답변
- **감마 보정은 무엇을 하나요?** 밝기 값을 재매핑하여 어두운 영역을 밝게, 밝은 영역을 어둡게 만들면서 전체 디테일을 유지합니다.  
- **어떤 라이브러리가 처리를 담당하나요?** Aspose.PSD for Java는 래스터 이미지용 전용 `adjustGamma` 메서드를 제공합니다.  
- **같은 흐름에서 PSD를 TIFF로 변환할 수 있나요?** 예 – 감마 조정 후 `TiffOptions`를 사용해 이미지를 직접 TIFF로 저장할 수 있습니다.  
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트 가능하지만, 상용 사용에는 상업용 라이선스가 필요합니다.  
- **지원되는 Java 버전은 무엇인가요?** Aspose.PSD는 Java 8 및 이후 버전을 지원합니다.

## Java 감마 보정이란?

감마 보정은 인코딩된 픽셀 값과 표시되는 밝기 사이의 비선형 관계를 변경합니다. 감마 곡선을 조정하면 **색이 바랜 이미지** 문제를 해결하거나 하이라이트를 과다 노출시키지 않으면서 그림자 디테일을 강화할 수 있습니다. 각 픽셀에 거듭제곱 함수를 적용하여 어두운 톤을 밝게 하고 하이라이트를 압축함으로써 보다 자연스러운 시각적 모습을 얻습니다.

## 감마 보정에 Aspose.PSD를 사용하는 이유

Aspose.PSD는 **java image processing library**로 PSD 형식의 복잡성을 추상화합니다. 2 GB까지 파일을 처리하고 50가지가 넘는 이미지 형식을 지원하며, 간단한 `adjustGamma` 호출만으로 **java gamma correction** 및 **convert PSD to TIFF** 워크플로에 이상적입니다.

## 전제 조건

1. **Java 개발 환경** – Java 8 이상이 설치되어 있어야 합니다.  
2. **Aspose.PSD 라이브러리** – JAR 파일을 다운로드하여 프로젝트에 추가하세요. 공식 [documentation](https://reference.aspose.com/psd/java/)을 참조하십시오.  
3. **샘플 이미지** – 처리하려는 PSD 파일 (예: `sample.psd`).  

## 패키지 가져오기

시작하기 전에, 래스터 처리와 파일 형식 옵션에 접근할 수 있는 필수 네임스페이스를 가져오세요.

## 1단계: 이미지 로드

`RasterImage` 클래스는 메모리 내 PSD 레이어의 래스터화된 픽셀 데이터를 나타냅니다. 이미지를 한 번 로드하고 캐시하면 이후 조정 시 메모리 사용량을 줄일 수 있습니다.

## 2단계: 감마 조정

`new RasterImage("sample.psd")`로 PSD를 로드하고 `rasterImage.adjustGamma(2.0f)`를 호출하세요 — 이 한 줄로 모든 색 채널에 감마 2.0을 적용해 그림자를 밝게 하면서 하이라이트는 그대로 유지합니다. 채널별로 다른 값을 전달하여 빨강, 초록, 파랑을 개별적으로 조정할 수도 있습니다.

## 3단계: TiffOptions 생성

`TiffOptions`를 사용하면 압축, 샘플당 비트 수 및 기타 TIFF‑특화 설정을 제어할 수 있습니다. 8‑비트 샘플 (`{8,8,8}`)을 설정하면 TIFF 파일 크기를 적절하게 유지하면서 색 정확성을 보존합니다.

## 4단계: 결과 이미지 저장

`rasterImage.save("output.tif", tiffOptions)`를 호출하여 처리된 이미지를 디스크에 기록합니다. 저장 후에는 인쇄 서비스나 웹 API와 같은 다운스트림 시스템에 TIFF를 전달할 수 있습니다.

## 일반적인 사용 사례

- **자동 그래픽 파이프라인** – 썸네일 생성 전에 실시간으로 감마를 조정합니다.  
- **배치 변환 도구** – 대용량 PSD 아카이브를 밝기 정규화하면서 TIFF로 변환합니다.  
- **웹 서비스** – PSD를 받아 감마 보정을 적용하고 클라이언트가 사용할 수 있도록 TIFF를 반환하는 엔드포인트를 제공합니다.

## 일반적인 문제 및 해결책

| 문제 | 발생 원인 | 해결 방법 |
|-------|----------------|------------|
| **이미지가 씻겨 나간 것처럼 보임** | 감마 값이 너무 높음 (예: > 2.5) | 감마 값을 1.8에서 2.2 사이로 낮추세요. |
| **`rasterImage.isCached()`가 false를 반환함** | 이미지가 아직 메모리에 로드되지 않음 | 감마 조정 전에 `rasterImage.cacheData()`를 호출하세요. |
| **TIFF 파일 크기가 큼** | 샘플당 비트가 16비트로 설정됨 | 예시와 같이 8비트 샘플 (`{8,8,8}`)을 사용하세요. |

## 자주 묻는 질문

**Q: 각 색 채널에 다른 감마 값을 적용할 수 있나요?**  
A: 예 – `adjustGamma` 메서드는 빨강, 초록, 파랑 채널에 대해 별도의 float 값을 허용합니다.

**Q: 저장하기 전에 여러 이미지 조정을 연속으로 적용할 수 있나요?**  
A: 물론입니다. 같은 `RasterImage` 인스턴스에서 크기 조정, 자르기, 색 보정 등을 순차적으로 수행할 수 있습니다.

**Q: Aspose.PSD가 다중 페이지 PSD 파일을 지원하나요?**  
A: 예, 각 레이어에 개별적으로 접근하고 처리할 수 있습니다.

**Q: TIFF 외에 어떤 형식으로 내보낼 수 있나요?**  
A: Aspose.PSD는 PNG, JPEG, BMP 등 다양한 포맷을 해당 옵션 클래스들을 통해 지원합니다.

**Q: 감마 보정 후 색이 바랜 이미지를 어떻게 방지하나요?**  
A: 중간 정도의 감마(약 2.0)로 시작하고 결과를 미리 확인한 뒤 이미지가 너무 밝으면 감마 값을 낮추세요.

## 결론

축하합니다! **java image processing** 워크플로에서 **감마를 조정하는 방법**을 성공적으로 학습하고, PSD를 TIFF로 변환했으며, **색이 바랜 이미지**와 같은 일반적인 함정을 피했습니다. 이 패턴은 밝기와 대비를 세밀하게 제어할 수 있어 자동 그래픽 파이프라인, 웹 서비스 또는 데스크톱 유틸리티에 이상적입니다.

---

**마지막 업데이트:** 2026-08-01  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Java 이미지 처리 튜토리얼 - Aspose.PSD for Java로 이미지 밝기 조정](/psd/java/advanced-techniques/adjust-brightness/)
- [Aspose.PSD for Java로 PSD를 TIFF로 변환하고 대비 조정하는 방법](/psd/java/advanced-techniques/adjust-contrast/)
- [Java에서 PSD를 이미지로 변환 – Aspose.PSD로 조정 레이어 적용](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```