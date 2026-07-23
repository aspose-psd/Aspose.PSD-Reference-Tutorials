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

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java를 사용하여 PSD를 TIFF로 변환하고 대비 조정하는 방법

## 소개

그래픽의 표현 품질을 조정하면서 **PSD를 TIFF로 변환**해야 하는 경우, 여기가 바로 원하는 곳입니다. 이 튜토리얼에서는 강력하게 **java 이미지 조작** 라이브러리인 Aspose.PSD for Java를 전체 작업 플로우를 통해 살펴봅니다. **이미지 대비 조정**을 강화하고, 배터리 래스터 데이터를 강화하여 성능을 향상시키고, 마지막으로 **이미지를 TIFF로 저장**하여 처리하는 방식을 활용하는 방법을 배웁니다. 를 방해하다!

## 빠른 답변
- **대비 조정**은 무엇을 의미하는건가요? 가장 밝은 아치형과 가장 밝은 아치형의 변형을 통해 변형을 돋보이게 합니다.
- **어떤 라이벌이 담당하는가요?** Aspose.PSD for Java – 전체 기능을 담당하는 이미지 처리 툴킷.
- **라이선스가 필요합니까?**용 **임시 라이선스**는 작동하지만, 클러스터에서는 클러스터가 필요합니다.
- **PSD를 TIFF로 변환할 수 있을까요?** 물론입니다 – 처리된 이미지를 제공하기 위해 `TiffOptions`를 사용합니다.
- **코드 실행 시간은 얼마든지 걸리나요?** 최신 하드웨어에서 일반 크기의 PSD 파일은 보통 1초 미만입니다.

## 이미지 대비 조정이란 무엇입니까?

대비는 이미지의 톤 범위를 변경하여 어두운 영역 사이의 구분을 강화합니다. 스캔 후 이미지가 잘 보이거나 인쇄용 그래픽을 준비할 때 특히 유용합니다.

## Java용 Aspose.PSD를 사용하는 이유는 무엇입니까?
- **풍부한 형식 지원** – 직접, 편집 및 **TIFF로 이미지 저장**, PNG, JPEG 등 다양한 용도로 디버깅할 수 있습니다.
- **고성능** – 캐싱 및 새스터 이미지 최적화를 통해 메모리 드라이버의 외부 PSD 파일 처리에 참여합니다.
- **간단한 API** – `adjustContrast`와 같은 단일 메서드 호출로 코드가 독성과 유지 보수성을 강화합니다.
- **포괄적인 Java 이미지 조작**을 제공하는 기능을 통해 다양한 기능까지 모두에게 적합합니다.

## 전제 조건

시작하기 전에 다음 준비를 하셔야 합니다:

- Java 프로그래밍에 대한 기본 지식.
- Aspose.PSD for Java 라이브러리 설치. 라이브러리는 [여기](https://releases.aspose.com/psd/java/) 에서 다운로드할 수 있습니다.

## 패키지 가져오기

Java 클래스에 필요한 가져오기를 추가합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1단계: 이미지 불러오기

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

우리는 소스 PSD 파일(`sample.psd`)을 `Image` 객체에 로드합니다. 이 객체는 이후 모든 처리를 위한 진입점 역할을 합니다.

## 2단계: 래스터 이미지로 변환 및 데이터 캐싱

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage`로 캐스팅하면 픽셀 수준 작업에 접근할 수 있습니다. 캐싱을 통해 특히 큰 파일의 성능이 크게 향상됩니다.

## 이미지 대비 조정 방법

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` 메서드는 변화 비율을 나타내는 정수를 인수로 받습니다. 이 예제에서는 대비를 **50 %** 상승시킵니다.

## Aspose를 사용하여 PSD를 TIFF로 변환하기.PSD

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

## 일반적인 문제 및 해결 방법
- **이미지가 캐시되지 않음:** 주최 PSD 파일에서 `cacheData()`를 호출하여 `OutOfMemoryError`를 방지합니다.
- **예기치 않은 색상 변화:** `setPhotometric`이 목표 색 공간(RGB vs. CMYK)과 일치하는지 확인하십시오.
- **파일을 찾을 수 없습니다:** `dataDir`이 올바른 폴더를 포함하고 파일 이름을 입력해야 합니다.

## 자주 묻는 질문

### Q1: Aspose.PSD가 다양한 이미지를 포맷하고 호환되나요?

A1: 네, Aspose.PSD는 다양한 이미지 제출을 지원하므로 프로젝트에서 유연하게 처리할 수 있습니다.

### Q2: Aspose.PSD 기동은 어떻게 보내나요?

A2: 기적은 [여기](https://purchase.aspose.com/temporary-license/) 에서 보낼 수 있습니다.

### Q3: Aspose.PSD 문서는 찾을 수 없나요?

A3: 문서는 [여기](https://reference.aspose.com/psd/java/) 에서 처리할 수 있습니다.

### Q4: Aspose.PSD 지원 옵션은 어떤 것이 있나요?

A4: 지원이 필요하면 [Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 에서 문의하십시오.

### Q5: Aspose.PSD를 구매할 수 있나요?

A5: 네, Aspose.PSD는 [여기](https://purchase.aspose.com/buy) 에서 구매할 수 있습니다.

## 결론

이제 Aspose.PSD for Java를 사용하여 **PSD를 TIFF로 변환**하고 **이미지 비교**를 수행하는 방법을 더 잘 이해합니다. 이러한 단계는 코드 품질을 세밀하게 제어하면서 개선을 유지하기 쉽게 만드는 것입니다. 필요에 따라 `adjustBrightness`나 `adjustGamma`와 같은 다른 조정 방법을 실험해 보세요.

---

**최종 업데이트:** 2026년 2월 25일
**테스트 환경:** Aspose.PSD for Java 24.12
**제작자:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}