---
title: Java용 Aspose.PSD를 사용하여 이미지 밝기 조정
linktitle: 이미지의 밝기 조정
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java에서 이미지 밝기를 향상시킵니다. 프로그래밍 방식으로 이미지 밝기를 조정하는 단계별 가이드입니다.
weight: 21
url: /ko/java/advanced-techniques/adjust-brightness/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.PSD를 사용하여 이미지 밝기 조정

## 소개

이미지 향상은 그래픽 디자인과 디지털 사진의 일반적인 요구 사항입니다. Aspose.PSD for Java는 프로그래밍 방식으로 이미지 밝기를 조정하는 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 Java 라이브러리용 Aspose.PSD를 활용하여 이미지의 밝기를 단계별로 조정하는 방법을 살펴보겠습니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제조건이 충족되었는지 확인하십시오.

-  Java 라이브러리용 Aspose.PSD: 다음에서 라이브러리를 다운로드하고 설치합니다.[Java 문서용 Aspose.PSD](https://reference.aspose.com/psd/java/).

## 패키지 가져오기

시작하려면 필요한 패키지를 Java 프로젝트로 가져옵니다. 이 예에서는 다음을 사용합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

이제 이미지의 밝기를 조정하는 과정을 간단한 단계로 나누어 보겠습니다.

## 1단계: 이미지 로드

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// RasterImage 클래스의 인스턴스에 기존 이미지 로드
Image image = Image.load(sourceFile);
// 이미지의 객체를 RasterImage로 캐스트
RasterImage rasterImage = (RasterImage) image;

// RasterImage가 캐시되었는지 확인하고 더 나은 성능을 위해 RasterImage를 캐시하세요.
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 이 단계에서는 대상 이미지를 로드하고 이를`RasterImage` 추가 처리를 위해.

## 2단계: 밝기 조정

```java
// 밝기를 조정하세요
rasterImage.adjustBrightness(-50);
```

 여기서는`adjustBrightness`이미지의 밝기를 수정하는 방법. 이 예에서는 밝기를 50단위만큼 줄였지만 요구 사항에 따라 이 값을 사용자 정의할 수 있습니다.

## 3단계: TiffOptions 설정

```java
int[] ushort = {8, 8, 8};
// 결과 이미지에 대한 TiffOptions 인스턴스를 생성합니다.
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 구성`TiffOptions` 조정된 이미지를 저장합니다. 조정하다`bitsPerSample` 그리고`photometric` 귀하의 특정 요구에 따라 속성을 제공합니다.

## 4단계: 결과 이미지 저장

```java
// 결과 이미지 저장
rasterImage.save(destName, tiffOptions);
```

 마지막으로 지정된 이미지를 사용하여 수정된 이미지를 저장합니다.`TiffOptions`.

## 결론

Aspose.PSD for Java를 사용하면 프로그래밍 방식으로 이미지의 밝기를 쉽게 조정할 수 있습니다. 이 튜토리얼은 Java 애플리케이션에서 이 기능을 구현하는 방법에 대한 포괄적인 가이드를 제공합니다.

## FAQ

### Q1: PSD 외에 다른 이미지 형식에서도 밝기를 조정할 수 있나요?

A1: 예, Java용 Aspose.PSD는 JPEG, PNG, TIFF와 같은 다양한 이미지 형식을 지원합니다.

### Q2: 이미지 조정 프로세스 중 오류를 처리하려면 어떻게 해야 합니까?

대답 2: try-catch 블록을 사용하여 오류 처리를 구현하여 발생할 수 있는 예외를 관리할 수 있습니다.

### Q3: 밝기 조정 범위에 제한이 있나요?

A3: 조정 범위는 이미지 내용과 형식에 따라 다르지만 Aspose.PSD는 사용자 정의에 유연성을 제공합니다.

### Q4: 상용 프로젝트에서 Java용 Aspose.PSD를 사용할 수 있나요?

 A4: 예, Java용 Aspose.PSD는 상업용 라이브러리이며 다음에서 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/buy).

### Q5: Aspose.PSD for Java에 대한 무료 평가판이 있습니까?

 A5: 예, 무료 평가판을 통해 라이브러리를 탐색할 수 있습니다.[여기](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
