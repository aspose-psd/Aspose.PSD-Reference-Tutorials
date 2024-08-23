---
title: PSD에서 채널 믹서 조정 레이어 내보내기 - Java
linktitle: PSD에서 채널 믹서 조정 레이어 내보내기 - Java
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD에서 채널 믹서 조정 레이어를 내보내는 방법을 알아보세요. RGB 및 CMYK 레이어 수정, 변경 사항 저장, PNG로 내보내기에 대한 단계별 가이드입니다.
type: docs
weight: 14
url: /ko/java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
---
## 소개

이미지 편집, 특히 Adobe Photoshop 파일(PSD)의 경우 레이어를 효율적으로 관리하는 것이 중요합니다. 이러한 레이어 중에서 채널 믹서 조정 레이어는 이미지의 색상 균형을 조정하는 데 중요한 역할을 합니다. 이러한 레이어를 프로그래밍 방식으로 조작하려는 Java 개발자라면 운이 좋을 것입니다! 이 문서에서는 Java용 Aspose.PSD를 사용하여 채널 믹서 조정 레이어를 내보내는 과정을 안내합니다. 이 가이드가 끝나면 RGB 및 CMYK 채널 믹서 조정 레이어를 처리하고, 변경 사항을 저장하고, 최종 이미지를 PSD 및 PNG 형식으로 내보낼 수 있게 됩니다.

## 전제조건

코드를 살펴보기 전에 필요한 모든 것이 갖추어져 있는지 확인하겠습니다.

1. Java 라이브러리용 Aspose.PSD: Java 라이브러리용 Aspose.PSD가 설치되어 있어야 합니다. 다음에서 다운로드할 수 있습니다.[다운로드 페이지](https://releases.aspose.com/psd/java/).
2. JDK(Java Development Kit): JDK 8 이상이 시스템에 설치되어 있는지 확인하십시오.
3. 통합 개발 환경(IDE): IntelliJ IDEA 또는 Eclipse와 같은 IDE를 사용하여 Java 코드를 작성하고 실행합니다.
4. PSD 파일: 특히 수정하려는 채널 믹서 조정 레이어가 포함된 PSD 파일을 준비하세요.

## 패키지 가져오기

먼저 필요한 패키지를 가져오겠습니다. 이 단계는 Java용 Aspose.PSD를 사용하기 위한 환경을 설정하는 데 필수적입니다.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1단계: RGB 채널 믹서 레이어를 사용하여 PSD 파일 로드

RGB 채널 믹서 조정 레이어가 포함된 PSD 파일을 로드하여 튜토리얼을 시작하겠습니다.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";

PsdImage im = (PsdImage) Image.load(sourceFileName);
```

이 단계에서는 PSD 파일이 저장되는 디렉터리를 정의합니다(`dataDir` ). 그런 다음 다음을 사용하여 PSD 파일을 로드합니다.`Image.load()` 메서드를 사용하여 캐스팅합니다.`PsdImage` 이를 통해 레이어를 조작할 수 있습니다.

## 2단계: RGB 채널 믹서 레이어 수정

파일이 로드되면 RGB 채널 믹서 레이어에 액세스하고 수정할 수 있습니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof RgbChannelMixerLayer) {
        RgbChannelMixerLayer rgbLayer = (RgbChannelMixerLayer) im.getLayers()[i];
        rgbLayer.getRedChannel().setBlue((short) 100);
        rgbLayer.getBlueChannel().setGreen((short) -100);
        rgbLayer.getGreenChannel().setConstant((short) 50);
    }
}
```

이 단계에서 일어나는 일은 다음과 같습니다.
- PSD 파일의 모든 레이어를 반복합니다.
-  레이어가 다음의 인스턴스인지 확인합니다.`RgbChannelMixerLayer`.
- 그렇다면 색상 채널 조정을 진행합니다. 예를 들어 빨간색 채널의 파란색 구성요소를 100으로 설정하고 파란색 채널의 녹색 구성요소를 100만큼 줄인 다음 녹색 채널에 상수 값을 설정합니다.

## 3단계: 수정된 PSD 파일 저장

RGB 채널 믹서 레이어를 수정한 후 변경 사항을 저장해야 합니다.

```java
String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
im.save(psdPathAfterChange);
```

 이 단계에서는 수정된 PSD 파일이 저장될 경로를 지정하고 다음을 사용합니다.`save()` 변경 사항을 저장하는 방법.

## 4단계: 이미지를 PNG로 내보내기

이제 PSD 파일이 저장되었으므로 이미지를 알파 투명도가 포함된 PNG 형식으로 내보내겠습니다.

```java
String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

이 단계에서는 다음을 수행합니다.
- PNG 파일의 내보내기 경로를 정의합니다.
-  우리는`PngOptions` 개체를 선택하고 색상 유형을 다음으로 설정합니다.`TruecolorWithAlpha`이미지의 투명성을 유지합니다.
- 마지막으로 이미지를 PNG 파일로 저장합니다.

## 5단계: CMYK 채널 믹서 레이어를 사용하여 PSD 파일 로드

다음으로 CMYK 채널 믹서 조정 레이어를 처리하는 방법을 살펴보겠습니다.

```java
sourceFileName = dataDir + "ChannelMixerAdjustmentLayerCmyk.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

이전 단계와 마찬가지로 CMYK 채널 믹서 레이어가 포함된 PSD 파일을 로드합니다.

## 6단계: CMYK 채널 믹서 레이어 수정

파일이 로드되면 CMYK 채널 믹서 레이어를 수정해 보겠습니다.

```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof CmykChannelMixerLayer) {
        CmykChannelMixerLayer cmykLayer = (CmykChannelMixerLayer) img.getLayers()[i];
        cmykLayer.getCyanChannel().setBlack((short) 20);
        cmykLayer.getMagentaChannel().setYellow((short) 50);
        cmykLayer.getYellowChannel().setCyan((short) -25);
        cmykLayer.getBlackChannel().setYellow((short) 25);
    }
}
```

이 단계에서 우리는 다음을 수행합니다.
- 레이어를 반복하여 CMYK 채널 믹서 레이어를 식별합니다.
- 청록색 채널의 검정색 구성 요소를 20으로 설정하고 이에 따라 다른 채널을 조정하는 등 CMYK 스펙트럼 내에서 다양한 색상 채널을 수정합니다.

## 7단계: 수정된 PSD 파일 저장

수정이 완료되면 업데이트된 PSD 파일을 저장합니다.

```java
psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
img.save(psdPathAfterChange);
```

 수정된 CMYK PSD 파일을 다음을 사용하여 지정된 경로에 저장합니다.`save()` 방법.

## 8단계: CMYK 이미지를 PNG로 내보내기

마지막으로 수정된 CMYK 이미지를 PNG 파일로 내보내 보겠습니다.

```java
pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
img.save(pngExportPath, options);
```

RGB 이미지와 마찬가지로 내보내기 경로를 정의하고 CMYK 이미지를 알파 투명도가 포함된 PNG 형식으로 저장합니다.

## 결론

이 가이드에서는 Java용 Aspose.PSD를 사용하여 PSD 파일의 채널 믹서 조정 레이어를 내보내는 전체 프로세스를 살펴보았습니다. 우리는 PSD 파일 로드, RGB 및 CMYK 채널 믹서 레이어 수정, PSD 및 PNG 형식으로 이미지 저장 및 내보내기에 이르기까지 모든 것을 다루었습니다. 이러한 단계를 수행하면 이제 Java 프로젝트에서 채널 믹서 레이어를 효율적으로 관리하고 조작할 수 있습니다.

## FAQ

### 다른 이미지 형식과 함께 Java용 Aspose.PSD를 사용할 수 있나요?  
예, Java용 Aspose.PSD는 PNG, JPEG, BMP, TIFF 등 다양한 형식을 지원합니다.

### 곡선이나 레벨과 같은 다른 조정 레이어를 어떻게 처리합니까?  
채널 믹서 레이어와 유사하게 Aspose.PSD for Java에서 제공하는 적절한 클래스를 사용하여 다른 조정 레이어를 조작할 수 있습니다.

### 여러 PSD 파일을 일괄 처리하는 방법이 있습니까?  
예, PSD 파일 디렉터리를 반복하면서 Aspose.PSD for Java를 사용하여 각 파일에 동일한 조정 사항을 적용할 수 있습니다.

### PNG로 내보낼 때 이미지 품질을 유지하는 가장 좋은 방법은 무엇입니까?  
 사용`PngOptions` ~와 함께`TruecolorWithAlpha` 투명성을 유지하면서 고품질 수출을 보장합니다.

### Java용 Aspose.PSD를 사용하려면 라이센스가 필요합니까?  
 예, Aspose.PSD for Java는 라이선스 제품입니다. 당신은 얻을 수 있습니다[임시면허](https://purchase.aspose.com/temporary-license/) 정식 라이센스를 테스트하거나 구매하려면