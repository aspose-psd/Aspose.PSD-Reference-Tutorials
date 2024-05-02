---
title: Java용 Aspose.PSD에 패턴 효과 추가
linktitle: 패턴 효과 추가
second_title: Aspose.PSD 자바 API
description: Java용 Aspose.PSD를 사용하여 Java 이미지 패턴을 손쉽게 향상하세요. 매혹적인 패턴 효과를 추가하려면 단계별 튜토리얼을 따르세요.
type: docs
weight: 12
url: /ko/java/advanced-image-effects/add-pattern-effects/
---
## 소개

Java 개발 세계에서는 이미지 패턴을 강화하는 것이 일반적인 작업이며 Java용 Aspose.PSD는 이에 대한 강력한 솔루션을 제공합니다. 이 튜토리얼은 Aspose.PSD를 사용하여 패턴 효과를 추가하는 과정을 안내하여 고유한 오버레이 및 향상 기능으로 이미지를 돋보이게 합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
-  Java 라이브러리용 Aspose.PSD가 다운로드되어 프로젝트에 추가되었습니다. 다음에서 다운로드할 수 있습니다.[Aspose.PSD 웹사이트](https://releases.aspose.com/psd/java/).

## 패키지 가져오기

Java 프로젝트에서 Aspose.PSD 작업에 필요한 패키지를 가져옵니다. Java 클래스 시작 부분에 다음 코드를 포함합니다.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## 1단계: 이미지 로드

```java
// PSD 이미지 로드
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

"YourImagePath" 및 "YourExportPath"를 프로젝트의 실제 경로로 바꾸십시오.

## 2단계: 패턴 오버레이 정보 추출

```java
// 패턴 오버레이에 대한 정보 추출
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## 3단계: 패턴 오버레이 설정 수정

```java
// 패턴 오버레이 설정 수정
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## 4단계: 패턴 데이터 편집

```java
// 패턴 데이터 편집
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## 5단계: 편집된 이미지 저장

```java
// 편집한 이미지를 저장하세요
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## 6단계: 변경 사항 확인

```java
// 편집된 파일의 변경 사항 확인
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// 변경 사항이 성공적으로 적용되었는지 확인하기 위해 어설션을 추가합니다.
```

## 결론

축하해요! Java용 Aspose.PSD를 사용하여 패턴 효과를 추가하는 방법을 성공적으로 배웠습니다. 이 강력한 라이브러리를 사용하면 사용자 정의된 패턴으로 시각적으로 매력적인 이미지를 생성하여 Java 기반 프로젝트에 무한한 가능성을 제공할 수 있습니다.

## FAQ

### Q1: 다른 Java 이미지 처리 라이브러리와 함께 Java용 Aspose.PSD를 사용할 수 있나요?

A1: Aspose.PSD for Java는 독립적으로 작동하도록 설계되었지만 필요한 경우 다른 Java 라이브러리와 통합할 수 있습니다.

### Q2: Java용 Aspose.PSD에 대한 자세한 문서는 어디에서 찾을 수 있습니까?

 A2: 다음을 참조하세요.[Java 문서용 Aspose.PSD](https://reference.aspose.com/psd/java/) 포괄적인 정보를 얻으려면.

### Q3: Aspose.PSD for Java에 대한 무료 평가판이 있습니까?

 A3: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Java용 Aspose.PSD에 대한 지원을 어떻게 받을 수 있나요?

 A4: 다음을 방문하세요.[Aspose.PSD 포럼](https://forum.aspose.com/c/psd/34) 지역 사회 지원을 원하거나 지원 계획 구입을 고려하십시오.

### Q5: Java용 Aspose.PSD의 임시 라이선스를 얻을 수 있나요?

A5: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).