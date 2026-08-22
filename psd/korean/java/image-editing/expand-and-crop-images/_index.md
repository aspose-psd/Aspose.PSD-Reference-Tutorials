---
date: 2026-07-08
description: 'Java 이미지 편집 라이브러리 튜토리얼: Aspose.PSD for Java를 사용하여 Java에서 이미지를 자르고, 리사이즈하고,
  캔버스를 확장하며, PSD를 JPEG로 변환하는 방법을 배웁니다.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: 캔버스 확장 및 이미지 자르기
og_description: Java 이미지 편집 라이브러리 튜토리얼에서는 Aspose.PSD for Java를 사용하여 몇 분 만에 이미지를 자르고,
  캔버스를 확장하며, PSD를 JPEG로 변환하는 방법을 보여줍니다.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java 이미지 편집 라이브러리 – Aspose.PSD로 이미지 자르기
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java 이미지 편집 라이브러리 – Aspose.PSD로 이미지 자르기
url: /ko/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 이미지 편집 라이브러리: Aspose.PSD를 사용한 Java 이미지 자르기

## 소개

이 튜토리얼에서는 **java image editing library**—특히 Aspose.PSD for Java—를 사용하여 PSD 파일을 자르고, 확장하고, JPEG로 변환하는 방법을 배웁니다. 웹 포털용 자산을 준비하거나 썸네일 생성을 자동화하든, 아래 단계는 반복 가능한 프로덕션‑레디 워크플로우를 제공하며 Java 8+ 프로젝트에 통합할 수 있습니다.

## 빠른 답변
- **crop image java를 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java.  
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트가 가능하며, 프로덕션에서는 상업용 라이선스가 필요합니다.  
- **자르면서 PSD를 JPEG로 변환할 수 있나요?** 예, `JpegOptions`와 자르기 사각형을 함께 사용하면 됩니다.  
- **Java 8을 지원하나요?** Aspose.PSD는 Java 8 및 이후 버전을 지원합니다.  
- **구현에 얼마나 걸리나요?** 기본 자르기 작업은 일반적으로 10분 미만 소요됩니다.

## “crop image java”란 무엇인가요?

Crop image java는 원본 이미지에서 사각형 영역을 선택하고 해당 영역 외부를 버리는 것을 의미합니다. Aspose.PSD를 사용하면 영역을 정의하는 `Rectangle`을 생성하고 이를 `RasterImage`에 적용한 뒤 JPEG와 같은 지원 포맷으로 결과를 저장합니다.

## Java 이미지 자르기에 Aspose.PSD를 사용하는 이유

Aspose.PSD는 PSD 파일을 네이티브로 처리하고 100개 이상의 레이어 기능을 지원하며, 메모리 사용량을 500 MB 이하로 유지하면서 최대 10 000 × 10 000 픽셀 이미지를 처리할 수 있는 **java image editing library**를 제공합니다. 또한 JPEG, PNG, BMP 등으로의 내장 변환을 제공하므로 외부 도구가 필요 없습니다. 이는 대량 처리 파이프라인을 빠르고 안정적이며 유지 관리가 용이하게 합니다.

## 사전 요구 사항

1. **Java Development Kit (JDK)** – Java 8 이상이 설치되어 있어야 합니다.  
2. **Aspose.PSD for Java** – 공식 사이트에서 라이브러리를 다운로드하십시오 **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** `ClassNotFoundException`을 방지하려면 Aspose.PSD JAR를 프로젝트의 클래스패스 또는 Maven/Gradle 의존성에 추가하십시오.

## 패키지 가져오기

Java 소스 파일에 필요한 import 문을 추가하십시오. 이러한 클래스는 이미지 로드, 래스터 조작, 사각형 정의 및 JPEG 내보내기 옵션에 접근할 수 있게 해줍니다.

## Aspose.PSD를 사용한 Java 이미지 자르기 방법

`RasterImage`로 원본 PSD를 로드하고, 자르기 영역을 설명하는 `Rectangle`을 정의합니다(음수 좌표는 캔버스를 확장할 수 있음). 마지막으로 `JpegOptions`로 결과를 저장합니다. 이 3단계 흐름은 자르기와 포맷 변환을 한 번에 처리하여 중간 파일이 필요하지 않습니다.

## 단계 1: 문서 디렉터리 설정

원본 PSD 파일이 들어 있는 폴더를 지정하십시오. 자리표시자를 실제 경로로 교체하세요.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 단계 2: 소스 및 대상 경로 지정

PSD를 읽을 위치와 자른 JPEG를 쓸 위치를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 단계 3: 이미지 로드 및 캐시

`RasterImage`는 메모리 내에서 PSD 파일의 래스터화된 버전을 나타냅니다.  
PSD를 `RasterImage` 객체에 로드합니다. 캐싱은 자르기와 같은 후속 작업의 성능을 향상시킵니다.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## 단계 4: 자르기용 Rectangle 생성

`Rectangle`는 자르기 영역의 X, Y 좌표와 너비/높이를 정의합니다.  
보관하려는 영역을 설명하는 `Rectangle`을 생성합니다. 좌표를 음수로 지정하면 자르기 전에 캔버스를 **확장**할 수 있으며, 이는 원본 이미지 주변에 테두리를 추가할 때 유용합니다.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **왜 음수 좌표를 사용하나요?**  
> 음수 X/Y 값은 자르기 영역을 왼쪽/위쪽으로 이동시켜 최종 자르기 전에 원본 콘텐츠 주변에 빈 공간(확장)을 효과적으로 추가합니다.

## 단계 5: 자른 이미지 저장

`JpegOptions`는 품질 및 압축과 같은 JPEG 출력 설정을 지정합니다.  
마지막으로 `JpegOptions`를 사용해 결과 이미지를 저장합니다. 이 단계는 자르기 사각형을 적용하면서 **convert psd jpeg**를 보여줍니다.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Result:** `jpeg_out.jpg`는 이제 각 측면이 200 px씩 확장된 후 정의된 사각형으로 잘린 300 × 300 픽셀 이미지를 포함합니다.

축하합니다! **java image cropping**을 성공적으로 수행했고, 캔버스를 확장했으며, PSD 파일을 JPEG로 변환했습니다—모두 몇 줄의 간결한 코드로 이루어졌습니다.

## 일반적인 사용 사례

- **웹용 자산 준비** – 업로드 전에 스크린샷이나 디자인을 자르고 크기를 조정합니다.  
- **썸네일 생성** – 미리보기 용도로 큰 PSD에서 특정 영역을 추출합니다.  
- **자동 배치 처리** – PSD 파일이 들어 있는 폴더를 순회하면서 동일한 자르기 사각형을 각 파일에 적용합니다.

## 문제 해결 및 팁

| 문제 | 제안된 해결책 |
|-------|----------------|
| `OutOfMemoryError` when loading large PSDs | `rasterImage.cacheData()`를 일찍 호출하고 JVM 힙 크기(`-Xmx`)를 늘리는 것을 고려하십시오. |
| Cropped area is off‑center | 사각형의 X/Y 오프셋을 확인하십시오; 음수 값은 캔버스를 확장한다는 점을 기억하세요. |
| Output JPEG looks blurry | `JpegOptions` 품질 설정을 조정하십시오(예: `new JpegOptions { Quality = 90 }`). |

## 자주 묻는 질문

### Q1: Aspose.PSD가 다양한 Java 버전과 호환되나요?

A1: 예, Aspose.PSD는 Java 8, 11, 17 및 최신 릴리스를 지원하므로 다양한 개발 환경에서 폭넓은 호환성을 보장합니다.

### Q2: Aspose.PSD를 상업 프로젝트에 사용할 수 있나요?

A2: 물론입니다. Aspose.PSD는 개발자를 위한 상업용 라이선스를 제공하므로 개인 및 상업용 애플리케이션 모두에 사용할 수 있습니다.

### Q3: 지원되는 이미지 파일 포맷에 제한이 있나요?

A3: Aspose.PSD는 PSD, JPEG, PNG, BMP, TIFF 등을 포함한 30개 이상의 이미지 포맷을 지원합니다. 전체 목록은 [documentation](https://reference.aspose.com/psd/java/)을 참고하십시오.

### Q4: Aspose.PSD 관련 문의에 대한 지원은 어떻게 받을 수 있나요?

A4: 커뮤니티 또는 Aspose 지원팀에 도움을 요청하려면 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)을 방문하십시오.

### Q5: 무료 체험판이 있나요?

A5: 예, 무료 체험판으로 Aspose.PSD를 체험할 수 있습니다. [here](https://releases.aspose.com/)에서 다운로드하십시오.

**마지막 업데이트:** 2026-07-08  
**테스트 환경:** Aspose.PSD for Java 24.12  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## 관련 튜토리얼

- [Aspose.PSD를 사용한 간단한 리사이징 – Java 이미지 조작 라이브러리](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java로 이미지 270도 회전하는 방법](/psd/java/advanced-image-manipulation/rotate-image/)
- [Aspose.PSD를 사용한 Java 이미지 처리에서 감마 조정 방법](/psd/java/advanced-techniques/adjust-gamma/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}