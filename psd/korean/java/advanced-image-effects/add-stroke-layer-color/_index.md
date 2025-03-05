---
title: Java용 Aspose.PSD에 스트로크 레이어 색상 추가
linktitle: 획 레이어 색상 추가
second_title: Aspose.PSD 자바 API
description: 스트로크 레이어 색상 추가에 대한 단계별 가이드를 통해 Java용 Aspose.PSD의 강력한 기능을 살펴보세요. 그래픽 디자인을 손쉽게 향상시켜 보세요.
type: docs
weight: 14
url: /ko/java/advanced-image-effects/add-stroke-layer-color/
---
## 소개

Aspose.PSD를 사용하여 Java 애플리케이션의 그래픽 디자인 잠재력을 활용해 보세요. 이 튜토리얼에서는 Java용 Aspose.PSD를 사용하여 획 레이어 색상을 추가하는 흥미로운 세계를 탐구합니다. 눈에 띄는 획으로 그래픽을 향상시켜 시각적으로 매력적인 디자인을 손쉽게 만들어 보세요.

## 전제조건

이 창의적인 여정을 시작하기 전에 다음과 같은 전제 조건이 갖추어져 있는지 확인하세요.

-  Aspose.PSD 라이브러리: 다음을 따라 Aspose.PSD 라이브러리를 다운로드하고 설정하세요.[선적 서류 비치](https://reference.aspose.com/psd/java/).

- JDK(Java Development Kit): 시스템에 Java가 설치되어 있는지 확인하세요.

- 통합 개발 환경(IDE): 원하는 IDE를 선택하세요. Eclipse 또는 IntelliJ가 널리 사용됩니다.

## 패키지 가져오기

Aspose.PSD 마법이 일어나도록 하기 위해 필요한 패키지를 가져오는 것부터 시작해 보겠습니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 1단계: 프로젝트 설정

선호하는 IDE에서 새 Java 프로젝트를 생성하는 것부터 시작하세요. Aspose.PSD 라이브러리가 프로젝트에 추가되었는지 확인하세요.

## 2단계: PSD 파일 로드

Aspose.PSD를 사용하여 PSD 파일을 로드하면 효과 리소스를 로드할 수 있습니다.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## 3단계: 스트로크 레이어에 액세스

PSD 파일 내의 획 효과 레이어에 액세스합니다.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## 4단계: 획 속성 확인

스트로크 속성이 예상한 대로인지 확인합니다.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## 5단계: 색상 및 불투명도 설정

획 레이어의 색상과 불투명도를 수정합니다.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## 6단계: 수정된 PSD 저장

새로 추가된 스트로크 레이어 색상으로 수정된 PSD 파일을 저장합니다.

```java
im.save(exportPath);
```

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 PSD 파일에 스트로크 레이어 색상을 성공적으로 추가했습니다. 다양한 색상과 설정을 실험하여 그래픽 디자인에 생기를 불어넣으세요.

## FAQ

### Q1: Aspose.PSD를 다른 Java 그래픽 라이브러리와 함께 사용할 수 있습니까?

A1: 예, Aspose.PSD는 향상된 기능을 위해 다른 Java 그래픽 라이브러리와 통합될 수 있습니다.

### Q2: Aspose.PSD는 최신 PSD 파일 형식과 호환됩니까?

A2: 물론이죠! Aspose.PSD는 최신 PSD 파일 형식 사양과 보조를 맞춰 호환성을 보장합니다.

### Q3: Aspose.PSD를 사용하는 동안 예외를 어떻게 처리합니까?

 A3: 다음을 참조하세요.[지원 포럼](https://forum.aspose.com/c/psd/34) 예외 처리 및 문제 해결에 대한 지원을 받으려면

### Q4: 구매하기 전에 Aspose.PSD를 사용해 볼 수 있나요?

 A4: 물론이죠! 잡아[무료 평가판](https://releases.aspose.com/) 약속을 하기 전에 Aspose.PSD의 기능을 살펴보세요.

### Q5: Aspose.PSD 임시 라이선스는 어디서 구할 수 있나요?

 A5: 획득[임시면허](https://purchase.aspose.com/temporary-license/) Aspose.PSD가 프로젝트의 기능을 평가합니다.