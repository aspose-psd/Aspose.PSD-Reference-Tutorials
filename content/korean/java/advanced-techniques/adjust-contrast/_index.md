---
title: Java용 Aspose.PSD를 사용하여 이미지 대비 조정
linktitle: 이미지의 대비 조정
second_title: Aspose.PSD 자바 API
description: Aspose.PSD를 사용하여 Java의 이미지 대비 조정 세계를 탐험해보세요. 원활한 이미지 조작을 위한 단계별 가이드를 따르세요.
type: docs
weight: 22
url: /ko/java/advanced-techniques/adjust-contrast/
---
## 소개

Java를 사용한 이미지 처리 영역에서 Aspose.PSD는 강력한 도구로 돋보입니다. 수많은 기능 중에서 이미지 대비 조정은 일반적인 요구 사항입니다. 이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 이미지 대비를 조정하는 과정을 안내합니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 가이드는 이미지 조작의 필수 측면을 익히는 데 도움이 될 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 프로그래밍에 대한 기본 이해.
-  Java 라이브러리용 Aspose.PSD가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/psd/java/).

## 패키지 가져오기

시작하려면 필요한 패키지를 Java 프로젝트로 가져와야 합니다. 코드에 다음 줄을 추가합니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1단계: 이미지 로드

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// RasterImage 클래스의 인스턴스에 기존 이미지 로드
Image image = Image.load(sourceFile);
```

 이 단계에서는 다음을 사용하여 샘플 이미지("sample.psd")를 로드합니다.`Image.load` 방법.

## 2단계: RasterImage 및 캐시 데이터로 캐스팅

```java
// 이미지의 객체를 RasterImage로 캐스트
RasterImage rasterImage = (RasterImage)image;

// RasterImage가 캐시되었는지 확인하고 더 나은 성능을 위해 RasterImage를 캐시하세요.
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 여기서는 일반을 캐스팅합니다.`Image` a에 이의를 제기하다`RasterImage` 특정 처리를 위해. 이미지 데이터를 캐싱하면 성능이 향상됩니다.

## 3단계: 대비 조정

```java
// 대비를 조정하세요
rasterImage.adjustContrast(50);
```

 그만큼`adjustContrast`방법은 이미지의 대비를 수정하는 데 사용됩니다. 이 예에서는 대비가 50% 증가했습니다.

## 4단계: TiffOptions 생성 및 저장

```java
// 결과 이미지에 대한 TiffOptions 인스턴스를 생성합니다.
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// 결과 이미지를 TIFF 형식으로 저장
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 여기서 우리는 설정했습니다.`TiffOptions` 출력 이미지의 경우 형식 및 기타 속성을 지정합니다. 그런 다음 최종 이미지는 TIFF 파일에 저장됩니다.

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 이미지의 대비를 성공적으로 조정했습니다. 이 튜토리얼에서는 패키지 가져오기부터 처리된 이미지 저장까지 필수 단계를 다루었습니다.

## FAQ

### Q1: Aspose.PSD는 다른 이미지 형식과 호환됩니까?

A1: 예, Aspose.PSD는 다양한 이미지 형식을 지원하여 프로젝트에 유연성을 제공합니다.

### Q2: Aspose.PSD의 임시 라이선스를 어떻게 얻을 수 있나요?

 A2: 임시 라이센스를 얻을 수 있습니다[여기](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.PSD 문서는 어디서 찾을 수 있나요?

A3: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/psd/java/).

### Q4: Aspose.PSD에 어떤 지원 옵션을 사용할 수 있나요?

 A4: 지원을 받으려면[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34).

### Q5: Aspose.PSD를 구입할 수 있나요?

 A5: 예, Aspose.PSD를 구입할 수 있습니다.[여기](https://purchase.aspose.com/buy).