---
title: PSD에서 색상 채우기로 획 효과 적용 - Java
linktitle: PSD에서 색상 채우기로 획 효과 적용 - Java
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 PSD 파일에 색상 채우기로 획 효과를 적용하는 방법을 알아보세요. 이미지를 쉽게 향상하려면 이 단계별 가이드를 따르세요.
type: docs
weight: 21
url: /ko/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---
## 소개

이 가이드에서는 Java용 Aspose.PSD를 사용하여 PSD 파일에 색상 채우기로 획 효과를 적용하는 과정을 안내합니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 단계별 튜토리얼을 통해 작업을 쉽게 완료할 수 있습니다. 환경 설정부터 효과가 적용된 최종 이미지 저장까지 모든 과정을 다룹니다.

## 전제조건

시작하기 전에 이 튜토리얼을 따라야 할 모든 것이 있는지 확인하십시오.

1. JDK(Java Development Kit) 설치: 시스템에 JDK 8 이상이 설치되어 있는지 확인하십시오.
2.  Java 라이브러리용 Aspose.PSD: Java 라이브러리용 Aspose.PSD가 필요합니다. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/psd/java/).
3. 통합 개발 환경(IDE): IntelliJ IDEA, Eclipse 또는 기타 원하는 IDE.
4. 샘플 PSD 파일: 획 효과를 적용할 수 있는 샘플 PSD 파일입니다. PSD가 없으면 Photoshop에서 간단한 PSD 파일을 만들거나 인터넷에서 다운로드할 수 있습니다.
5. Java 기본 지식: 이 튜토리얼은 초보자에게 적합하지만 Java에 대한 기본 지식이 있으면 도움이 됩니다.

이러한 필수 구성 요소가 준비되면 PSD 파일에 색상 채우기를 사용하여 획 효과를 적용할 수 있는 모든 설정이 완료된 것입니다.

## 패키지 가져오기

Java용 Aspose.PSD 작업을 시작하려면 필요한 패키지를 Java 프로젝트로 가져와야 합니다. 방법은 다음과 같습니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

이러한 가져오기는 PSD 파일 작업, 효과 적용, 이미지를 원하는 형식으로 저장하는 데 필요한 모든 클래스를 가져옵니다.

## 1단계: PSD 파일 로드

 프로세스의 첫 번째 단계는 수정하려는 PSD 파일을 로드하는 것입니다. Java용 Aspose.PSD는 이를 매우 간단하게 만듭니다.`PsdImage` 수업. 방법은 다음과 같습니다.

### 1.1 디렉토리 경로 설정

먼저 PSD 파일이 저장되는 디렉터리 경로를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` PSD 파일이 있는 실제 경로를 사용합니다.

### 1.2 PSD 이미지 로드

 이제 다음을 사용하여 PSD 파일을 로드합니다.`PsdLoadOptions` 그리고`PsdImage` 수업:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 여기서는`PsdLoadOptions`PSD 내의 기존 효과에 액세스할 수 있도록 효과 리소스를 로드하도록 구성됩니다.

## 2단계: 색상 채우기로 획 효과 적용

PSD 파일이 로드된 상태에서 다음 단계는 이미지 레이어에 획 효과를 적용하는 것입니다. 이것이 진짜 마법이 일어나는 곳입니다.

각 PSD 파일에는 여러 레이어가 포함될 수 있으며 각 레이어에 효과를 적용해야 합니다. 수행 방법은 다음과 같습니다.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

이 루프에서:

- `im.getLayers()`: PSD 파일의 모든 레이어를 검색합니다.
- `StrokeEffect effect`: 레이어에 적용된 획 효과를 추출합니다.
- `ColorFillSettings settings`: 획 효과에 대한 채우기 설정을 수정합니다.
- `settings.setColor(Color.getDeepPink())`: 획 색상을 진한 분홍색으로 설정합니다. 원하는 색상으로 변경할 수 있습니다.

## 3단계: 수정된 PSD를 저장하고 PNG로 내보내기

획 효과를 적용한 후에는 변경 사항을 저장하고 이미지를 내보낼 차례입니다.

### 3.1 PSD 파일 저장

수정된 PSD 파일을 저장하려면 다음 코드를 사용하십시오.

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

그러면 지정된 경로에 획 효과가 적용된 파일이 저장됩니다.

### 3.2 PNG로 내보내기

이미지에 더 쉽게 접근할 수 있도록 하려면 해당 이미지를 PNG 파일로 내보내는 것이 좋습니다. 방법은 다음과 같습니다.

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

이 코드 조각은 이미지를 트루 컬러와 알파 투명도를 갖춘 PNG로 저장하여 웹 애플리케이션이나 다른 플랫폼에서 사용할 수 있도록 해줍니다.

## 결론

Java용 Aspose.PSD를 사용하여 PSD 파일에 색상 채우기로 획 효과를 적용하는 것은 간단할 뿐만 아니라 매우 강력합니다. 단 몇 줄의 코드만으로 복잡한 이미지 처리 작업을 자동화하여 시간과 노력을 절약할 수 있습니다.

대량의 이미지 작업을 하거나 파일 몇 개만 조정해야 하는 경우에도 이 방법은 유연하고 효율적인 솔루션을 제공합니다. 이제 기본 사항을 익혔으므로 다양한 효과와 사용자 정의를 실험하여 이미지를 정말 돋보이게 만들 수 있습니다.

시험해 볼 준비가 되셨나요? 지금 바로 샘플 PSD 파일을 다운로드하고 놀라운 효과를 추가해 보세요!

## FAQ

### Aspose.PSD for Java를 사용하여 단일 레이어에 여러 효과를 적용할 수 있나요?
예, 레이어의 혼합 옵션에 액세스하고 원하는 효과를 추가하여 단일 레이어에 여러 효과를 적용할 수 있습니다.

### PSD 파일 배치에 대한 프로세스를 자동화할 수 있습니까?
전적으로! PSD 파일 디렉토리를 반복하고, 획 효과를 적용하고, 결과를 자동으로 저장할 수 있습니다.

### Java용 Aspose.PSD를 사용하여 PSD 파일의 변경 사항을 되돌리려면 어떻게 해야 합니까?
변경 사항을 되돌리려면 수정 사항을 저장하기 전에 원본 PSD 파일을 다시 로드해야 합니다. Aspose.PSD에는 직접적인 실행 취소 기능이 없습니다.

### 획 너비와 위치를 사용자 정의할 수 있나요?
 예, Java용 Aspose.PSD를 사용하면 획 너비, 위치 및 기타 속성을 사용자 정의할 수 있습니다.`StrokeEffect` 수업.

### Java 라이브러리용 Aspose.PSD는 무료로 사용할 수 있나요?
 Aspose.PSD for Java는 무료 평가판을 제공하지만 모든 기능에 완전히 액세스하려면 라이센스를 구입해야 합니다. 당신은 탐색 할 수 있습니다[옵션 구매](https://purchase.aspose.com/buy)그들의 웹사이트에서.