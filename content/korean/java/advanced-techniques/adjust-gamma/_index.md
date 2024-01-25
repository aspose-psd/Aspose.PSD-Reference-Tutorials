---
title: Java용 Aspose.PSD를 사용하여 이미지 감마 조정
linktitle: 이미지의 감마 조정
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 이미지 감마를 손쉽게 조정하는 방법을 알아보세요. 최적의 결과를 얻으려면 단계별 가이드를 따르십시오.
type: docs
weight: 23
url: /ko/java/advanced-techniques/adjust-gamma/
---
## 소개

이미지 처리 영역에서 이미지의 감마를 조정하는 것은 시각적 매력을 향상시키는 중요한 단계입니다. Aspose.PSD for Java는 Java 개발자가 이미지 감마를 쉽게 조작할 수 있는 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 Aspose.PSD를 사용하여 감마를 조정하는 방법을 살펴보고 원활한 구현을 보장하기 위해 각 단계를 세분화합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 설정되어 있는지 확인하세요.

1. Java 개발 환경: 시스템에 Java 개발 환경이 설치되어 있는지 확인하십시오.
2.  Aspose.PSD 라이브러리: Aspose.PSD 라이브러리를 다운로드하여 Java 프로젝트에 통합하세요. 다음에서 필요한 리소스를 찾을 수 있습니다.[선적 서류 비치](https://reference.aspose.com/psd/java/).
3. 샘플 이미지: 감마 조정을 적용하는 데 사용할 샘플 PSD 이미지를 준비합니다.

## 패키지 가져오기

프로세스를 시작하려면 Java 프로젝트에 필요한 패키지를 가져옵니다. 이는 Aspose.PSD 기능을 원활하게 활용하기 위한 단계를 설정합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1단계: 이미지 로드

 샘플 PSD 이미지를 인스턴스에 로드하는 것부터 시작하세요.`RasterImage` 수업. 이는 후속 감마 조정의 기초입니다.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// RasterImage 클래스의 인스턴스에 기존 이미지 로드
Image image = Image.load(sourceFile);

// 이미지의 객체를 RasterImage로 캐스트
RasterImage rasterImage = (RasterImage)image;

// 성능 향상을 위해 RasterImage가 캐시되었는지 확인하세요.
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## 2단계: 감마 조정

 이제 로드된 이미지의 감마를 조정합니다.`adjustGamma` 방법. 요구 사항에 따라 감마 값을 미세 조정합니다.

```java
// 감마 조정
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 3단계: TiffOptions 생성

 인스턴스 만들기`TiffOptions` 결과 이미지를 위해. 샘플당 비트 수, 측광 옵션 등 다양한 속성을 설정하여 출력을 사양에 맞게 조정하세요.

```java
// 결과 이미지에 대한 TiffOptions 인스턴스를 생성합니다.
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 4단계: 결과 이미지 저장

 이전에 정의한 형식을 사용하여 조작된 이미지를 TIFF 형식으로 저장합니다.`TiffOptions`.

```java
// 결과 이미지를 TIFF 형식으로 저장
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 이미지의 감마를 성공적으로 조정했습니다. 이 프로세스를 통해 개발자는 손쉽게 이미지 품질을 향상하여 시각적으로 매력적인 사용자 경험을 제공할 수 있습니다.

## FAQ

### Q1: Aspose.PSD 설명서는 어디서 찾을 수 있나요?

 A1: 다음에서 문서에 액세스할 수 있습니다.[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Java용 Aspose.PSD를 어떻게 다운로드합니까?

 A2: 다음에서 라이브러리를 다운로드하세요.[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Aspose.PSD는 어디서 구입할 수 있나요?

 A3: 방문[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) Aspose.PSD를 구입하세요.

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, 다음에서 무료 평가판을 탐색할 수 있습니다.[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Aspose.PSD에 대한 지원은 어디서 구할 수 있나요?

 A5: 지원을 받으려면 Aspose.PSD 포럼을 방문하세요.[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).