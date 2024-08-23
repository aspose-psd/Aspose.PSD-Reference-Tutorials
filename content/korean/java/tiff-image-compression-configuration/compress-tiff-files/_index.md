---
title: Java용 Aspose.PSD를 사용하여 TIFF 파일 압축
linktitle: Java용 Aspose.PSD를 사용하여 TIFF 파일 압축
second_title: Aspose.PSD 자바 API
description: 품질 저하 없이 Java용 Aspose.PSD를 사용하여 TIFF 파일을 효율적으로 압축합니다. 작업 흐름을 간소화하려면 자세한 가이드를 따르세요.
type: docs
weight: 10
url: /ko/java/tiff-image-compression-configuration/compress-tiff-files/
---
## 소개

대규모 그래픽 디자인 프로젝트를 진행 중이고 PSD 파일이 시스템을 무겁게 짓누르고 있다고 상상해 보십시오. 이러한 파일을 공유하거나 나중에 사용하기 위해 저장해야 하지만 크기가 너무 커서 처리할 수 없습니다. 이때 PSD 파일을 TIFF 형식으로 압축하는 것이 유용합니다. TIFF 파일은 품질과 크기 간의 균형을 제공하므로 저장 및 공유에 이상적입니다. 이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 TIFF 파일을 압축하는 과정을 안내하여 이미지를 컴팩트하면서도 품질을 유지하도록 합니다.

## 전제조건

코드를 살펴보기 전에 먼저 살펴보겠습니다. 이 튜토리얼을 진행하려면 다음이 필요합니다.

1.  Java용 Aspose.PSD: Java용 Aspose.PSD 라이브러리가 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/psd/java/).
2. Java 개발 환경: JDK가 설치되어 있는지 확인하세요. IntelliJ IDEA 또는 Eclipse와 같은 IDE도 도움이 될 것입니다.
3. 샘플 PSD 파일: 작업하려면 PSD 파일이 필요합니다. PSD 파일이 없으면 Adobe Photoshop과 같은 그래픽 디자인 소프트웨어를 사용하여 간단한 PSD 파일을 만들 수 있습니다.

모든 설정이 완료되면 TIFF 파일 압축을 시작할 준비가 된 것입니다.

## 패키지 가져오기

실제 코딩을 시작하기 전에 필요한 패키지를 Java 프로젝트로 가져와야 합니다. 이러한 패키지는 PSD 및 TIFF 파일을 조작하는 데 필요한 클래스와 메서드를 제공합니다.

```java
import com.aspose.psd.ColorPaletteHelper;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

이제 필요한 패키지를 가져왔으므로 PSD 파일을 TIFF 형식으로 압축하는 단계별 가이드를 살펴보겠습니다.

## 1단계: PSD 파일 로드

여정의 첫 번째 단계는 압축하려는 PSD 파일을 로드하는 것입니다. Java용 Aspose.PSD는 이 프로세스를 매우 간단하게 만듭니다.
 PSD 파일을 로드하려면 다음을 사용합니다.`Image.load()` 방법. 이 메서드는 지정된 디렉터리에서 PSD 파일을 읽습니다. 어떻게 완료되었는지 살펴보겠습니다.

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

 여기서는 다음과 같은 PSD 파일을 로드합니다.`layers.psd` 다음에 지정된 디렉토리에서`dataDir` . 그만큼`Image.load()` 메소드는 일반을 반환합니다.`Image` 그런 다음 객체를`PsdImage` 물체. 이 캐스팅을 통해 PSD 파일의 특정 기능에 액세스할 수 있습니다.

이것이 왜 중요합니까? PSD 파일을 로드하는 것은 앞으로 수행할 모든 작업의 기초입니다. 메인 이벤트 전에 무대를 준비하는 것과 같습니다.

## 2단계: TIFF 옵션 생성

PSD 파일이 로드되면 다음 단계는 최종 TIFF 이미지의 모양을 결정하는 TIFF 옵션을 만드는 것입니다. 이 단계에는 압축, 샘플당 비트 및 기타 중요한 설정을 설정하는 작업이 포함됩니다.

 이미지를 압축하려면 다음 인스턴스를 생성해야 합니다.`TiffOptions`수업. 이 클래스를 사용하면 TIFF 파일에 대한 다양한 설정을 구성할 수 있습니다.

```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
```

 여기서는 초기화했습니다.`TiffOptions` 기본 형식으로. 그러나 이것은 시작에 불과합니다. 조정해야 할 설정을 분석해 보겠습니다.

## 3단계: TIFF 압축 구성

이제 TIFF 옵션이 설정되었으므로 압축에 집중할 차례입니다. 압축은 파일 크기를 줄여 TIFF 파일을 보다 쉽게 관리할 수 있도록 해줍니다.

이 예에서는 무손실 압축 방법인 LZW 압축을 사용합니다. 이는 파일 크기가 줄어드는 동안 이미지 품질은 그대로 유지된다는 것을 의미합니다.

```java
outputSettings.setCompression(TiffCompressions.Lzw);
```

 압축을 다음으로 설정하면`Lzw`, 이미지 품질을 저하시키지 않고 파일 크기를 줄이는 것을 보장합니다. 이는 작은 파일 크기와 고품질이라는 두 가지 장점을 모두 활용하는 것과 같습니다.

LZW를 선택하는 이유는 무엇입니까? LZW 압축은 그래픽 및 디자인 파일에서 흔히 나타나는 반복적인 패턴이 있는 이미지에 특히 효과적입니다.

## 4단계: 샘플당 비트 수 및 측광 모드 조정

압축은 필수적이지만 최종 TIFF 파일의 품질과 크기에 영향을 미치는 다른 요소도 있습니다. 가장 중요한 두 가지는 샘플당 비트 수와 측광 모드입니다.

### 샘플당 비트 설정

샘플당 비트는 이미지의 색상 심도를 결정합니다. 이 튜토리얼에서는 이미지 품질과 파일 크기의 균형을 맞추는 4비트 회색조 팔레트를 사용합니다.

```java
int[] ushort = {4};  
outputSettings.setBitsPerSample(ushort);
```

여기서는 샘플당 비트 수를 4로 설정했습니다. 이는 이미지의 각 픽셀이 4비트로 표시되어 16개의 서로 다른 회색 음영을 허용한다는 의미입니다. 이 설정은 전체 색상 범위가 필요하지 않은 이미지에 이상적입니다.

### 측광 모드 설정

측광 모드는 픽셀 데이터가 해석되는 방식을 결정합니다. 우리의 경우에는 색상이 없는 이미지를 압축하는 데 적합한 회색조 팔레트를 사용하겠습니다.

```java
outputSettings.setPhotometric(TiffPhotometrics.Palette);
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(true));
```

 측광 모드를 다음으로 설정하여`Palette`4비트 회색조 팔레트를 사용하여 이미지를 제한된 수의 음영을 가진 회색조 이미지로 처리하도록 프로그램에 지시합니다. 이렇게 하면 시각적 무결성을 유지하면서 파일 크기가 더욱 줄어듭니다.

## 5단계: 압축된 TIFF 파일 저장

모든 설정이 완료되면 마지막 단계는 PSD 파일을 압축된 TIFF 파일로 저장하는 것입니다. 이 단계는 지금까지 수행한 모든 작업의 정점입니다.

압축된 TIFF 파일을 저장하는 방법은 다음과 같습니다.

```java
psdImage.save(dataDir + "SampleTiff_out.tiff", outputSettings);
```

 이 코드 줄은 PSD 파일을 다음에서 지정한 디렉토리에 TIFF 파일로 저장합니다.`dataDir` . 그만큼`outputSettings` 이전에 구성한 파일이 사양에 따라 압축되었는지 확인하세요.

그리고 거기에 있습니다! 이제 PSD 파일은 쉽게 공유할 수 있는 컴팩트한 TIFF 파일입니다.

## 결론

Java용 Aspose.PSD를 사용하여 TIFF 파일을 압축하는 것은 이미지 품질을 유지하면서 많은 저장 공간을 절약할 수 있는 간단한 프로세스입니다. 이 튜토리얼에 설명된 단계를 따르면 PSD 파일의 크기를 효율적으로 줄이고 관리하기 쉬운 TIFF 형식으로 변환할 수 있습니다. 이미지를 저장, 공유 또는 보관하려는 경우 이 방법을 사용하면 품질이나 성능을 타협할 필요가 없습니다.

## FAQ

### 다른 형식에 비해 TIFF를 사용하면 어떤 이점이 있나요?

TIFF 파일은 무손실 압축을 제공하므로 파일 크기를 줄이면서 이미지 품질을 유지합니다. 또한 다양한 플랫폼과 소프트웨어에서 널리 지원됩니다.

### 이 방법을 사용하여 컬러 이미지를 압축할 수 있습니까?

 예, 가능합니다. 그러나 이 튜토리얼에서는 회색조 이미지에 중점을 둡니다. 컬러 이미지를 처리하도록 설정을 수정할 수 있습니다.`BitsPerSample` 그리고`Photometric` 모드.

### LZW 압축이 모든 이미지에 가장 적합한 옵션입니까?

LZW 압축은 로고나 단순한 그래픽과 같이 반복적인 패턴이 있는 이미지에 탁월합니다. 그러나 사진의 경우 JPEG와 같은 다른 압축 방법이 더 적합할 수 있습니다.

### Java용 Aspose.PSD를 사용하여 다른 파일 형식을 압축할 수 있나요?

Java용 Aspose.PSD는 주로 PSD 파일을 처리하지만 이러한 파일을 TIFF, JPEG, PNG 등을 포함한 다양한 형식으로 변환하기 위한 광범위한 지원을 제공합니다.

### 그레이스케일 압축은 이미지 품질에 어떤 영향을 줍니까?

회색조 압축은 이미지의 색상 수를 줄여 시각적 세부 묘사를 감소시킬 수 있습니다. 그러나 특정 유형의 이미지에서는 이러한 절충이 최소화되어 파일 크기가 크게 줄어들 수 있습니다.