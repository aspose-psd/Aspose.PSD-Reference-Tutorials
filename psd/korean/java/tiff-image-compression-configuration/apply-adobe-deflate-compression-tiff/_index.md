---
title: TIFF에 Adobe Deflate 압축 적용 - Java
linktitle: TIFF에 Adobe Deflate 압축 적용 - Java
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 TIFF 이미지에 Adobe Deflate 압축을 적용하는 방법을 알아보세요. 효율적인 이미지 처리를 위한 단계별 가이드입니다.
type: docs
weight: 12
url: /ko/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---
## 소개

품질 저하 없이 TIFF 이미지를 효율적으로 압축하는 방법이 궁금하신가요? 대용량 이미지 파일을 처리하는 경우 느린 로딩 시간과 저장 문제로 인한 어려움을 알고 계실 것입니다. Adobe Deflate 압축이 작동하는 곳이 바로 여기이며, Java용 Aspose.PSD를 사용하면 프로젝트에서 이를 쉽게 구현할 수 있습니다. 이 튜토리얼에서는 TIFF 이미지에 Adobe Deflate 압축을 적용하는 과정을 단계별로 안내합니다. 다이빙할 준비가 되셨나요? 시작해 봅시다!

## 전제조건

실제 코드로 넘어가기 전에 모든 것이 설정되었는지 확인하겠습니다. 필요한 것은 다음과 같습니다.

1. JDK(Java Development Kit): 컴퓨터에 최신 버전의 JDK가 설치되어 있는지 확인하세요.
2.  Java용 Aspose.PSD: Java용 Aspose.PSD 라이브러리를 다운로드하여 프로젝트에 통합하세요. 당신은 그것을 얻을 수 있습니다[여기](https://releases.aspose.com/psd/java/).
3. 개발 환경: IntelliJ IDEA, Eclipse 또는 NetBeans와 같은 IDE.
4.  임시 라이선스(선택 사항): 구매할 준비가 되지 않은 경우 임시 라이선스를 받을 수 있습니다.[임시면허](https://purchase.aspose.com/temporary-license/) 기능을 시험해 보세요.

## 패키지 가져오기

Java 프로젝트에 필요한 패키지를 가져오는 것부터 시작하겠습니다. 이러한 가져오기는 Aspose.PSD 라이브러리 및 Java 유틸리티로 작업할 수 있게 해주기 때문에 매우 중요합니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

이제 기본 사항을 다루었으므로 프로세스를 따라하기 쉬운 단계로 나누어 보겠습니다.

## 1단계: TIFF 옵션 설정

 먼저, 인스턴스를 생성해야 합니다.`TiffOptions` 필요에 따라 구성하세요. 이러한 옵션은 해상도, 색 구성표 및 압축을 포함하여 TIFF 파일이 처리되는 방법을 정의합니다.

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

여기서는`TiffOptions` 기본 형식의 개체입니다. 하지만 그건 시작에 불과해요! 

## 2단계: 이미지 속성 구성

 다음으로 TIFF 이미지의 다양한 속성을 설정해야 합니다.`BitsPerSample`, `Photometric`, `Resolution` , 그리고`PlanarConfiguration`. 이러한 설정은 이미지 데이터가 저장되고 표시되는 방식을 결정합니다.

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

각 속성이 수행하는 작업은 다음과 같습니다.
- BitsPerSample: 각 색상 채널의 샘플당 비트 수를 설정합니다.
- 광도계: 색상 모델(이 경우 RGB)을 정의합니다.
- 해상도: 이미지의 수평 및 수직 해상도를 지정합니다.
- PlanarConfiguration: 픽셀 데이터가 저장되는 방법을 결정합니다.

## 3단계: Adobe Deflate 압축 적용

이제 마법이 온다! TIFF 이미지에 Adobe Deflate 압축을 적용하면 이미지 품질 저하 없이 파일 크기를 줄이는 데 도움이 됩니다.

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

Adobe Deflate는 파일 크기를 줄이면서 높은 품질을 유지해야 하는 이미지에 적합한 무손실 압축 방법입니다.

## 4단계: TIFF 이미지 생성 및 편집

옵션이 설정되면 새로운 TIFF 이미지를 생성하고 조작할 차례입니다. 이 단계에서는 간단한 100x100 이미지를 만들고 빨간색 픽셀로 채웁니다.

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

여기서는 이미지의 각 픽셀을 반복하고 색상을 빨간색으로 설정합니다. 물론 이 부분을 사용자 정의하여 더 복잡한 이미지를 만들 수도 있습니다.

## 5단계: 압축된 TIFF 이미지 저장

마지막으로 이미지를 구성하고 생성한 후 마지막 단계는 압축이 적용된 이미지를 저장하는 것입니다. 올바른 디렉토리 경로를 지정했는지 확인하십시오.

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

그게 다야! Java용 Aspose.PSD를 사용하여 TIFF 이미지에 Adobe Deflate 압축을 성공적으로 적용했습니다.

## 결론

그리고 거기에 있습니다! TIFF 이미지에 Adobe Deflate 압축을 적용하는 것은 Aspose.PSD for Java를 사용하는 간단한 프로세스입니다. 웹 사이트, 디지털 미디어 또는 기타 프로젝트의 대용량 이미지를 처리하는 경우 이 방법을 사용하면 파일 크기를 보다 쉽게 관리할 수 있으면서도 고품질을 유지할 수 있습니다. Aspose.PSD for Java의 장점은 단순성과 효율성에 있기 때문에 복잡한 이미지 형식으로 작업하는 개발자에게 적합한 도구입니다.

## FAQ

### Adobe Deflate 압축이란 무엇입니까?
Adobe Deflate는 품질 저하 없이 TIFF 이미지의 크기를 줄이는 데 사용되는 무손실 압축 방법입니다.

### Java용 Aspose.PSD에서 다른 압축 방법을 사용할 수 있나요?
예, Aspose.PSD는 LZW, CCITT 및 JPEG와 같은 다양한 압축 방법을 지원합니다.

### Aspose.PSD 라이브러리는 무료인가요?
 Aspose.PSD는 무료 평가판을 제공하지만 전체 기능을 사용하려면 라이센스가 필요합니다. 당신은 얻을 수 있습니다[임시면허](https://purchase.aspose.com/temporary-license/) 그것을 시험해보려고.

### 해상도 설정은 TIFF 이미지에 어떤 영향을 줍니까?
해상도는 인쇄하거나 표시할 때 이미지의 선명도를 결정합니다. 해상도가 높을수록 품질은 향상되지만 파일 크기가 커집니다.

### Java용 Aspose.PSD를 사용하여 다른 이미지 형식을 조작할 수 있나요?
전적으로! Aspose.PSD는 PSD, PNG, JPEG 등과 같은 다양한 형식을 지원합니다.