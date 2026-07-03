---
date: 2026-07-03
description: Aspose.PSD for Java를 사용하여 Java 이미지 자르는 방법을 배웁니다. 이 단계별 이미지 자르기 튜토리얼에서는
  PSD 파일 로드, 시프트 값 설정 및 결과 저장에 대해 다룹니다.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: 시프트로 이미지 자르기
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD와 함께하는 Java 이미지 시프트 자르기
url: /ko/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD와 함께 이동을 사용한 Java 이미지 자르기

## 소개

Java 이미지 처리에서 **crop image java**는 그래픽, 썸네일 또는 UI 자산을 준비할 때 흔히 요구되는 작업입니다. Aspose.PSD for Java는 지원되는 모든 래스터 형식에서 작동하는 간단한 `crop` 메서드를 제공하여 이 작업을 쉽게 수행할 수 있게 합니다. 이 튜토리얼에서는 PSD 파일을 로드하고, 좌‑우‑상‑하 이동 값을 정의하고, 자르기를 적용한 뒤 결과를 저장하는 방법을 배웁니다—맞춤형 픽셀 조작 코드를 작성할 필요 없이.

## 빠른 답변
- **크롭을 처리하는 라이브러리는 무엇인가요?** Aspose.PSD for Java는 내장된 `crop` 메서드를 제공합니다.  
- **라이선스가 필요합니까?** 평가용으로는 임시 라이선스로 충분하지만, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **지원되는 형식은?** PSD, JPEG, PNG, BMP, TIFF 등을 포함한 30개 이상의 래스터 형식을 지원합니다.  
- **최대 파일 크기는?** 전체 이미지를 메모리에 로드하지 않고도 2 GB까지의 파일을 처리할 수 있습니다.  
- **코드 라인은 몇 줄인가요?** 로드, 캐시, 이동 정의, 크롭, 저장의 다섯 단계만 필요합니다.

## crop image java란 무엇인가요?
`crop image java`는 Java 애플리케이션에서 비트맵을 잘라내는 작업을 의미합니다. Aspose.PSD를 사용하면 이미지 각 면에 대한 이동 값을 받아 새로운 이미지 인스턴스를 반환하는 `crop` 메서드로 이 작업을 수행합니다.

## 이미지 크롭에 Aspose.PSD를 사용하는 이유는?
Aspose.PSD는 **30개 이상의** 이미지 형식을 지원하며, 150 MB 미만의 RAM을 사용하면서 수백 페이지에 달하는 PSD 파일을 처리할 수 있습니다. 이는 지연 로딩 아키텍처 덕분입니다. 또한 라이브러리는 픽셀 단위로 정확한 결과를 보장하며, 레이어, 마스크, 컬러 프로파일을 보존합니다—많은 일반 이미지 라이브러리가 제공하지 못하는 기능입니다.

## 전제 조건

### Java 개발 키트 (JDK)

시스템에 최신 버전의 JDK가 설치되어 있는지 확인하십시오. [here](https://www.oracle.com/java/technologies/javase-downloads.html)에서 다운로드할 수 있습니다.

### Aspose.PSD for Java 라이브러리

시작하려면 Aspose.PSD for Java 라이브러리를 받아야 합니다. [download page](https://releases.aspose.com/psd/java/)에서 최신 버전을 다운로드하십시오.

### 통합 개발 환경 (IDE)

Eclipse 또는 IntelliJ와 같은 선호하는 Java IDE를 선택하여 원활한 코딩 환경을 구축하십시오.

## crop image java를 어떻게 수행하나요?

소스 파일을 로드하고 각 면에 대한 픽셀 이동 값을 정의한 뒤 `crop` 메서드를 호출하면 됩니다—전체 워크플로는 다섯 줄의 간결한 코드로 작성할 수 있습니다. `crop` 작업은 지정한 영역만 포함하는 새로운 이미지를 생성하며, 원본 파일은 그대로 유지됩니다.

### 1단계: 이미지 로드

`Image`는 Aspose.PSD에서 모든 이미지 유형의 기본 클래스입니다.  
`RasterImage`는 래스터 이미지를 나타내며 크롭 기능을 제공합니다.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 2단계: 이미지 데이터 캐시

`cacheData()`는 이미지 데이터를 메모리로 로드하여 처리 속도를 높입니다.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### 3단계: 이동 값 정의

이미지의 네 면(왼쪽, 위, 오른쪽, 아래)에 대한 이동 값을 픽셀 단위로 지정합니다.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### 4단계: 크롭 적용

`crop(left, right, top, bottom)`은 지정된 픽셀 이동 값에 따라 이미지 각 면을 잘라냅니다.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### 5단계: 결과 저장

`JpegOptions`는 품질 및 컬러 프로파일과 같은 JPEG 인코딩 설정을 정의합니다.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

축하합니다! Aspose.PSD for Java를 사용하여 이미지를 성공적으로 크롭했습니다.

## 일반적인 문제 및 해결책

- **이미지가 변경되지 않음:** 이동 값이 양수이며 원본 차원을 초과하지 않는지 확인하십시오.  
- **대용량 파일에서 OutOfMemoryError:** 2단계에서 보여준 대로 캐싱을 활성화하십시오; 이렇게 하면 전체 이미지를 RAM에 유지하는 대신 임시 파일을 사용하게 됩니다.  
- **크롭 후 색상 변동:** 정확한 색상 일치를 위해 `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })`를 호출하여 컬러 프로파일을 보존하십시오.

## 자주 묻는 질문

**Q:** Aspose.PSD가 모든 이미지 형식과 호환되나요?  
**A:** 예, Aspose.PSD는 PSD, JPEG, PNG, BMP, TIFF, GIF 등을 포함한 30개 이상의 래스터 형식을 지원하여 광범위한 호환성을 보장합니다.

**Q:** 같은 이미지에 여러 번 크롭 작업을 적용할 수 있나요?  
**A:** 물론입니다. 각 `crop` 호출 후 새로운 이미지 객체를 받으며, 필요에 따라 다시 크롭할 수 있습니다.

**Q:** Aspose.PSD 지원을 위한 커뮤니티 포럼이 있나요?  
**A:** 예, [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)에서 지원을 받고 커뮤니티와 소통할 수 있습니다.

**Q:** Aspose.PSD 임시 라이선스를 어떻게 얻을 수 있나요?  
**A:** 임시 라이선스를 얻으려면 [here](https://purchase.aspose.com/temporary-license/)를 방문하십시오.

**Q:** Aspose.PSD 기능을 보여주는 샘플 프로젝트가 있나요?  
**A:** [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/)에서 문서와 예제를 확인하십시오.

---

**마지막 업데이트:** 2026-07-03  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## 관련 튜토리얼

- [Aspose.PSD for Java에서 사각형으로 이미지 자르기](/psd/java/image-editing/crop-image-by-rectangle/)
- [Java 이미지 자르기 - Aspose.PSD for Java로 이미지 확장 및 크롭](/psd/java/image-editing/expand-and-crop-images/)
- [Java 이미지 크기 조정 - Aspose.PSD for Java에서 Resize Type 열거형 사용](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}