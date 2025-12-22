---
date: 2025-12-21
description: Aspose.PSD for Java, 선도적인 Java 이미지 조작 라이브러리를 사용하여 이미지의 대비를 조정하는 방법을 배우고,
  PSD를 TIFF로 효율적으로 변환하세요.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java를 사용하여 이미지 대비 조정하는 방법
url: /ko/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 이미지 대비 조정하는 방법

## 소개

Java 프로젝트에서 **대비 조정 방법**을 찾고 있다면, 바로 여기가 정답입니다. Aspose.PSD for Java는 강력한 **java image manipulation library**로, 대비, 밝기 등 이미지 속성을 세밀하게 조정할 수 있습니다. 이 튜토리얼에서는 PSD 파일의 대비를 높이고 **PSD를 TIFF로 변환**하는 정확한 단계를 안내합니다.

## 빠른 답변
- **“대비 조정”이란 무엇인가요?** 가장 어두운 픽셀과 가장 밝은 픽셀 사이의 차이를 변경하여 디테일을 돋보이게 합니다.
- **어떤 라이브러리가 이를 처리하나요?** Aspose.PSD for Java – 완전한 이미지 처리 툴킷.
- **라이선스가 필요합니까?** 테스트용 임시 라이선스로 가능하지만, 실제 운영 환경에서는 정식 라이선스가 필요합니다.
- **결과를 TIFF로 저장할 수 있나요?** 네, `TiffOptions`를 사용해 처리된 이미지를 내보낼 수 있습니다.
- **코드 실행 시간은 얼마나 걸리나요?** 일반적인 크기의 PSD 파일은 보통 1초 이하로 실행됩니다.

## 대비 조정이란?
대비 조정은 이미지의 톤 범위를 변경하여 밝은 영역과 어두운 영역 사이의 구분을 강화합니다. 스캔 후 이미지가 평면적으로 보이거나 인쇄용 그래픽을 준비할 때 특히 유용합니다.

## 왜 Aspose.PSD for Java를 사용해야 할까요?
- **Rich format support** – PSD, TIFF, PNG, JPEG 등 다양한 포맷을 열고, 편집하고, 저장할 수 있습니다.
- **High performance** – 캐싱 및 래스터 이미지 최적화를 통해 메모리 사용량을 최소화합니다.
- **Straight‑forward API** – `adjustContrast`와 같은 단일 메서드 호출로 코드를 직관적으로 작성할 수 있습니다.

## 전제 조건

시작하기 전에 다음을 준비하십시오:

- Java 프로그래밍에 대한 기본 지식.
- Aspose.PSD for Java 라이브러리 설치. 라이브러리는 [여기](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

## 패키지 가져오기

Java 클래스에 필요한 import 문을 추가합니다:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 단계 1: 이미지 로드

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

우리는 소스 PSD 파일(`sample.psd`)을 `Image` 객체에 로드합니다. 이 객체는 이후 모든 처리의 진입점 역할을 합니다.

## 단계 2: RasterImage로 캐스팅하고 데이터 캐시

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage`로 캐스팅하면 픽셀 수준의 작업에 접근할 수 있습니다. 캐싱은 특히 큰 파일에서 성능을 크게 향상시킵니다.

## 이미지 대비 조정 방법

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 메서드는 변화 비율을 나타내는 정수를 입력받습니다. 이 예제에서는 대비를 **50 %** 상승시킵니다.

## Aspose.PSD를 사용하여 PSD를 TIFF로 변환

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

여기서는 `TiffOptions`(샘플당 비트 수, 포토메트릭 해석)를 설정하고, 대비가 강화된 이미지를 TIFF 파일로 저장합니다.

## 일반적인 문제 및 해결책
- **Image not cached:** 큰 PSD 파일에서는 `cacheData()`를 반드시 호출하여 `OutOfMemoryError`를 방지하세요.
- **Unexpected color shift:** `setPhotometric`이 목표 색 공간(RGB vs. CMYK)과 일치하는지 확인하세요.
- **File not found:** `dataDir`가 올바른 폴더를 가리키는지, 파일 이름이 정확히 입력되었는지 점검하세요.

## 자주 묻는 질문

### Q1: Aspose.PSD가 다양한 이미지 형식과 호환되나요?

A1: 네, Aspose.PSD는 다양한 이미지 포맷을 지원하여 프로젝트에서 유연하게 활용할 수 있습니다.

### Q2: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

A2: 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

### Q3: Aspose.PSD 문서는 어디에서 찾을 수 있나요?

A3: 문서는 [여기](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

### Q4: Aspose.PSD에 대한 지원 옵션은 무엇이 있나요?

A4: 지원이 필요하면 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34)을 방문하세요.

### Q5: Aspose.PSD를 구매할 수 있나요?

A5: 네, Aspose.PSD는 [여기](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

## 결론

이제 Aspose.PSD for Java를 사용하여 PSD 이미지의 **대비를 조정**하고 **PSD를 TIFF로 변환**하는 방법을 알게 되었습니다. 이러한 단계는 이미지 품질을 세밀하게 제어하면서 코드를 깔끔하고 유지보수하기 쉽게 만들어 줍니다. 필요에 따라 `adjustBrightness`나 `adjustGamma`와 같은 다른 이미지 조정 메서드도 자유롭게 실험해 보세요.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}