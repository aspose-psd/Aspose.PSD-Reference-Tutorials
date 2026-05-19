---
date: 2026-02-27
description: Aspose.PSD를 사용한 Java 이미지 처리에서 감마를 조정하고, PSD를 TIFF로 변환하며, 색이 바랜 이미지를 수정하는
  방법을 간결한 튜토리얼에서 배워보세요.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD를 사용한 Java 이미지 처리에서 감마 조정 방법
url: /ko/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD를 사용한 Java 이미지 처리에서 감마 조정 방법

## 소개

**java 이미지 처리** 작업을 할 때 **감마 조정 방법**을 배우는 것은 밝기와 대비를 디테일을 잃지 않으면서 개선하는 기본 기술입니다. 이 튜토리얼에서는 **Aspose.PSD for Java**를 사용해 PSD 파일에 감마 보정을 적용하고, **PSD를 TIFF로 변환**하며 **색이 흐린 이미지**를 방지하는 방법을 단계별로 살펴봅니다. 이 접근 방식이 빠르고 신뢰할 수 있으며 서버‑사이드 이미지 파이프라인에 최적임을 확인하게 될 것입니다.

## 빠른 답변
- **감마 보정은 무엇을 하나요?** 밝은 영역은 어둡게, 어두운 영역은 밝게 만들어 전체 디테일을 유지하면서 휘도 값을 재매핑합니다.  
- **어떤 라이브러리가 처리를 담당하나요?** Aspose.PSD for Java는 래스터 이미지용 전용 `adjustGamma` 메서드를 제공합니다.  
- **같은 흐름에서 PSD를 TIFF로 변환할 수 있나요?** 예 – 감마 조정 후 `TiffOptions`를 사용해 이미지를 바로 TIFF로 저장할 수 있습니다.  
- **개발에 라이선스가 필요하나요?** 테스트용 무료 체험판을 사용할 수 있으며, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** Aspose.PSD는 Java 8 이상을 지원합니다.

## Java 이미지 처리에서 감마 조정하기
감마 조정은 밝기나 대비를 다루는 **java 이미지 처리 튜토리얼**의 핵심 요소입니다. 아래에서는 단계별로 설명하고, 각 코드 라인이 왜 중요한지, 기존 코드베이스에 어떻게 통합하는지 보여드립니다.

## Java 감마 보정이란?
감마 보정은 인코딩된 픽셀 값과 화면에 표시되는 밝도 사이의 비선형 관계를 변경합니다. 감마 곡선을 조정하면 **색이 흐린 이미지** 문제를 해결하거나 하이라이트를 과다 노출시키지 않으면서 그림자 디테일을 강화할 수 있습니다.

## 왜 Aspose.PSD를 감마 보정에 사용하나요?
Aspose.PSD는 PSD 포맷의 복잡성을 추상화해주는 강력한 **java 이미지 처리 라이브러리**입니다. 색상 프로파일, 캐싱 등을 자동으로 처리하고, 간단한 `adjustGamma` 호출만으로 **java 감마 보정** 및 **PSD를 TIFF로 변환** 워크플로우에 최적화됩니다.

## 사전 준비

1. **Java 개발 환경** – Java 8 이상이 설치되어 있어야 합니다.  
2. **Aspose.PSD 라이브러리** – JAR 파일을 다운로드하여 프로젝트에 추가합니다. 공식 [documentation](https://reference.aspose.com/psd/java/)을 참고하세요.  
3. **샘플 이미지** – 처리하려는 PSD 파일 (예: `sample.psd`).  

## 패키지 가져오기

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

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

**팁:** 래스터 데이터를 한 번 캐시하면 연속으로 여러 조정을 적용할 때 메모리 사용량을 줄일 수 있습니다.

## 단계 2: 감마 조정

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

필요에 따라 빨강, 초록, 파랑 채널별로 다른 값을 전달해 채널별 미세 조정도 가능합니다.

## 단계 3: TiffOptions 생성

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

8‑비트 샘플(`{8,8,8}`)을 사용하면 TIFF 파일 크기를 적절히 유지하면서 색 정확성을 보존합니다.

## 단계 4: 결과 이미지 저장

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

저장 후에는 TIFF 파일을 인쇄 서비스나 웹 API와 같은 다운스트림 시스템에 전달할 수 있습니다.

## 일반적인 사용 사례

- **자동 그래픽 파이프라인** – 썸네일을 생성하기 전에 실시간으로 감마를 조정합니다.  
- **배치 변환 도구** – 대용량 PSD 아카이브를 밝기 정규화와 함께 TIFF로 변환합니다.  
- **웹 서비스** – PSD를 받아 감마 보정을 적용하고 TIFF를 반환하는 엔드포인트를 제공합니다.

## 흔히 발생하는 문제와 해결책

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Image appears washed out** | Gamma value too high (e.g., > 2.5) | Lower the gamma factor to a value between 1.8 and 2.2. |
| **`rasterImage.isCached()` returns false** | Image not yet loaded into memory | Call `rasterImage.cacheData()` before adjusting gamma. |
| **TIFF file size is large** | Bits per sample set to 16‑bit | Use an 8‑bit sample (`{8,8,8}`) as shown in the example. |

## 자주 묻는 질문

**Q: 각 색상 채널에 다른 감마 값을 적용할 수 있나요?**  
A: 예 – `adjustGamma` 메서드는 빨강, 초록, 파랑 채널에 대한 별도 float 값을 받습니다.

**Q: 저장하기 전에 여러 이미지 조정을 연속으로 적용할 수 있나요?**  
A: 물론입니다. 같은 `RasterImage` 인스턴스에서 리사이징, 크롭, 색 보정 등을 순차적으로 수행할 수 있습니다.

**Q: Aspose.PSD가 다중 페이지 PSD 파일을 지원하나요?**  
A: 예, 각 레이어에 개별적으로 접근하여 처리할 수 있습니다.

**Q: TIFF 외에 어떤 포맷으로 내보낼 수 있나요?**  
A: Aspose.PSD는 PNG, JPEG, BMP 등 다양한 포맷을 해당 옵션 클래스를 통해 지원합니다.

**Q: 감마 보정 후 색이 흐린 이미지를 방지하려면 어떻게 해야 하나요?**  
A: 중간 정도의 감마(약 2.0)부터 시작하고 결과를 미리 확인한 뒤, 이미지가 너무 밝으면 감마 값을 낮춥니다.

## 결론

축하합니다! 이제 **java 이미지 처리** 워크플로우에서 **감마 조정 방법**을 익히고, PSD를 TIFF로 변환하며 **색이 흐린 이미지**와 같은 일반적인 함정을 피하는 방법을 마스터했습니다. 이 패턴은 밝기와 대비를 세밀하게 제어할 수 있어 자동 그래픽 파이프라인, 웹 서비스, 데스크톱 유틸리티 등에 최적입니다.

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}