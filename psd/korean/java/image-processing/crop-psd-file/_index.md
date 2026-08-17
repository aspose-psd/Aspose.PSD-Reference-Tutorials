---
date: 2026-08-17
description: Aspose.PSD for Java를 사용하여 Java에서 PSD 파일을 자르는 방법을 배우세요 – Java 애플리케이션에서
  Photoshop 문서를 빠르고 정확하게 다듬는 방법입니다.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: PSD 파일 자르기
og_description: Aspose.PSD for Java를 사용하여 Java PSD 파일을 자릅니다. 이 가이드는 코드 없이도 Photoshop
  파일을 효율적으로 다듬는 단계별 방법과 모범 사례 팁을 제공합니다.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Aspose.PSD와 함께 Java PSD 파일 자르기 – 빠른 이미지 크롭
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Aspose.PSD를 사용한 Java PSD 파일 자르기
url: /ko/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD를 사용한 Java에서 PSD 파일 자르기

## 소개

프로그램matically 포토샵 문서를 잘라야 할 경우, **crop psd file java**는 그래픽 파이프라인, 에셋 파이프라인 또는 자동화된 디자인 워크플로우에서 작업하는 Java 개발자에게 흔한 작업입니다. Aspose.PSD for Java는 사각형을 정의하고 몇 줄의 코드만으로 필요한 영역을 추출할 수 있는 전용 API를 제공합니다. 이 튜토리얼에서는 라이브러리가 고성능 크롭을 위해 설계된 이유, 환경 설정 방법, 그리고 PSD와 PNG 결과물을 생성하는 정확한 단계를 배웁니다.

## 빠른 답변
- **Java에서 PSD 자르기를 처리하는 라이브러리는 무엇입니까?** Aspose.PSD for Java.
- **기본 자르기를 위해 필요한 코드 라인은 몇 줄입니까?** 이미지를 로드한 후 두 번의 API 호출.
- **잘린 영역을 PNG로 내보낼 수 있나요?** 예, 내장된 PNG 저장 옵션을 사용합니다.
- **프로덕션 사용에 라이선스가 필요합니까?** 평가 기간 이후에는 상업용 라이선스가 필요합니다.
- **지원되는 Java 버전은 무엇입니까?** Java 8 및 이후 버전, Java 11, 17, 21 포함.

## crop psd file java는 무엇인가요?

crop psd file java는 Java 코드를 사용하여 Photoshop Document(.psd)에서 사각형 영역을 프로그래밍 방식으로 잘라내는 과정을 의미합니다. Aspose.PSD를 사용하면 포토샵을 실행하지 않고도 이 작업을 수행할 수 있어 서버‑사이드 이미지 파이프라인에 이상적입니다.

## 왜 Aspose.PSD for Java를 사용해야 할까요?

Aspose.PSD는 **30개 이상의 입력 및 출력 형식**을 지원하며 스트리밍 아키텍처 덕분에 전체 문서를 메모리에 로드하지 않고도 **500 MB**까지의 PSD 파일을 처리할 수 있습니다. 라이브러리는 레이어, 마스크 및 색상 프로파일을 보존하여 포토샵의 네이티브 출력과 일치하는 크롭 결과를 제공합니다. 이러한 정량화된 성능 덕분에 일반 하드웨어에서도 예측 가능한 메모리 사용량으로 배치 작업을 처리할 수 있습니다.

## 전제 조건

- **Java 개발 환경** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.
- **Aspose.PSD for Java** – 최신 JAR 및 문서를 다운로드하십시오 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **샘플 PSD 파일** – 프로젝트 디렉터리 안에 .psd 파일을 배치하여 코드가 찾을 수 있도록 합니다.

## Java에서 PSD 파일을 자르는 방법은?

소스 파일을 로드하고, 유지하려는 사각형을 정의한 뒤, 크롭을 적용하고, 원하는 형식으로 결과를 저장합니다. 전체 워크플로는 다섯 단계로 구성되며, 각 단계마다 코드를 삽입할 자리 표시자가 제공됩니다.

### 1단계: 문서 디렉터리 설정

“Your Document Directory”를 PSD 파일이 들어 있는 절대 경로나 상대 경로로 교체하십시오.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### 2단계: PSD 파일 로드

`RasterImage` 클래스는 PSD 파일에 대한 래스터 기반 작업을 수행하기 위한 Aspose.PSD의 진입점입니다. 파일을 로드하면 메모리 내 표현이 생성되어 조작할 수 있습니다.

```java
String dataDir = "Your Document Directory";
```

### 3단계: 자르기 영역 정의

`Rectangle`은 유지할 영역의 X, Y 좌표와 너비·높이를 정의합니다. 이 클래스는 표준 Java AWT 패키지의 일부이며 Aspose.PSD에서 크롭 경계를 지정하는 데 사용됩니다.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### 4단계: 잘린 PSD 저장

크롭을 적용한 후 결과를 PSD 형식으로 다시 저장할 수 있습니다. 라이브러리는 원본 색상 모드와 비트 깊이를 유지하면서 잘린 픽셀만 기록합니다.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### 5단계: 잘린 이미지를 PNG로 저장

웹 친화적인 버전이 필요하면 잘린 래스터를 PNG로 내보냅니다. Aspose.PSD는 압축 수준 및 인터레이싱을 제어할 수 있는 PNG 저장 옵션을 제공합니다.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## 일반적인 문제와 해결책

- **잘못된 사각형 좌표** – X/Y 값이 왼쪽 위 모서리에서 0부터 시작하는지 확인하십시오; 음수 값은 `ArgumentException`을 발생시킵니다.
- **대용량 파일에서 메모리 급증** – 숨겨진 레이어가 필요 없을 경우 `loadOptions.setLoadOnlyVisibleLayers(true)` 옵션을 사용하여 메모리 사용량을 줄이십시오.
- **색상 프로파일 손실** – 크롭 전 `image.getColorProfile()`을 호출하여 원본 ICC 프로파일을 보존하고, 작업 후 다시 할당하십시오.

## 자주 묻는 질문

### Q1: Aspose.PSD for Java를 사용하여 다른 형식의 이미지를 자를 수 있나요?

A1: Aspose.PSD는 주로 PSD 파일을 대상으로 하지만 BMP, GIF, JPEG, PNG, TIFF 등 여러 래스터 형식의 입력 및 출력도 지원합니다.

### Q2: Aspose.PSD for Java가 대규모 이미지 처리에 적합한가요?

A2: 예. 라이브러리의 스트리밍 아키텍처는 메모리 사용량을 100 MB 이하로 유지하면서 수백 페이지에 달하는 PSD 파일을 처리할 수 있어 배치 작업에 이상적입니다.

### Q3: Aspose.PSD for Java를 사용할 때 라이선스와 관련된 고려 사항이 있나요?

A3: 프로덕션 배포에는 상업용 라이선스가 필요합니다. 자세한 내용은 [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy)에서 확인하십시오.

### Q4: Aspose.PSD for Java와 관련된 문제에 대한 지원을 어떻게 받을 수 있나요?

A4: [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34)에서 질문을 올리고 코드 스니펫을 공유하면 커뮤니티와 제품 엔지니어로부터 도움을 받을 수 있습니다.

### Q5: 구매 전에 Aspose.PSD for Java를 체험해 볼 수 있나요?

A5: 예, 완전 기능을 갖춘 무료 체험판을 [Aspose.PSD free trial download](https://releases.aspose.com/)에서 다운로드할 수 있습니다.

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## 관련 튜토리얼

- [Aspose.PSD for Java에서 사각형으로 이미지 자르기](/psd/java/image-editing/crop-image-by-rectangle/)
- [Aspose.PSD for Java에서 이동으로 이미지 자르기](/psd/java/image-editing/crop-image-by-shifts/)
- [Aspose.PSD를 사용한 Java 이미지 회전 방법](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}