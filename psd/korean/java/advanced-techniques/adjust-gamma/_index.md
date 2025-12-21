---
date: 2025-12-21
description: Aspose.PSD를 사용하여 이미지 감마를 조정함으로써 Java 이미지 처리를 수행하는 방법을 배워보세요. PSD를 TIFF로
  변환하고 감마 보정을 적용하는 단계별 가이드.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java 이미지 처리 – Aspose.PSD로 감마 조정
url: /ko/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 이미지 처리 – Aspose.PSD로 감마 조정

## 소개

**java image processing** 작업을 하고 있다면, 사진의 감마를 조정하는 것은 디테일을 잃지 않으면서 밝기와 대비를 개선하는 기본 기술입니다. 이 튜토리얼에서는 **Aspose.PSD for Java**를 사용하여 PSD 파일에 감마 보정을 적용하고 결과를 TIFF 이미지로 내보내는 방법을 단계별로 안내합니다. 이 방법이 빠르고 신뢰성이 높으며 서버‑사이드 이미지 파이프라인에 최적임을 확인할 수 있습니다.

## 빠른 답변
- **감마 보정은 무엇을 하나요?** 밝기 값을 재매핑하여 어두운 영역은 밝게, 밝은 영역은 어둡게 만들면서 전체 디테일을 유지합니다.  
- **어떤 라이브러리가 처리를 담당하나요?** Aspose.PSD for Java는 래스터 이미지용 전용 `adjustGamma` 메서드를 제공합니다.  
- **같은 흐름에서 PSD를 TIFF로 변환할 수 있나요?** 예 – 감마 조정 후 `TiffOptions`를 사용해 이미지를 바로 TIFF 형식으로 저장할 수 있습니다.  
- **개발에 라이선스가 필요합니까?** 테스트용으로는 무료 체험판을 사용할 수 있으며, 실제 운영에서는 상용 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** Aspose.PSD는 Java 8 이상을 지원합니다.

## java 이미지 처리란?

Java 이미지 처리는 Java 라이브러리를 사용해 시각 데이터를 조작, 분석 및 변환하는 것을 의미합니다. 작업에는 크기 조정, 필터링, 색 보정, 포맷 변환 등이 포함되며, 이 모든 작업을 데스크톱 또는 웹 애플리케이션에서 자동화할 수 있습니다.

## 왜 Aspose.PSD를 감마 보정에 사용하나요?

Aspose.PSD는 PSD 포맷의 복잡성을 추상화한 고수준 API를 제공하여 실제 이미지 조정에 집중할 수 있게 합니다. 캐싱, 색 프로파일을 처리하고 간단한 `adjustGamma` 호출을 제공하므로 **이미지 감마 보정** 및 **psd를 tiff로 변환** 워크플로에 이상적입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 준비되어 있는지 확인하세요:

1. **Java 개발 환경** – 시스템에 Java 개발 환경이 설치되어 있는지 확인합니다.  
2. **Aspose.PSD 라이브러리** – Aspose.PSD 라이브러리를 다운로드하여 Java 프로젝트에 통합합니다. 필요한 리소스는 [documentation](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.  
3. **샘플 이미지** – 감마 조정에 사용할 샘플 PSD 이미지를 준비합니다.

## 패키지 가져오기

프로세스를 시작하려면 Java 프로젝트에 필요한 패키지를 가져옵니다. 이렇게 하면 Aspose.PSD 기능을 원활하게 사용할 수 있는 기반이 마련됩니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 단계 1: 이미지 로드

`RasterImage` 클래스의 인스턴스로 샘플 PSD 이미지를 로드합니다. 이는 이후 감마 조정의 기반이 됩니다.

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

## 단계 2: 감마 조정

이제 `adjustGamma` 메서드를 사용해 로드된 이미지의 감마를 조정합니다. 요구 사항에 맞게 감마 값을 미세 조정하세요.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 단계 3: TiffOptions 생성

결과 이미지에 대한 `TiffOptions` 인스턴스를 생성합니다. 샘플당 비트 수와 포토메트릭 옵션 등 다양한 속성을 설정하여 출력이 요구 사항에 맞도록 조정합니다.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 단계 4: 결과 이미지 저장

앞서 정의한 `TiffOptions`를 사용해 조작된 이미지를 TIFF 형식으로 저장합니다.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 일반적인 문제 및 해결책

| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| **이미지가 색이 바래 보임** | 감마 값이 너무 높음 (예: > 2.5) | 감마 계수를 1.8~2.2 사이 값으로 낮춥니다. |
| **`rasterImage.isCached()`가 false 반환** | 이미지가 아직 메모리에 로드되지 않음 | 감마 조정 전에 `rasterImage.cacheData()`를 호출합니다. |
| **TIFF 파일 크기가 큼** | 샘플당 비트 수가 16‑bit로 설정됨 | 예시와 같이 8‑bit 샘플 (`{8,8,8}`)을 사용합니다. |

## 자주 묻는 질문

**Q: 각 색 채널에 서로 다른 감마 값을 적용할 수 있나요?**  
A: 예 – `adjustGamma` 메서드는 빨강, 초록, 파랑 채널에 대한 별도 float 값을 받습니다.

**Q: 저장하기 전에 여러 이미지 조정을 연속으로 적용할 수 있나요?**  
A: 물론입니다. 동일한 `RasterImage` 인스턴스에서 크기 조정, 자르기, 색 보정 등을 순차적으로 수행할 수 있습니다.

**Q: Aspose.PSD가 다중 페이지 PSD 파일을 지원하나요?**  
A: 예, 각 레이어에 개별적으로 접근하고 처리할 수 있습니다.

**Q: TIFF 외에 어떤 포맷으로 내보낼 수 있나요?**  
A: Aspose.PSD는 PNG, JPEG, BMP 등 다양한 포맷을 해당 옵션 클래스를 통해 지원합니다.

## 결론

축하합니다! Aspose.PSD for Java를 사용해 PSD 파일의 감마를 조정하고 TIFF 이미지로 내보내는 **java image processing**을 성공적으로 수행했습니다. 이 워크플로는 이미지 밝기와 대비를 세밀하게 제어할 수 있어 자동화된 그래픽 파이프라인, 웹 서비스 또는 데스크톱 유틸리티에 이상적입니다.

---

**마지막 업데이트:** 2025-12-21  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## FAQ

### Q1: Aspose.PSD 문서는 어디에서 찾을 수 있나요?

A1: 문서는 [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)에서 확인할 수 있습니다.

### Q2: Aspose.PSD for Java를 어떻게 다운로드하나요?

A2: 라이브러리는 [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)에서 다운로드합니다.

### Q3: Aspose.PSD를 어디서 구매할 수 있나요?

A3: Aspose.PSD 구매는 [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy)에서 가능합니다.

### Q4: 무료 체험판이 있나요?

A4: 예, 무료 체험판은 [https://releases.aspose.com/](https://releases.aspose.com/)에서 이용할 수 있습니다.

### Q5: Aspose.PSD 지원은 어디에서 받을 수 있나요?

A5: 지원은 Aspose.PSD 포럼([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34))에서 받을 수 있습니다.